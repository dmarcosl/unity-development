# Emitters

## **Particle System**

A Particle System component simulates fluid entities such as liquids, clouds and flames y generating and animating large number of small 2D images in the scene.

The Particle System has many properties, for convenience, the Inspector organises them in collapses modules.

![](image46.png)

* **Emission**, controls the rate at which particles are emitted as well as blur emissions
* **Shape**, defines the shape from which particles can be emitted and the direction of the start velocity. Sphere, Hemisphere, Cone, Box, Mesh, Mesh Renderer, Skinned Mesh Renderer, Circle and Edge.
* **Velocity over Lifetime**, allows to control the velocity of particles over their lifetime
* **Limit Velocity over Lifetime**, controls how the speed of particles is reduced over their lifetime
* **Inherit Velocity**, controls how the speed of particles reacts to movement of their parent object over time
* **Force over Lifetime**, controls the acceleration of particles by forces (such as wind)
* **Color over Lifetime**, specifies how a particle's color and transparency changes over its lifetime
* **Color by Speed**, controls the color of the particle according to its speed in distance units per second
* **Size over Lifetime**, specifies how a particle's size changes over its lifetime
* **Size by Speed**, controls the size of the particle according to its speed in distance units per second
* **Rotation over Lifetime**, changes the rotation of the particles as they move
* **Rotation by Speed**, changes the rotation of a particle according to its speed in distance units per second
* **External Forces**, modifies the effect of wind zones on particles
* **Collision**, controls how particles collide with GameObjects in the Scene
* **Sub Emitters**, allows to set up additional particle emitters that are created at a particle's position at certain stages of its lifetime
* **Texture Sheet Animation**, lets you treat the Texture as a grid of separate sub-images that can be played back as frames of animation
* **Renderer**, determines how a particle's image or Mesh is transformed, shaded and overdrawn by other particles

To give the appearance that the Particle System was playing prior to runtime, it must have the properties Play on Awake and Prewarm.