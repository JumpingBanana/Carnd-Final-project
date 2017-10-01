# Project Team

  * Reinhard Steffens steffens21@gmail.com
  * Yury Melnikov Yury.Melnikov@gmail.com
  * Naoto Yoshida yossy0157@gmail.com
  * Tawit Uthaicharoenpong iamtawit@gmail.com
  * Olli Vertanen overtane@gmail.com

## Notes on our Implementation

### Traffic Light detection

### Waypoint Updater
After we have got traffic light detection working we then cooperate traffic light position and its status to adjust our vehicle speed.

Speed of the vehicle will get adjust from original waypoint velocity (20 MPH) when the light is closer than 50 meter ahead of the car and status of traffic light is either Red or Yellow. Once these condition are met, vehicle will adapt its speed down to complete stop at the light using following equation.

![first equation](http://latex.codecogs.com/gif.latex?adjusted%5C_velocity%20%3D%20%7Bnext%5C_waypoint%5C_velocity%7D%20-%20%7B%5Cfrac%7Bnext%5C_waypoint%5C_%20velocity%7D%7Bdistant%5C_to%5C_traffic%5C%2C%20light%20-%20next%5C_waypoint%5C_position%7D%7D)

![alt text][logo]

[logo]: https://github.com/JumpingBanana/Carnd-Final-project/blob/master/velocity_adjustment "velocity_adjustment"

This adjusted velocity will then update a velocity of subsequence waypoint. 

### Twist Cotroller


