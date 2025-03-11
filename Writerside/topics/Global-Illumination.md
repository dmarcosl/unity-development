# Global Illumination

Global Illumination is a system that model how light is bounced off of surfaces onto other surfaces (indirect light) rather than being limited to just the light that hits a surface directly from a light source (direct light).

Traditionally, videogames and other realtime graphics have been limited to direct lightning because of the calculations for indirect lighting were too slow that could only be used in non-realtime.

A way for games to work around this limitation is to calculate indirect light only for static objects and surfaces. That way the slow computation can be done ahead of time, but since the objects don't move, the indirect light that is pre-calculated this way will still be correct at runtime. This is Baked GI, also known as Baked Light Maps.

Baked GI and Precomputed Realtime GI have the limitation that only static objects can be included in the bake/precomputation, so moving objects cannot bounce light onto other objects. However they can still pick up bounce light from Light Probec

## Global Illumination UVs

There are two sets of GI Light Maps: baked and realtime. How you define which set to use depends on whether you are working with environment lightning or specific lights.

**Baked Light Maps**, are mainly useful for lights which do not change at all during runtime, and are therefore stored as static rendering in the Light Map.  
**Realtime Light Maps**, are mainly useful for lights that are animated during runtime, and therefore need to be rendered in real time.  
**Mixed Light Maps**, baked Light Maps and also gives direct realtime lightning to non-static objects.

[https://docs.unity3d.com/540/Documentation/Manual/GlobalIllumination.html](https://docs.unity3d.com/540/Documentation/Manual/GlobalIllumination.html)