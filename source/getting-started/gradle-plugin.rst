Gradle Plugin
===============

The SnobotSimPlugin is a gradle plugin designed to make the simulator easier to use. It
provides a easy to use mechanism to pull in all of the dependencies, and provide tasks
to start the simulator from the command line.

Manual Installation Notes
..........................
Note: You can use the installation tool outlined in :ref:`vs-code-extension` to avoid doing the manual installation

To add the plugin to your robot project, update the plugin block of your ``build.gradle`` file like so

.. code-block:: groovy
   :emphasize-lines: 4

   plugins {
      id "java"
      id "edu.wpi.first.GradleRIO" version "2020.1.2"
      id "com.snobot.simulator.plugin.SnobotSimulatorPlugin" version "2020-0.0.0" apply false
   }

Notice the ``apply false`` line maker. This means that we are not activating the plugin yet,
because we need more information from the rest of the build script first.

The recommend place to add the activiation is between your ``repositories`` block and your ``dependencies`` block, like so:

.. code-block:: groovy
   :emphasize-lines: 6-11

    // Maven central needed for JUnit
    repositories {
        mavenCentral()
    }
    
    //////////////////////////////////
    // SnobotSim
    //////////////////////////////////
    apply plugin: com.snobot.simulator.plugin.SnobotSimulatorPlugin
    apply from: "snobotsim/snobot_sim.gradle"
    //////////////////////////////////
    
    // Defining my dependencies. In this case, WPILib (+ friends), and vendor libraries.
    // Also defines JUnit 4.
    dependencies {
        compile wpi.deps.wpilib()
        compile wpi.deps.vendor.java()
        nativeZip wpi.deps.vendor.jni(wpi.platforms.roborio)
        nativeDesktopZip wpi.deps.vendor.jni(wpi.platforms.desktop)
        testCompile 'junit:junit:4.12'
    }

Running the simulator
.....................

The easiest way to run the simulator is from the command line. Open a command window 
in your root directory (the directory that has the main ``build.gradle`` script), and
run the following command, ``./gradlew runJavaSnobotSim`` and you should see the the
simulator GUI open on your computer

Notes:

* Windows users don't need to put the ``./`` in front of gradlew, only Linux users do
* C++ teams should use ``./gradlew runCppSnobotSim``. For more specific C++ notes and exceptions, see :ref:`cpp-guide`


Release Notes
...............


Current Release
^^^^^^^^^^^^^^^

`2020-0.0.0 <https://github.com/snobotsim/SnobotSimPlugin/releases/tag/2020-0.0.0>`_
####################################################################################

* 2020 Kickoff Release
* Includes a new task, `updateSnobotSimConfig`, which will download the latest SnobotSim config file



Previous Releases
^^^^^^^^^^^^^^^^^

`2019-2.0.0 <https://github.com/snobotsim/SnobotSimPlugin/releases/tag/2019-2.0.0>`_
####################################################################################

* Added ability to simulator REV SparkMax motor controllers

`2019-1.0.0 <https://github.com/snobotsim/SnobotSimPlugin/releases/tag/2019-1.0.0>`_
####################################################################################

* Updates to make the build script easier to set up and use

`2019-0.2.0 <https://github.com/snobotsim/SnobotSimPlugin/releases/tag/2019-0.2.0>`_
####################################################################################

* Updates required for the 2019.1.1 WPLib release

`2019-0.0.0 <https://github.com/snobotsim/SnobotSimPlugin/releases/tag/v2019-0.0.0>`_
#####################################################################################

* Initial beta release for the 2019 season