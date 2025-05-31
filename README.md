# MobileRobot-Openloopcontrol
## Aim:

To develop a python control code to move the mobilerobot along the predefined path.

## Equipments Required:
1. RoboMaster EP core
2. Python 3.7

## Procedure

Step1:

Use from robomaster import robot

Step2:

Choose the x,y,z - axis movement distance(meters).

Step3:

Give ep_chassis.move to move straight.

Step4:

Give time.sleep() for a break.

Step5:

Give ep_chassis.drive_speed to have a circular movement.

## Program
```python
from robomaster import robot
import time

if __name__ == '__main__':
    ep_robot = robot.Robot()
    ep_robot.initialize(conn_type="ap")

    ep_chassis = ep_robot.chassis
        ep_led = ep_robot.led
    ep_camera = ep_robot.camera

    print("Video streaming started.....")
    ep_camera.start_video_stream(display=True, resolution = camera.STREAM_360P)

    ep_chassis.move(x=2.55, y=0, z=0, xy_speed=0.9).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=0,b=0,effect="on")

    ep_chassis.move(x=0.4, y=0, z=80, xy_speed=0.8).wait_for_completed()
    ep_led.set_led(comp = "all",r=128,g=0,b=0,effect="on")

    ep_chassis.move(x=0.75, y=0, z=0, xy_speed=0.8).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=128,b=128,effect="on")

    ep_chassis.move(x=0.3, y=0, z=90, xy_speed=0.8).wait_for_completed()
    ep_led.set_led(comp = "all",r=225,g=0,b=0,effect="on")

    ep_chassis.move(x=1.5, y=0, z=0, xy_speed=0.8).wait_for_completed()
    ep_led.set_led(comp = "all",r=225,g=0,b=225,effect="on")

    ep_chassis.move(x=0, y=0, z=60, xy_speed=0.8).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=225,b=255,effect="on")

    ep_chassis.move(x=0, y=1.58, z=0, xy_speed=0.8).wait_for_completed()
    ep_led.set_led(comp = "all",r=128,g=0,b=0,effect="on")

    ep_chassis.move(x=0, y=0, z=48, xy_speed=0.8).wait_for_completed()
    ep_led.set_led(comp = "all",r=153,g=51,b=102,effect="on")

    ep_chassis.move(x=0, y=1.55, z=0, xy_speed=0.8).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=0,b=128,effect="on")

    ep_chassis.move(x=2.05, y=0, z=0, xy_speed=0.8).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=102,b=0,effect="on")
     
    ep_chassis.move(x=0, y=0, z=80, xy_speed=0.8).wait_for_completed()
    ep_led.set_led(comp = "all",r=153,g=51,b=0,effect="on")

    ep_chassis.move(x=0.65, y=0, z=0, xy_speed=0.8).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=0,b=0,effect="on")

    ep_chassis.move(x=0, y=0, z=360, xy_speed=0.8).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=0,b=255,effect="on")

    time.sleep(4)
    ep_camera.stop_video_stream()
    print("Stopped video streaming.....")



    
    ep_robot.close()


```
## MobileRobot Movement Image:
![image](https://github.com/user-attachments/assets/5828c7f4-58f3-44b5-b7af-b13accac9057)
## MobileRobot Movement video:

https://youtu.be/Mcwbm-W5Tyo?si=K4dsOz7QcBLan1z7



Mobile Robotics Laboratory
Department of Artificial Intelligence and Data Science/ Machine Learning
Saveetha Engineering College
```
