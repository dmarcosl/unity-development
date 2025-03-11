# Layers

Layers are most commonly used by Cameras to render only a part of the scene, and by Lights to illuminate only parts of the scene. But they can also be used by raycasting to selectively ignore colliders or to create collisions.

A development use of the layers is the option to make them visible or invisible in the scene, by uncheck the layers that we don't want to watch in the Layers dropdown of the Toolbar tab.

To create layers, navigate to Edit menu of the top navbar → Project Settings → Tags and Layers, and expand the Layer list. We can have to 32 layers.

To assign a layer to a GameObject, select the GameObject, and in the GameObject properties of the Inspector view, expand the Layers dropdown and choose one.

A GameObject can only have one Layer assigned.

Using the camera's culling mask property, you can choose which layer's GameObjects will be rendered.