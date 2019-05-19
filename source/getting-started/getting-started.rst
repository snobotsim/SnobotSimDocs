Getting started
===============

Introduction
............

SnobotSim is a easy to use, customizable, and extendable extension of the WPILib simulation framework.
It was designed to require no changes to your robot code, and only minor changes to your build script.

The goal of the simulator is to provide you with a mechanism to visualize your robot components, and 
run, test, and debug your code. It supports rudimentary physics simulations, and simulations of third
party libraries like CTRE, REV Robotics, and NavX sensors. You can simulate joysticks, simulate your
auontomous code, and even create unit tests without the complex set up of tools like Mockito.

The simulator is not intended to be a 100% accurate real world simulation, so don't plan on tuning
your mechanisms or your path planning with it. If set up properly, it should get you pretty close,
but you should always be sure to test your code on your real hardware.

Quickstart Guide
................

Several tools have been developed to make the setup process as easy and painless as possible. The
initial setup is detailed further along in the documentation, but the process is essentially:

1. Install the VS Code extension
2. Run the setup progrom
3. Run the simulator
4. Customize your robot
