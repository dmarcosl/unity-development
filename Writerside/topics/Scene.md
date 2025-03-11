# Scene

## Scene Gizmo

![](image38.png)

The Scene Gizmo is in the upper-right corner. It displays the Scene View camera's current orientation, and allows to quickly modify the viewing angle and projection mode.

It has an arm on each side of the cube, labeled X, Y and Z. At click on any of them, the view is snapched to the axis that it represents. By right clicking, a list with all viewing angles are shown. To return to the default viewing angle, right click and select Free.

You can also change the projection mode between Perspective and Orthographic (Isometric) in the menu showed by right clicking.

The Scene Gizmo is only shown in the 3D Mode.

## Moving, Orbiting and Zooming

Moving, orbiting and zooming are key operations in the Scene view. Unity provides several ways to perform them:

### Arrow Movement

You can use the Arrow Keys of the keyboard to move around. Hold the Shift key to move faster.

### Hand Tool

When the Hand Tool is selected, you can:

* **Move**: click and drag
* **Orbit**: alt + click and drag (Only 3D Mode)
* **Zoom**: alt + right click and drag (or ctrl + click / two finger swipe on Mac)

Hold the Shift key to move faster.

### Flythrough Mode

Use Flythrough mode to navigate the Scene by flying around in first-person:

* Click and hold the right button
* Move the view around using the mouse and the WASD keys to move around
* Hold shift to move faster

It is designed to Perspective Mode, in Orthographic Mode orbits the Camera instead.

It’s not available in 2D mode.

## Centering the view on a GameObject

To center the Scene View on a GameObject, select the GameObject in the Hierarchy, then move the mouse over the Scene and press F. Also can be done by Edit > Frame Selected

To lock the view, press Shift + F. Also with Edit > Lock View to Selected