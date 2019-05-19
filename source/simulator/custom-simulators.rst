Custom Simulators
=================

There are several times when you might want to add a custom simulator to your robot, such as 

- Simulating limit switches being triggered when your elevator encoder reaches a certain height
- Simulate non-supported SPI/I2C devices like a PixyCam or Dotstar LED strips
- Simulate your camera ICD to fake data based on your robot position (i.e. faking the Limelight NetworkTable or the NetworkTable/socket messages coming from a co-processor)
- Simulating delayed sensor responses (i.e. When I press my "intake ball" button, it takes .25 seconds before my sensor gets tripped)

Examples
........

Some of these are outdataed and are using the old SnobotSim API, but the logic behind them should still hold

Camera Simulators
~~~~~~~~~~~~~~~~~
* `STEAMworks UDP Camera Simulator <https://github.com/ArcticWarriors/snobot-2017/blob/master/Simulator/2017Simulator/src/com/snobot/simulator/robot_sim/snobot2017/CameraSimulator.java>`_
* `DeepSpace Limelight Simulator <https://gitlab.com/XCats/Software/software-2019/blob/dev/DeepSpace2019/src/xcats_simulator_ext/java/org/xcats/frc/deep_space/CameraSimulator.java>`_

Sensor Feedback Simulators
~~~~~~~~~~~~~~~~~~~~~~~~~~
* `Potentiometer Simulator <https://github.com/ArcticWarriors/snobot-2015/blob/master/Simulator/SimulatorMain/src/com/snobot/StackerPotSim.java>`_
* `NavX Pitch Simulator <https://gitlab.com/XCats/Software/software-2019/blob/dev/DeepSpace2019/src/xcats_simulator_ext/java/org/xcats/frc/deep_space/ClimberSimulator.java>`_

SPI/I2C
~~~~~~~
* `Dotstar LED simulator <https://github.com/ArcticWarriors/snobot-2018/blob/master/RobotCode/snobot2018/simulator_extensions/org/snobot/simulator2018/DotstarSimulator.java>`_