# FlatSat
This repository is the master repo for all data related to the FlatSat project.

#Introduction
The project began as a simpler form of a 3-axis gimble. The goal of the gimble was to test various apparatus that would be installed in our 3U-Cubesat. In order to get the various subsystems (ADCS, EPS, OBC, TTC, STS) associated with the main project familiar with the process, FlatSat was born.

A one-axis stabilization design was settled upon, which would use a pyramidal configuration of reaction wheels. Although we would only be working with the angular velocity about a fixed axis, the BNO055 IMU sensor was selected to obtain attitude readings. From there, the readings would be pushed to the Arduino Uno, which would run an Extended Kalman Filter(EKF) on the quaternion inputs. Using the stable output of the EKF, we would run PID control on the reaction wheel system to stop the entire system.

Three goals will ideally be achieved. Stopping the system in the least amount of time, stopping the system using the least amount of energy, and stopping the system using reaction wheels only in one axis. The documentation goes into more depth on each of the components used and the process and mathematics followed.
