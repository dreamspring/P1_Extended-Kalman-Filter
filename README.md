# Extended Kalman Filter Project
Self-Driving Car Engineer Nanodegree Program, Project 1

## Overview
In this project, I utilized a kalman filter using C++ code to estimate the state of a moving object of interest with noisy lidar and radar measurements. 

## Basic Build Instructions
The project has the following dependencies (from Udacity's seed project):

cmake >= 3.5
make >= 4.1
gcc/g++ >= 5.4

To build the project:
1. Clone this repo.
2. Make a build directory: `mkdir build && cd build`
3. Compile: `cmake .. && make` 
   * On windows, you may need to run: `cmake .. -G "Unix Makefiles" && make`
4. Run it: `./ExtendedKF `

To run the code:
Set the build directory as current directory, then run ./ExtendedKF.
The following words will be shown on screen: Listening to port 4567.
Then run the simulator. There are two dataset sets in the simulator.

## Results
Results with dataset 1:

The RSME is calculated: 
X: 0.0973;  Y: 0.0855;  VX: 0.4513;  VY: 0.4399

Snapshot from simulator:

![Test One Visualization](https://github.com/dreamspring/P1_Extended-Kalman-Filter/blob/master/pic_dataset1.png "Test One Visualization")

Results with dataset 2:

The RSME is calculated: 
X: 0.0726;  Y: 0.0965;  VX: 0.4216;  VY: 0.4932

Snapshot from simulator:

![Test One Visualization](https://github.com/dreamspring/P1_Extended-Kalman-Filter/blob/master/pic_dataset2.png "Test One Visualization")









