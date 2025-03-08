Requirements :
CUDA GPU Nvidia A-100
`Note: We are not working over the TPU & CPU if you do not have CUDA technology enabled GPU you will bydefault woek on CPU`

## Jupyter Notebook model for Neural Style Transfer utilising CUDA GPU Technology

## We introduce a computer system based on a Deep Neural Network, capable of producing artistic images with exceptionally high visual quality. This system uses neural representations  to separate and then combine the content and style elements from any given images.Essentially, it offers a computerized method for creating artistic images.

## Image Reconstruction
![image](https://github.com/Ashish-Waykar/Neural-Style-Transfer-Deep-Learning-Root-AI-Model/assets/81794601/2f4df1d7-40ef-4139-a1d4-860082a3cc3b)
We can virtualize the information on different processing stages of layers in CNN with re-building the input image from only knowing the network’s responses in several layers.We rebuild the input image from layers ‘conv1 1’ (We can virtualize the information on different processing stages of layers in CNN with re-building the input imagefrom only knowing the network’s responses in several layer), ‘conv2 1’ (b), ‘conv3 1’ (c), ‘conv4 1’ (d) and ‘conv5 1’ (e) of the original pretrained VGG19-Network.

## 02 Style Reconstruction
On top of the original CNN layers representations we built a new feature space layers that captures the style of an input image. The style representation computes correlations between the different features units in different layers of the CNN. • Where presentations built on different subsets of CNN layers ( ‘conv1 1’ (a), ‘conv1 1’ and ‘conv2 1’ (b), ‘conv1 1’, ‘conv2 1’ and ‘conv3 1’ (c), ‘conv1 1’, ‘conv2 1’, ‘conv3 1’ and ‘conv4 1’ (d), ‘conv1 1’, ‘conv2 1’, ‘conv3 1’, ‘conv4 1’ and ‘conv5 1’ (e)). • We reconstruct the style of the input image from style This creates images that match the style of a input image on an highly increasing scale while discarding information of the default arrangement of the scene.

## 03 VGG19 ARCHITECTURE
![image](https://github.com/Ashish-Waykar/Neural-Style-Transfer-Deep-Learning-Root-AI-Model/assets/81794601/5baedbab-8439-4613-b406-368f6aa5a066)

## 04 How we work for this modal 
![image](https://github.com/Ashish-Waykar/Neural-Style-Transfer-Deep-Learning-Root-AI-Model/assets/81794601/4b2c7e1f-efb5-4fd7-933a-100429cd2a78)
VGG19 network is used for Neural Style transfer. VGG-19 is a convolutional neural network that is trained on more than a 14 million images from the ImageNet database. The network is 19 layers deep and trained on millions of images. Because of which it is able to detect high-level features in an image.
Now, this ‘encoding nature’ of CNN’s is the key in Neural Style Transfer. Firstly, we initialize a noisy image, which is going to be our output image(G). We then calculate how similar is this image to the content and style image at a particular layer in the network(VGG network). Since we want that our output image(G) should have the content of the content image(C) and style of style image(S) we calculate the loss of generated image(G) with respective to the respective content(C) and style(S) image. • Similar datasets Resnet18 , AlexNet actually VGG19pretrained will use the ImageNet dataset where it has been trained over 14 million images from ImageNet.

## 05 Representation of each layer with respect to style transfer 
![image](https://github.com/Ashish-Waykar/Neural-Style-Transfer-Deep-Learning-Root-AI-Model/assets/81794601/bbec90a1-4829-40cc-ae3c-20cf75b3c937)
The image is represented by collection of filtered images with each processing stage in CNN. While number of multiple filters are increasing with processing. The size of the above filtered images are reduced by some down sampling mechanisms MAX POOLING leading the total number of units per layer network

![image](https://github.com/Ashish-Waykar/Neural-Style-Transfer-Deep-Learning-Root-AI-Model/assets/81794601/36a23cf9-8f9d-4ec0-b5bf-3236ccda8de8)
