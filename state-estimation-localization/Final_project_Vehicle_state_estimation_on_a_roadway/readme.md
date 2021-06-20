# Vehicle State Estimation on a Roadway

In this project, I implemented the Error-State Extended Kalman Filter (ES-EKF) to localize a vehicle using data from the CARLA simulator. The project has the following parts.

## Implementation of the ES-EKF

In this part, I wrote code to perform the filter prediction step and the correction step. The filter relies on IMU data to propagate the state forward in time, and GPS and LIDAR position updates to correct the state estimate. The sensor data have been prepackaged for you - it is possible to visualize the output of the estimator and compare it to the ground truth vehicle position. The complete filter implementation will be tested by comparing the estimated vehicle position (produced by my code) with the ground truth position, for a 'hold out' portion of the trajectory (i.e., for which ground truth is not provided).

# Sensor miscalibration

In this part, I examined the effects of sensor miscalibration on the vehicle pose estimates. Originally, use of the incorrect transform between the LIDAR sensor frame and the IMU sensor frame will result in errors in the vehicle position estimates. After looking at the errors, the task is to determine how to adjust the filter parameters (noise variances) to attempt to compensate for these errors.

#  Effects of sensor dropout

In Part 3, I explored the effects of sensor dropout, that is, when all external positioning information (from GPS and LIDAR) is lost for a short period of time. The goal of Part 3 is to illustrate how the loss of external corrections results in drift in the vehicle position estimate, and also to aid in understanding how the uncertainty in the position estimate changes when sensor measurements are unavailable.