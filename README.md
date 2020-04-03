# BackyardFlyer
In this project we must use event driven programming in order to fly autonomously a drone. All the action will happen in a Unity simulator, flying a quadcopter.

### Drone API
To link with the drone, we will be using the [Udacidrone API](https://udacity.github.io/udacidrone/). It's providing a way to communicate with the quadcopter. The API is basically designed in two parts: a Drone class and a set of connection classes. The goal of this project is to design a subclass from the Drone class implementing a state machine to autonomously fly a box.
### Phases of Flight
The quadcopter will have six phases of flight:
1. Manual Phase: In this phase the quadcopter it's not being controlled by the Flight Controller and just sitting on the ground.
This phase ends when the arming phase begins.

2. Arming Phase: In this phase the flight computer takes control the drone, and gets the rotors spinning.
This phase ends when the rotors are up to speed and the takeoff can begin.

3. Takeoff Phase: In this phase involves the drone going straight up and continuing straight up until it's reached it's target height.
This phase ends when the waypoint pahse begins (it's possible to jump this phase if it's nowhere to go and jump straight to landing phase)

4. Waypoint Phase: In this phase the drone it's flying to the designated point.
This phase ends when there are no more waypoint's and the landing phase is initializing.

5. Landing Phase: In this phase is just the drone descends back to ground level and it continues descending until it gets sufficiently close to ground. And once that happens, the disarming phase begins.

6. Disarming Phase: In this phase is just where the computer control is disabled and the motors are disarmed.

### And here is the final result 
![](backyard_flyer.gif)
