# Shadows

Unity's lights can cast Shadows from a GameObject onto other parts of itself or onto other nearby GameObjects. Shadows add a degree of depth and realism to a scene.

Light rays travel in straight lines from the light source, and may eventually hit GameObjects in the Scene. Once a ray has hit one, it can't travel any further to illuminate anything else. The shadows cast by the GameObject are simply the areas that are not illuminated because the light couldn't reach them.

Use the Shadow Type property in the Inspector to enable and define shadows for an individual light.

Hard Shadows produce shadows with a sharp edge, they are not particularly realistic compared to Soft Shadows but they involve less processing, and are acceptable for many purposes. Soft Shadows are also tend to reduce the "blocky" aliasing effect from the shadow map.

Each Mesh Renderer in the Scene has a Cast Shadow and Receive Shadows property.

The shadows for a given light are determined during the final Scene rendering. When the Scene is rendered to the main Camera view, each pixel position in the view is transformed into the coordinate system of the light. The distance of a pixel from the light is then compared to the corresponding pixel in the shadow map. If the pixel is more distant than the shadow map pixel, then it is presumably obscured from the light by another GameObject and it obtains no illumination.

A surface directly illuminated by a light sometimes appears to be partly in shadow. This is because pixels that should be exactly at the distance specified in the shadow map are sometimes calculated as being further away for using a low-resolution image or a shadow filtering.