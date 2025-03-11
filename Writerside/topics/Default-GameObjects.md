# Default GameObjects

GameObjects are the fundamental objects in Unity that represent characters, props and scenery. They do not accomplish much in themselves but they act as containers for Components, which implement the real functionality.

A GameObject always has a Transform component attached to represent position and orientation (that it is not possible to remove). The other components that give the objects its functionality can be added from the editor's component in the Inspector view or from a script.

## GameObjects

We can add default GameObjects by three ways:

* Right click on Hierarchy
* Create button of Hierarchy
* GameObject menu of the top navbar

The default GameObjects are:

* **Create Empty**
* **3D Object**
    * Cube
    * Sphere
    * Capsule
    * Cylinder
    * Plane
    * Quad
    * Ragdoll
    * Terrain
    * Tree
    * Wind Zone
    * 3D Text
* **2D Object**
    * Sprite
    * Tilemap
    * Sprite Maks
* **Effects** (new)
    * Particle System
    * Trail
    * Line
* **Light**
    * Directional Light
    * Point of Light
    * Spothlight
    * Area Light
    * Reflection Probe
    * Light Probe Group
* **Audio**
    * Audio Source
    * Audio Reverb Zone
* **UI**
    * Text
    * Image
    * Raw
    * Button
    * Toogle
    * Slider
    * Scrollbar
    * Dropdown
    * Input Field
    * Canvas
    * Panel
    * Scroll View
    * Event System
* **Particle System** (Obsolete)
* **Camera**

## Scripts

Scripting is an essential ingredient in all games. Even the simplest game needs scripts to respond to input from the player and arrange for events in the gameplay.

Beyond that, scripts can be used to create graphical effects, control the physical behaviour of objects or even implement a custom AI system.

We can add scripts by three ways:

* Right click on Project view → Create
* Create button of Project view
* Asset menu of the top navbar → Create

The default scripts are:

* **C# Script**
* **Javascript** (Obsolete)
* **Editor Test C# Script** (Obsolete), allows to write automatic testing for the game
* **Shader**, program that run on the GPU instead of the CPU
    * Standard Surface Shader
    * Unlit Shader
    * Image Effect Shader
    * Compute Shader, can run anything, like physic calculations on the GPU
* **Testing** (new)
    * EditMode Test C# Script
    * PlayMode Test C# Script
* **Playable** (new)
    * Playable Behavior C# Script
    * Playable Asset C# Script