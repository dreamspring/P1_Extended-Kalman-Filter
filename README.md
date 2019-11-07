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
Set the build directory as current directory, then run ./ExtendedKF. <br />
The following words will be shown on screen: Listening to port 4567. <br />
Then run the simulator. There are two dataset sets in the simulator. <br />

## Data
Lidar data example: <br />
L	3.122427e-01	5.803398e-01	1477010443000000	6.000000e-01	6.000000e-01	5.199937e+00	   0	    0	    6.911322e-03 <br />
L-----px------------py------------time step---------x_gt----------y_gt----------vx_gt-----vy_gt  <br />

R	1.014e+00	5.529e-01	4.892e+00	1477010443050000	8.599e-01	6.000e-01	5.1997e+00	1.796e-03	3.455e-04	1.382e-02 <br />
R-----rho-----theta------rho_dot--------time step----------x_gt-------y_gt-------vx_gt------vy_gt  <br />

time step is 1.0e-6 second. <br />
x_gt, y_gt, vx_gt and vy_gt are ground truth values. <br />
	
## Extended Kalman Filter
![Test One Visualization](https://github.com/dreamspring/P1_Extended-Kalman-Filter/blob/master/2019-11-06%2022_38_14-Extended%20Kalman%20filter%20-%20Wikipedia.png "First Order Extended Kalman Filter")

First-order extended Kalman filter (EKF) is obtained by retaining the first term of the Taylor series expansions. <br />

![Test One Visualization](https://github.com/dreamspring/P1_Extended-Kalman-Filter/blob/master/2019-11-06%2022_55_51-Extended%20Kalman%20filter%20-%20Wikipedia.png "Continuous-time Extended Kalman Filter")

P is state covariance matrix. <br />
F is state transition matrix. <br />
H is measurement matrix. <br />
Q is a covariance matrix associated with the noise in states. <br />
R is the covariance matrix of the measurement noise. <br />

## Results
Results with dataset 1:

The RMSE is calculated: 
X: 0.0973;  Y: 0.0855;  VX: 0.4513;  VY: 0.4399

Snapshot from simulator:

![Test One Visualization](https://github.com/dreamspring/P1_Extended-Kalman-Filter/blob/master/pic_dataset1.png "Test One Visualization")

Results with dataset 2:

The RMSE is calculated: 
X: 0.0726;  Y: 0.0965;  VX: 0.4216;  VY: 0.4932

Snapshot from simulator:

![Test One Visualization](https://github.com/dreamspring/P1_Extended-Kalman-Filter/blob/master/pic_dataset2.png "Test One Visualization")









