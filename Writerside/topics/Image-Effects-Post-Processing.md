# Image Effects / Post-Processing

Image Effects handle all Render Texture-based full-screen image post-processing effects. They add a lot to the look and feel of the game without the needing to spend too much time on artwork.

The Unity Editor ships with many Image Effects in the Standard Assets Effect package, but you can also write your own effects.

You can use the effects to simulate physical camera and film properties, for example:

* **Bloom**, is the optical effect where light from a bright source appears to leak into surrounding objects.
* **Depth of Field**, is a common post-processing effect that simulates the properties of a camera lens, focusing sharply on an object at a specific distance, and objects nearer or farther from the camera will be out of focus.
* **Tone Mapping**, is the process of mapping color values from HDR (High Dynamic Range) to LDR (Low Dynamic Range), this means for most platform that arbitrary 16-bit floating point color values will be mapped to traditional 8-bit values.
* **Color Correction**
    * **Curves**, make color adjustment using curves for each color channel.
    * **Ramp Texture**, allows you apply arbitrary color correction from PhotoShop or GIMP.
    * **Lookup Texture**, instead of tweaking the color channels as in Curves, in  this effect only a single texture is used to produce corrected image.
* **Motion blur**, enhances fast-moving Scenes by leaving "motion trails" of previously rendered frames.
* **Tilt Shift**, is a local blur effect that blurs the image based on distance to the center
* **Vignette**, introduces darkening, blur and chromatic aberration at the edges and corners of the image.
* **Chromatic Aberration**, is an effect resulting from a camera's lens failing to converge all colors to the same point. It appears as "fringes" of color along boundaries that separate dark and bright parts of the image.
* **Noise and Grain**, simulates noise and film grain which is a typical effect happening in film or photography
* **Crease Shading**, enhances the visibility of objects by adding outlines of variable thickness.