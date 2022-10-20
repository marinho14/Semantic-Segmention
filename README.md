# Semantic Segmention

## How to run the main code?

### Main

<p align="justify"> In the following Notebook you will find the results with images of the Test Folder. </p>

- [Main](main.ipynb)

- ***It is important to have the Train and Test folders at the same level as the Notebooks for proper operation.***

### Requirements

For this project, a virtual environment with python 3.8.13 was used. The packages and their versions are in the following file.

- [Requirements.txt](requirements.txt)

## Approach to the problem

### Semantic segmention

***To understand how to solve the semantic segmentation task, a model was created for it, but it is important to clarify that only ONE model was used to solve both tasks, as shown below.***

<p align="justify"> The first step that was carried out was the understanding of what semantic segmentation is and how it could be solved. </p>

<p align="justify">
At first it was decided to build a Neural Network model from scratch, but since unsatisfactory results and a very high training time were obtained, a pre-trained Tensorflow Unet network was implemented. The following Notebook shows the development of this first approach and its respective entry:</p>

- [Train Semantic Segmentation Model](Train_seg_sem.ipynb)

<p align="justify">
Below is an image of the result after training only the Semantic Segmentation model.  </p>

<p >
   <img src=Imagenes\Resul_seg_1.jpeg>
</p>


### Semantic segmention and Image Level Classification in One Model

<p >
As it was requested that a single model be used for the prediction of semantic segmentation and Image Level Classification, it was decided to use a model where the previously created model and other layers were implemented to give two outputs, the design model would be of the next way. </p>


<p >
   <img src=Imagenes\Model_rw.png>
</p>


<p align="justify">
Subsequently, the neural network was trained to output the complete model. This training is found in the following Notebook:</p>

- [Train Complete Model](Train_label_seg.ipynb)

## Results

<p align="justify">
Below are the results of the network, where the titles show, the image, what it should be, and the output of the network
</p>

<p >
   <img src=Imagenes\Resul_complete.jpeg>
</p>

<p >
   <img src=Imagenes\resul_3.PNG>
</p>


**In training, a mean_iou of 94% and an accuracy of 90% were reached.**


## Submissions 

<p align="justify">In this Notebook you will find the code to save the output images of the dataset and their respective Image Level Classification for the competition in codalab</p>

- [Submissions](Save_test.ipynb)

<p align="justify">
The zips that were used in the competition are focused on the following folder, in the name of the zip are the scores obtained in the competition</p>

- [zips](submissions)

## Conclusions 

- According to the results of the competition, it could be intuited that the network is overtrained, since in the training and test results of 94% were obtained for mean_iou and 90% for accuracy and f1. The results of the competition were 38%, 78% and 78% respectively.

- To try to reduce overfitting, I tried to improve by training only the semantic segmentation network, since there were 3,000 images with its segmentation and only 2,000 with the two labels.

- Something that could improve the model could be to enter the depth image to obtain better results

- Reading about semantic segmentation, you have the problem that your data may be unbalanced, so a solution would be to apply methods and functions to improve the model.
 
- Open and willing to learn and listen how to improve the model and how to achieve better results :)

- An attempt was made to improve overfitting by reducing the size of the convolutional network filters but no significant improvement was seen. I also tried to increase the number of test images



