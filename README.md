# Performance-Analysis-of-Deep-Learning-Algorithms

Summary
For testing the algorithms, a classification problem is chosen. The three selected classes are apples, oranges, and peaches. Part of the dataset used will be downloaded from the internet, with pre-labeled images, while another part will be downloaded through available APIs. Statistical analyses will be conducted on the images to observe later if they influence the network's performance. The quality of the classification will be checked by the density of edges detected in each image using the Sobel filter. Edges are key features learned by convolutional neural networks (CNN), which is why the verification of deep learning algorithms will be done using statistical metrics such as skewness, kurtosis, and standard deviation, extracted from the edge density histograms.

Four deep neural networks will be created, two using transfer learning and two custom-built, followed by training on the datasets. Comparisons will be made between the models' performances based on different parameters such as the number of epochs, and conclusions will be drawn regarding the optimization of the neural network design process.

Dataset:
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



 
 

