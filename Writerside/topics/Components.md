# Components

Components are the nuts and bolts of objects and behaviors in a game. They are the functional pieces of every GameObject.

A GameObject is a container for many different Components.

You can add Components to the selected GameObject through the Component menu of the top navbar or by the filter at the bottom of the Inspector view.

The Components are divided into groups, the most used are:

* **Mesh**, renders the object
    * **Mesh Filter**, take a mesh from the assets and passes it to the Mesh Renderer
    * **Mesh Renderer**, takes the geometry from the Mesh Filter and renders it
    * **Skinned Mesh Renderer**, render bone animations
* **Effect**, visual effects applied to cameras, GameObjects, light sources, etc.
    * **Particle System**, simulates fluid entities, such liquids, clouds and flames, by generating and animating large number of small 2D images in the Scene
    * **Line Renderer**, takes an array of two or more points in 3D space, and draws a straight line between each one
    * **Trail Renderer**, is used to make trails behind GameObjects in the Scene as they move
* **Physics**
    * **Rigidbody**, enables physical behaviour for a GameOBject
    * **Colliders**, define the shape of an object to allow physical collisions
    * **Joints**, way to attach one rigidbody of an object to another or to a point in space
    * **Character Controllers**, gives the character a simple, capsule-shaped collider that is always upright
* **Audio**
    * **Audio Listener**, hears audio
    * **Audio Source**, plays a audio clip
    * **Audio Reverb Zone**, create reverb sound in an area, like echo in a cave
* **Rendering**
    * **Camera**, capture and display the world to the player
    * **Light**, bright the object
    * **Canvas Renderer**, represents the abstract space in which the UI is laid out and rendered
* **UI**, needs the Canvas Renderer component
    * **Text**, shows text
    * **Button**, interactive part of the UI
    * **Image**, shows a sprite
* **Script**, define components