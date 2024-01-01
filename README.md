git# MobileRobot-Openloopcontrol
## Aim:

To develop a python control code to move the mobilerobot along the predefined path.

## Equipments Required:
1. RoboMaster EP core
2. Python 3.7

## Procedure

Step1:

robomaster is a built-in module in python in which robots are imported and import time.

Step2:

initialize the robot by giving an initialize function for the robots to get commands from the user and move.

Step3:

Give a value to the x axis so the robot moves in forward direction and for the robot to move towards left or right give a ceertain value to y.

Step4:

the value assigned to the z variable indicates the speed of the robot.

Step5:

set_led determines the colour of the LED lights on each side of the robot with certain values of red,green,blue to get the colour.

step6 :
 
 Give a distance,speed,coloue change for specified path and at the end give close to end the function.

 step7 :

  End the program.

## Program
```python
from robomaster import robot
import time
from robomaster import camera

if _name_ == '_main_':
    ep_robot = robot.Robot()
    ep_robot.initialize(conn_type="ap")

    ep_chassis = ep_robot.chassis
    ep_led = ep_robot.led
    ep_camera = ep_robot.camera

    print("Video streaming started.....")
    ep_camera.start_video_stream(display=True, resolution = camera.STREAM_360P)

    ep_chassis.move(x=2.5, y=0, z=0, xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=0,b=0,effect="on")

    ep_chassis.move(x=0.4, y=0, z=75, xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=255,b=0,effect="on")

    ep_chassis.move(x=1, y=0, z=0, xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=192,g=192,b=192,effect="on")

    ep_chassis.move(x=0, y=0, z=90, xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=235,g=153,b=153,effect="on")

    ep_chassis.move(x=1.6, y=0, z=0, xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=255,b=204,effect="on")

    ep_chassis.move(x=0, y=0, z=-30, xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=128,b=128,effect="on")

    ep_chassis.move(x=1.2, y=0, z=0, xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=102,b=0,effect="on")

    ep_chassis.move(x=0, y=0, z=45, xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=102,b=0,effect="on")
    
    ep_chassis.move(x=1.6, y=0, z=0, xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=153,b=204,effect="on")
    
    ep_chassis.move(x=0, y=0, z=95 ).wait_for_completed()
    ep_led.set_led(comp = "all",r=204,g=255,b=255,effect="on")

    ep_chassis.move(x=2.1, y=0, z=0,xy_speed=1.3 ).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=102,b=0,effect="on")

    ep_chassis.move(x=0, y=0, z=85 ).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=0,b=255,effect="on")

    ep_chassis.move(x=0.4, y=0, z=0, xy_speed=1.3 ).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=255,b=255,effect="on")

    time.sleep(4)
    ep_camera.stop_video_stream()
    print("Stopped video streaming.....")
    ep_robot.close()
```

## MobileRobot Movement Image:

![Screenshot 2024-01-01 124456](https://github.com/jyesvanthe/mobilerobot-openloopcontrol/assets/150319392/0d6f4bb9-ba5c-4f19-b455-e2f310340f72)





## MobileRobot Movement Video:

Upload your video in Youtube and paste your video-id here

 https://youtube.com/shorts/DN7oSsqC-tU?feature=shared
 
Saveetha Engineering College
```
