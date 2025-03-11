# Light

Light determine the shading of an object and the shadows it cast. As such, they are fundamental part of graphical rendering.

![](image23.png)

* **Type**, the current type of light
* **Range**, defines how far the light emitted from the center of the object travels (Point and Spot light)
* **Spot Angle**, defines the angle at the base of a spot light cone (Spot light)
* **Color**, uses the color picker to set the color of the emitted light
* **Mode**, specifies the Light Mode used to determinate if and how a light is "baked"
* **Intensity**, sets the brightness of the light. The default of Directional is 0.5, for Point, Spot and Area is 1
* **Indirect Multiplier**, use this value to vary the intensity of indirect light, that is the light bounced from one object to another.
* **Shadow Type**, determines whether this light casts hard shadows, soft shadows or no shadows at all
    * **Baked Shadow Angle**, if light is Directional, mode is Baked and shadow is Soft Shadows, this property adds some artificial softening to the edges of shadows
    * **Baked Shadow Radius**, if light is Point or Spot, mode is Baked and shadow is Hard or Soft Shadows, this property adds some artificial softening to the edges of shadows
    * **Realtime Shadows**, if mode is Realtime and shadow is Hard or Soft Shadows, this properties allows to control realtime shadow rendering
        * **Strength**, controls how dark the shadows cast by light are, 1 to 0, default 1
        * **Resolution**, controls the rendered resolution of shadow maps, a higher value more impact to the GPU
        * **Bias**, controls the distance at which shadows are pushed away from the light, 2 to 0, default 0.05
        * **Normal Bias**, controls the distance at which the shadow casting surfaces are shrunk along the surface normal, 3 to 0, default 0.4
        * **Near Plane**, controls the value for the near clip plane when rendering shadows, 10 to 0.1, default 0.2
* **Cookie**, specifies a texture mask through which shadows are cast
* **Draw Halo**, draws a spherical Halo of light with a diameter equal to the range value
* **Flare**, you can set a Flare to be rendered at the light position by placing an Asset in this field to be used as its source
* **Render Mode**, sets the rendering priority of the selected light. Can affect lighting fidelity and performance
    * **Auto**, the rendering method is determined at runtime, depending on the brightness of nearby lights and the current Quality Settings
    * **Important**, the light is always rendered at per-pixel quality, this is used only for the most noticeable visual effects
    * **Not Important**, the light is always rendered in a faster vertex/object light mode
* **Culling Mask**, selectively exclude groups of objects from being affected by the light

Different types of light emit their assigned color in different ways.