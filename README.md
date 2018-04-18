# ECSE 421: Embedded Systems Labs
### McGill University, Montreal, Canada
### Author: Adam Cavatassi, MEng Candidate

Last Update: April 2018

## Introduction
The labs in this introductory embedded systems course are based on the labs taken by Dr. Brett Meyer (McGill University) in previous years under the direction of Dr. Jeremy Cooperstock (McGill University). These labs are designed to introduce students to machine learning with an incremental approach, while also challenging students to work with the limitations of real-time embedded systems. The students work their way up to the final project by implementing the forward and backward pass of a neural network in the labs leading up to the project. The labs lead the students to learn the basics of neural networks with a simple position detection task, making use of the accelerometer in the *National Instruments* **myRIO-1900** development board. This approach allows students to ease their way into the final project, which features a new [MNIST](http://yann.lecun.com/exdb/mnist/)-inspired learning task unique from that the previous labs. 

## Lab 1
Serves as an introduction to the *National Instruments* **LabVIEW** environment. Based on the National Instruments finite state machine [tutorial](http://www.ni.com/tutorial/7595/en/), students are required to implement a simple vending machine.

## Lab 2
Using the myRIO-1900, students must initialize the on-board accelerometer. The accelerometer signals must be passed through an adjustable lowpass filter and used to compute the roll and pitch angles of the myRIO. These five signals are to be collected into uniform arrays for future use. 

## Lab 3
Students must implement a real-time inference engine based on a pre-trained neural network, named *Position-Net*. Weight matrices are provided to be able to build a fully connected network which uses the sigmoid function as an activation. The pre-trained network accepts a time sample from the five signals acquired in Lab 2 as an input vector, and predicts which of three predetermined positions the myRIO-1900 is currently in. The position classification is indicated by the LEDs on the board.


| ![alt text](https://github.com/adamcavatassi/McGill-ECSE-421-Embedded-Systems-Labs/blob/master/Lab%203/Specifications/figs/pos0.png "Position 0") | ![alt text](https://github.com/adamcavatassi/McGill-ECSE-421-Embedded-Systems-Labs/blob/master/Lab%203/Specifications/figs/pos1.png "Position 2") | ![alt text](https://github.com/adamcavatassi/McGill-ECSE-421-Embedded-Systems-Labs/blob/master/Lab%203/Specifications/figs/pos2.png "Position 2") |
|Position 0 | Position 1 | Position 2 |

## Lab 4
Students are to recreate their inference engine from Lab 3 by training the neural network themselves and obtaining their own weight matrices. This requires the implementation of the backpropagation algorithm. A training set of 1500 examples is provided to accomplish the task.

## Final Project
Inspired by the [MNIST](http://yann.lecun.com/exdb/mnist/) classification task, this project requires that students implement a neural network which will recognize imaginary hand-drawn digits in the air using the myRIO-1900 accelerometer as an input. Students must generate their own training set and explore the network architecture design space to produce an optimal solution.

