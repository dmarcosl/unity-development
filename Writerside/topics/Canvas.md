# Canvas

The Canvas is the area that all UI elements should be inside. It is a GameObject with a Canvas component on it, and all UI elements must be children of such a Canvas.

Creating a new UI element automatically creates a Canvas, if there isn't already a Canvas in the scene, and the UI element is created as a child to this Canvas.

The Canvas area is shown as a rectangle in the Scene view, this makes it easy to position UI elements without needing to have the Game view visible.

## Draw Order

UI elements in the Canvas are drawn in the same order they appear in the Hierarchy.

To change which element appear on top of other elements, simply reorder the elements in the Hierarchy.

The order also can be controlled from scripting by using ordering methods.

## Render Modes

The Canvas has a Render Mode setting which can be used to make it render in screen space or world space

### Screen Space - Overlay

This render mode places UI elements on the screen rendered on top of the scene. If the screen is resized or changes resolution, the Canvas will automatically change size to match this.

### Screen Space - Camera

Similar to Overlay, but in this mode the Canvas is placed a given distance in front of a specified Camera.

The UI elements are rendered by this camera, which means that the Camera settings affect the appearance of the UI. If the camera is set to Perspective, the UI elements will be rendered with perspective.

If the screen is resized, changes resolution or the camera frustum changes, the Canvas will automatically change size to match as well.

### World Space

In this mode, the Canvas will behave as any other object in the scene. The size of the Canvas can be set manually using its Rect Transform, and UI elements will render in front of or behind other objects in the scene based on 3D placement.

This is useful for UIs that are meant to be a part of the world. This is known as "diegetic interface".