.. _vs-code-extension:

VS Code Extension
=================

Note: This tool is in development and may not function as expected

This is a VS Code Extension that allows you to easily add SnobotSim to your project, as well as
simplify the process for upgrading versions and running the simulator from your IDE. If you are
not a VS Code user but still want the setup tool, you can use the `standalone tool <#>`_ instead.

Installing the Extension
........................

The extension is not available on the marketplace yet, so you must install it using a VSIX package.
The releases of the extension are stored on the `projects Github page <https://github.com/snobotsim/SnobotSimExtension/releases>`_.

To install:

1. Open VS Code
2. Select and download the vscode-RE.LEA.SE.vsix bundle
3. In VS Code, press CTRL+SHIFT+P to open the command pallete, and type "Install From VSIX"
4. Select Extensions: Install from VSIX...
5. Navigate to where you downloaded the SnobotSim VSIX package, and select it

Using the Extension
...................

Once the extension has been installed, there should now be some SnobotSim commands available.

To set up your project for the first time, you can right click your ``build.gradle`` file, and 
select "Setup Snobot Sim". This will open the window that will allow you to customize your installation
