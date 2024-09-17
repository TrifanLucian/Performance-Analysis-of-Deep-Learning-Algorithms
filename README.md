# Performance-Analysis-of-Deep-Learning-Algorithms

<p><b>Summary</b></p>
For testing the algorithms, a classification problem is chosen. The three selected classes are apples, oranges, and peaches. Part of the dataset used will be downloaded from the internet, with pre-labeled images, while another part will be downloaded through available APIs. Statistical analyses will be conducted on the images to observe later if they influence the network's performance. The quality of the classification will be checked by the density of edges detected in each image using the Sobel filter. Edges are key features learned by convolutional neural networks (CNN), which is why the verification of deep learning algorithms will be done using statistical metrics such as skewness, kurtosis, and standard deviation, extracted from the edge density histograms.

Four deep neural networks will be created, two using transfer learning and two custom-built, followed by training on the datasets. Comparisons will be made between the models' performances based on different parameters such as the number of epochs, and conclusions will be drawn regarding the optimization of the neural network design process.

<p><b>Dataset:</b></p>
The Apple2Orange and Flickr Image Peaches datasets were used to test the accuracy of fruit classification. The original images have a resolution of 256x256 pixels, and during preprocessing, they were resized to either 80x80 pixels or 224x224 pixels depending on the network used. The images are represented in the RGB color model (red, green, and blue). Images from the third class (peaches) were downloaded using the FLICKR API. The algorithm used is a Python script that leverages the Flickr API to search for and download images, as well as resize those images to 256x256 pixels. The "flickr.photos.search" method is used to download images, returning a list of photos matching the search criteria (provided as method parameters) and the corresponding URLs for each photo. The image is then copied from the URL using Python’s urllib module and the urllib.request.urlretrieve method. The number of images in each category is found in the table below:

<table>
  <tr>
    <th>Fruit</th>
    <th>Training Set</th>
    <th>Test Set</th>
  </tr>
  <tr>
    <td>Apples</td>
    <td>995 (79%)</td>
    <td>266 (21%)</td>
  </tr>
  <tr>
    <td>Peaches</td>
    <td>1019 (80%)</td>
    <td>248 (20%)</td>
  </tr>
  <tr>
    <td>Oranges</td>
    <td>999 (85%)</td>
    <td>176 (15%)</td>
  </tr>
</table>

![image](https://github.com/user-attachments/assets/759482be-9a9d-4f40-b02f-8c0caf5c2f68) ![image](https://github.com/user-attachments/assets/5abc7005-ddb5-49af-9348-a6e84345ff1e)

In order to extract structural information from images and to compare the three classes (apples, oranges, and peaches), several statistical calculations will be performed based on edge intensity in the images. To generate them, the Sobel filter will be used, which is a first-order derivative filter. 

By detecting edges, convolutional networks can identify fundamental structures in the image, which are essential for the subsequent recognition of objects.

![image](https://github.com/user-attachments/assets/4125ce99-635a-41a9-8320-0a3c1eb80029) ![image](https://github.com/user-attachments/assets/7bec1d3a-948a-49c6-81cc-804d511aaf92) ![image](https://github.com/user-attachments/assets/a6feaafe-fb31-46bd-80d1-ee3649afd4fd)

<p><b>Statistical Analyses:</b></p>

Based on histograms (projections), the horizontal and vertical standard deviation is calculated to measure the dispersion or how scattered the values are relative to the mean. In this way, we can evaluate the variation in edge intensity along the two axes.

Additionally, we will measure the skewness of the probability distribution of vertical and horizontal projections/profiles for each image. Positive skewness can indicate that the distribution tail is longer to the right, while negative skewness suggests a longer tail to the left. This allows us to determine the predominance of certain edge directions in each image.

The last statistical measure we perform on the images is kurtosis. It measures the peaks and tails of a distribution compared to a normal distribution. A kurtosis value greater than 3 indicates a distribution with longer tails and sharper peaks, while a kurtosis value less than 3 suggests a flatter distribution with shorter tails. Vertical and horizontal kurtosis can provide insights into the image's uniformity and the extreme variability of edge intensity.

Violin plots combine the features of a boxplot with those of a probability distribution to provide a detailed visualization of data distribution. The width of the violin describes how frequently a value appears in the dataset. Wider regions of the density plot indicate values that occur most often. Two lines are plotted on the violin graph representing the mean and the median. The mean shows the average value of the data, which is sensitive to extreme values, while the median splits the dataset into two equal parts and is not influenced by extreme values. This provides a complete picture of data distribution, including information about centrality and variation.

examples of generated graphs
![image](https://github.com/user-attachments/assets/be2f47cb-854c-47ea-acc4-233d0f1d48f8)
![image](https://github.com/user-attachments/assets/f66a45ec-b483-440f-ac91-b4db76443f7a)

<p><b>DNN and CNN architectures:</b></p>
Designing the best models can present unique challenges depending on the classification's particularities.

To evaluate network performance, two deep learning algorithms will be used: a deep neural network without convolutional layers (DNN) and a deep neural network with convolutional layers (CNN).

In general, optimizing and training the model is a difficult process that requires significant time. Training requires a graphical processing unit (GPU) and millions of training examples. These challenges can be addressed through transfer learning. In this case, two adapted architectures, AlexNet and GoogLeNet, were used to build the models, which were then trained with the datasets (apples, oranges, and peaches).

<p>an example of classification used in the project:</p>

![image](https://github.com/user-attachments/assets/e7370f61-cd53-4323-89a3-b00567944525)
![image](https://github.com/user-attachments/assets/525b76d1-20c7-4de9-845a-0610342930ff)

<p>some achieved performances:</p>

![image](https://github.com/user-attachments/assets/9d2bb5a4-1a02-4e33-94b3-517be5cd35ef)




 


 
 

