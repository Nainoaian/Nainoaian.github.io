---
layout: project
type: project
image: images/LongerImage.JPG
title: Cell Detection AI
permalink: projects/Cell_Detection_AI
# All dates must be YYYY-MM-DD format!
date: 2019-05-15
labels:
  - Machine Learning
  - Jupyter Notebook
  - TensorFlow
  - Python
summary: Using Jupyter Notebook with the Tensorflow library, I trained a neural net to detect and identify the level of healthy cells within a slide. 
---

<div class="ui small rounded images">
  <img class="ui image" src="../images/SHSY5Y_FUtreat_2017-06-01-142934-0000_4.jpg">
  <img class="ui image" src="../images/cat.2068.jpg">
  <img class="ui image" src="../images/dog.2081.jpg">
  <img class="ui image" src="../images/SampleMatrix.JPG">
</div>

This project started out with obtaining the dataset of cell images. This was made possible through the use of HNU Photonics' biochip, which is a small container containg a sample of cells with the intention of observing their reaction to certain environments. It was later established that this technology could be used to observe the reaction of cells to certain types of cancer treatment. With HNU providing the hardware, I along with AlgorithmHub set out to design a software that could be given the images and in turn, provide a count on the number of healthy cells that were present.Another goal for this project was to get the machine learning model to a state where it could record the varying level of healthy cells over a period of time and return a line graph based off of this change in the cell count. 

As I designed the neural net, I encountered several obstacles along the way. Some of them were easily solvable and only involved a change in the syntax, others involved some level of creativity and intuition. My first issue being that even though image identification is relatively easy for a neural net to do, object detection is quite a bit more difficult. To fix this, I used the labellmg tool to draw bounding boxes over each of the healthy cells and the pascal VOC-to-Images python tool to turn each of those bounding boxes into it's own separate image. The idea here was to train the neural net on these smaller single cell images with the intention of adapting the neural net to identify the cells in whole pictures later. The results of deriving images from my labelling can be seen below. 

<div class="ui small rounded images">
  <img class="ui image" src="../images/Tcell2.jpg">
  <img class="ui image" src="../images/Tcell3.jpg">
  <img class="ui image" src="../images/Tcell4.jpg">
  <img class="ui image" src="../images/Tcell5.jpg">
  <img class="ui image" src="../images/Tcell6.jpg">
  <img class="ui image" src="../images/Tcell7.jpg">
</div>



