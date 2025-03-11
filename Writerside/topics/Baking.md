# Baking

Baked lights are light components which have their Mode property set to Baked.

This mode is used for local ambience, rather than fully featured lights. Unity pre-calculates the illumination from these lights before runtime, and does not include them in any runtime lighting calculations. This means that there is no runtime overhead for baked lights.

Unity bakes direct and indirect lighting from baked lights into Light Maps (to illuminate static GameObjects) and Light Probes (to illuminate dynamic GameObjects).

Baked lights cannot emit specular lighting, do not change in response to actions or events. They are mainly useful for increasing brightness in dark areas without needing to adjust all of the lighting within a Scene.

## Light Map

There are two Directional Modes for Light Maps: Directional and Non-directional.

To set the Directional Mode for a Light Map, open the Lighting view (Window > Lighting > Settings), click Scene, navigate to Lightmapping Settings, ensure the Lightmapper is set to Enlighten, and use the Directional Mode dropdown menu.

Directional Light Maps store more information about the lighting environment that Non-directional Light Maps. Shaders can use that extra data about incoming light to better calculate outgoing light, which is how materials appear on the screen.

**Non-directional**, uses just a single Light Map, storing information about how much light does the surface emit, assuming it's purely diffuse. Objects lit this way will appear flat and diffuse.  
**Directional**, adds a secondary Light Map, which stores the incoming dominant light direction and a factor proportional to how much light in the first Light Map is the result of light coming in along the dominant direction. The rest is then assumed to come uniformly from the entire hemisphere.

## Light Probes

Light Probes provide a way to capture and use information about light that is passing through the empty space in your scene.

Similar to Light Maps, light probes store "baked" information about lighting in the scene. The difference is that while Light Maps store lighting information about light hitting the surfaces, light probes store information about light passing through empty space.