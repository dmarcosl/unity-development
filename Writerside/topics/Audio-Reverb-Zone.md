# Audio Reverb Zone

Reverb Zones take an Audio Clip and distorts it depending where the audio listener is located inside the reverb Zone.

![](image6.png)

They are used when you want to gradually change from a point where there is no ambient effect to a place where there is one, for example a cavern.

When a listener is inside two reverb zones with the same preset only one is applied.

![](image1.png)

* **Min Distance**, the radius of the inner circle in the gizmo
* **Max Distance**, the radius of the outer circle in the gizmo
* **Reverb Preset**, determines the reverb effect that will be used by the reverb zone
    * Off
    * Generic
    * User (editable)
    * Room
    * Bathroom
    * Cave
    * Hangar
    * ...