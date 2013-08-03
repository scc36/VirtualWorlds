Car Simulator
=============

This is the simulation platform for the self driving vehicle at https://github.com/derivatived/self-driving-car.

Overview
-------

The car simulator is built in the Unity3D Game Engine (Version 4.x), using pre-existing assets for the road and terrain. Currently, the simulator applies Artificial Intelligence to the car by sending and receiving information to a server. As such, the simulator is accompanied by a sample Artificial Intelligence server coded in Node.js.

Since default Unity projects maintain large amounts of metadata personalized to each user, the simulator utilizes an alternate form for source control (.metadata). This will require a more specific setup to manage the program through GitHub.

There is more information available on the GitHub Wiki.

Pre-requisites
--------------

* Unity3D -- Download and install the latest version of Unity 3d at (http://unity3d.com/)
* Node.js -- Node.js is ONLY needed to run the sample AI server. Download at (http://nodejs.org/)

Setup
-----

### Car Simulator

1.  Preset Unity3D to manage version control through meta files
2.  Create a New Project in Unity (needed to access Unity Settings)
3.  Select Edit -> Project Settings -> Editor to open an "Editor Settings" panel
4.  In "Version Control", change mode to "Meta Files"
5.  Save the project and Quit Unity3D so that the settings are applied
6.  Pull or download the Car Simulator into a new, desired folder
7.  Re-open Unity, then choose File -> Open Project...
8.  Select the folder Car Simulator was pulled to and open the project.
9.  The current scene used by the Simulator is "Complete Scene"
10. Start up an AI server (to run the demo server just run node SampleAI.js on the command line).
11. Select the Car GameObject in the hierarchy inside of Unity.
12. Edit the server and port to point towards your server(the example is on localhost:3000).

Note: it is currently not known if a opening a new/separate project first is required to properly change the version control setting, but better safe than sorry.

### Node.js AI server

1.  Download and install Node.js: http://nodejs.org/
2.  Open up the command prompt
3.  Navigate to the SampleAIServer folder
4.  Enter "node SimpleAI.js" to run the server
6.  Open the Car Simulator in Unity3D
7.  The Car model stores what port it will interact with
8.  To view this value, select the car model in the scene (Hierarchy -> Car)
9.  Near the bottom, under "Car AI Networked (script)", there is a "Port" setting (3000 in this case)
10. Run the program and the Car should move in accordance with the Node.js server