# PID Control

## Overview
This project implements a PID controller to drive a car within lanes in a Simulator.
The cross track error received from the simulator is sent to PID controller and it outputs the steering angle which in turn is sent to simulator to drive the car.

## Reflection

### Describe the effect each of the P, I, D components had in your implementation.

* The proportional part (P) helps the car to steer in correct direction.
ON using just this part, the output of PID controller will be proportional to CTE (just the current value).

* The Integral part(I) is used to counteract to bias in the system. If only this value is used and is high, car will move in circles.

* The Differentiation part (D) is used to reduce the oscillations and overshooting caused by Proportional part(P).

### Describe how the final hyper parameters were chosen.

The final hyper parameters were chosen manually by trial and error.
The proportional part is used to keep the car in center. A value of 0.2 is used so that it follows the track but it overshoots.
For integral part a negligible value was used as the simulator was not much biased. So, a value of 0.004 is used.
The Derivate part is high to dampen the oscillations and overshooting caused by P. Value used is 3.
