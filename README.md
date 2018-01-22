# CarND-Controls-PID
Self-Driving Car Engineer Nanodegree Program

---
# Overview

The three main components to control in driving a vehicle are steering, throttling, and braking. It sounds simple for human to drive the vehicle because human can interact to these components smoothly and adapt to the condition of driving. On the other hand, it is a very complicate task in self-driving vehicle to control these components. To solve the job for self-driving vehicle to control these components, there are many technologies that could be used. PID is considered the most practical technology and it has implemented in self-driving vehicle today. This project is using PID controller to drive the self-driving car and it is coding by using C++ programming.

## Project Introduction
The purpose of this project is using C++ to design a PID system to control the self-driving car. This project produces a program that is connected to the simulator by getting the data from the simulator and predicting the steering angle and acceleration speed and brake to make sure that the car will keep driving on the lane. 

## Running the Code
This project involves the Term 2 Simulator which can be downloaded [here](https://github.com/udacity/self-driving-car-sim/releases)

This repository includes two files that can be used to set up and intall uWebSocketIO for either Linux or Mac systems. For windows you can use either Docker, VMware, or even Windows 10 Bash on Ubuntu to install uWebSocketIO.

Once the install for uWebSocketIO is complete, the main program can be built and ran by doing the following from the project top directory.

1. mkdir build
2. cd build
3. cmake ..
4. make
5. ./pid

From the `build` directory, execute `./pid`. The output should be:

```
Listening to port 4567
Connected!!!
```

## Input Data into PID Controller

> * The input data such as cte ( cross track error), speed, and steering angle into the PID system is provided by simulator.

## Output of the PID Controller

All components of PID are affected to the performance of the controller.

- P: in case that only P is turn on and D and I are off, the car could drive it self for about 20 seconds and then it get off track. It is expected for the result like this because while only P is activated the system could not solve the problem of the cte. 

<a href="https://youtu.be/0tfK9QU9omE" target="blank"><img scr="https://github.com/loynin/SDND-09-PID-Control-Project/blob/master/images/image1.png" /></a>
[![Video of PID Controller with D and I  are Turn
Off](https://github.com/loynin/SDND-09-PID-Control-Project/blob/master/images/image1.png)](https://youtu.be/0tfK9QU9omE){:target="_blank"}

---

Here is the simulator final state after running the particle filter:

<kbd>
<img src="images/image3.png" />
</kbd>

---


## Dependencies

* cmake >= 3.5
 * All OSes: [click here for installation instructions](https://cmake.org/install/)
* make >= 4.1(mac, linux), 3.81(Windows)
  * Linux: make is installed by default on most Linux distros
  * Mac: [install Xcode command line tools to get make](https://developer.apple.com/xcode/features/)
  * Windows: [Click here for installation instructions](http://gnuwin32.sourceforge.net/packages/make.htm)
* gcc/g++ >= 5.4
  * Linux: gcc / g++ is installed by default on most Linux distros
  * Mac: same deal as make - [install Xcode command line tools]((https://developer.apple.com/xcode/features/)
  * Windows: recommend using [MinGW](http://www.mingw.org/)
* [uWebSockets](https://github.com/uWebSockets/uWebSockets)
  * Run either `./install-mac.sh` or `./install-ubuntu.sh`.
  * If you install from source, checkout to commit `e94b6e1`, i.e.
    ```
    git clone https://github.com/uWebSockets/uWebSockets 
    cd uWebSockets
    git checkout e94b6e1
    ```
    Some function signatures have changed in v0.14.x. See [this PR](https://github.com/udacity/CarND-MPC-Project/pull/3) for more details.
* Simulator. You can download these from the [project intro page](https://github.com/udacity/self-driving-car-sim/releases) in the classroom.

There's an experimental patch for windows in this [PR](https://github.com/udacity/CarND-PID-Control-Project/pull/3)

## Basic Build Instructions

1. Clone this repo.
2. Make a build directory: `mkdir build && cd build`
3. Compile: `cmake .. && make`
4. Run it: `./pid`. 

Tips for setting up your environment can be found [here](https://classroom.udacity.com/nanodegrees/nd013/parts/40f38239-66b6-46ec-ae68-03afd8a601c8/modules/0949fca6-b379-42af-a919-ee50aa304e6a/lessons/f758c44c-5e40-4e01-93b5-1a82aa4e044f/concepts/23d376c7-0195-4276-bdf0-e02f1f3c665d)

## Project Instructions and Rubric

Note: regardless of the changes you make, your project must be buildable using
cmake and make!

More information is only accessible by people who are already enrolled in Term 2
of CarND. If you are enrolled, see [the project page](https://classroom.udacity.com/nanodegrees/nd013/parts/40f38239-66b6-46ec-ae68-03afd8a601c8/modules/f1820894-8322-4bb3-81aa-b26b3c6dcbaf/lessons/e8235395-22dd-4b87-88e0-d108c5e5bbf4/concepts/6a4d8d42-6a04-4aa6-b284-1697c0fd6562)
for instructions and the project rubric.



