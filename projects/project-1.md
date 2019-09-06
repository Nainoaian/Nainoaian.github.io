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

For this project, I was the lead programmer who was responsible for programming the various capabilities of the mouse.  I started by programming the basics, such as sensor polling and motor actuation using interrupts.  From there, I then programmed the basic PD controls for the motors of the mouse.  The PD control the drive so that the mouse would stay centered while traversing the maze and keep the mouse driving straight.  I also programmed basic algorithms used to solve the maze such as a right wall hugger and a left wall hugger algorithm.  From there I worked on a flood-fill algorithm to help the mouse track where it is in the maze, and to map the route it takes.  We finished with the fastest mouse who finished the maze within our college.

Here is some code that illustrates how we read values from the line sensors:

```js
byte ADCRead(byte ch)
{
    word value;
    ADC1SC1 = ch;
    while (ADC1SC1_COCO != 1)
    {   // wait until ADC conversion is completed   
    }
    return ADC1RL;  // lower 8-bit value out of 10-bit data from the ADC
}
```

You can learn more at the [UH Micromouse Website](http://www-ee.eng.hawaii.edu/~mmouse/about.html).



