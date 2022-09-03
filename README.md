# Generating Voronoi Images

## Table of contents
* [Introduction](#Introduction)
* [Generating_Diverse_Images](#Generating_diverse_Images)
* [Technologies](#technologies)
* [Repository Contents](#Repository_Contents)
* [Methodology](#Methodology)

## Introduction:

 
Voronoi images have applications in different fields. For example, in natural sciences, it is possible to explain biological structures by them. They have also many applications in Engineering and Urban Management. The task of this project was to generate Voronoi images that can be used for image Labeling. The images are generated randomly, and they are saved in a PyTorch tensor. The script has been made in a way to generate a wide of Voronoi images.


## Generating_Diverse_Images
* It is possible to generate a wide variety of images. The followings are configurable:
* The batch which is the number of images
* Image size
* RGB or Grayscale
* Number of randomly sampled points for each image
* The thickness of boundaries between cells
* Possibility of highlighting the vertices. I have to explain when the numebr of voronoi points in an image is small it works well, but when the number of points is large, it decreases the quality of image. Thefrefore, it is suggested to use this option when the number of random points is less than 40
* Possibility of showing the Voronoi point of each cell
* Choosing the desired size for the Voronoi point
* The possibility of saving the output PyTorch tensor as a file with .pt format
* The seed for randomness




	
## Technologies
* The code has been implemented in Python version 3.8.8
* The following Libraries have been used to generate the images which are: 
* Torch version 1.12.1
* SciPy version 1.6.2 
* NumPy version 1.20.1
* PIL version 8.2.0
* matplotlib version 3.3.4

## Repository Contents
* The main files of the task are final_project.py, final_project_test.py, final_project_test.ipynb. the file final_project_test.ipynb works well in GoogleColab
* A bunch of images that can be generated by the script have been in the folder image samples
* The other files have been generated in different steps of the project

## Methodology
* It is suggested to run the script final_project_test.py. The needed information is gotten from the user to generate images. It is suggested to the data carefully
* Firstly, the needed information is gotten from the user. Based on the number of batches, a for loop is run for each image. With the help of the scipy.spatial which has Voronoi, voronoi_plot_2d, the image is generated in the format of matplotlib. Then the image is stored with the name of image.png in the directory where the script is run.  After that, the image.png is opened as Grayscales or RGB and it is resized to the desired size. After that, it is transformed into a PyTorch tensor, and it is added to the image_tensor. Again, the for loop is run for the second image and it is overwritten on the previous image. Therefore, at each moment, just one image is in the directory
* For each user some options are important. For example,  a user needs to generate images that has a speicail number for the thickness of boundaries while the other user may want to have images whose voronoi points have a size of 3. Thereofre, it is not compulsory that each user try to modify all the options

* All the generated images are stored in a PyTorch tensor named image_tensor which has 4 dimensions, which are [batch, channel, height, width]
* It is known that the goal is to store the images as PyTorch tensors, and it is not needed to save images in .png format. Just to show that the code works correctly, the first image is converted from a PyTorch tensor to an image in the format of img1.png
* cell_Colors function colors each cell randomly
* The boundary lines are the same for each image, and it is colored randomly by the boundary_Colors function
* It is also possible to save the output of the script as a file with the format of .pt






