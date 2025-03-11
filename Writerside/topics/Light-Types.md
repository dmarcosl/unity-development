# Light Types

## Point lights

![](image44.png)

A point of light is located at a point is space and sends light out in all directions equally. The direction of light hitting a surface is the line from the point of contact back to the center of the light object. The intensity diminishes with distance from the light, reaching zero at a specified range.

* The light emits similarly to a light bulb or candle.
* Rotating it won’t change how it hits objects.
* Easily drowned out by the directional light with default setting.
* They are useful for simulating lamps and local sources of light in a scene.

![](image66.png)

## Spot lights

![](image32.png)

Like point of light, a spot light has a specified location and range over which the light falls off, but is constrained to an angle, resulting in a cone-shaped region of illumination. Light also diminishes at the edges of the spot light cone.

They are generally used for artificial light sources, such as flashlights.

![](image13.png)

## Directional lights

![](image54.png)

A directional light does not have any identifiable source position and so the light object can be placed anywhere. All objects in the scene are illuminated as if the light is always from the same direction. The distance of the light from the target object is not defined and so the light does not diminish.

Directional lights are very useful for creating effects such as sunlight.

![](image4.png)

## Area lights

![](image53.png)

An area light is defined by a rectangle in space. Light is emitted in all directions uniformly across their surface area, but only from one side of the rectangle. Are lights are not available at runtime and can only be backed into lightmaps.

Area lights are used to create a realistic street light or a bank of lights close to the player.

![](image62.jpg)

## Emissive materials

Like area lights, emissive materials emit light across their surface area. They contribute to bounced light in the scene and associated properties such as color and intensity can be changed during gameplay. Whilst area lights are not supported in realtime, similar effect is possible using emissive materials.

Only affect static geometry in the scene. For dynamic, such as characters, light probes must be used.

![](image16.png)

## Ambient light

Ambient light is light that is present all around the scene and doesn't come from any specific source object.

Can be useful in a number of cases, depending on the art style, for example for cartoon-style rendering where dark shadows may be undesirable.

## Reflection Probe

![](image15.png)

Reflection Probe is rather like a camera that captures a spherical view of its surroundings in all directions.

The captured image is then stored as a Cubemap that can be used by objects with reflective materials.

![](image24.png)

## Light Probe Group

![](image11.png)

A Light Probe Group adds one or more light probes to a scene.