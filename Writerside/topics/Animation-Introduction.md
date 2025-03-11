# Animation Introduction

Unity has a rich and sophisticated animation system (referred as **'Mecanim'**), which provides:

* Easy workflow and setup of animations for all elements of Unity
* Support for imported animation clips and animations created within Unity
* Humanoid animation retargeting, the ability to apply animations from one character model onto another
* Simplified workflow for aligning animation clips
* Convenient preview of animations clips, transitions and interactions between them.
* Management of complex interactions between animations with a visual programming tool
* Animation different body parts with different logic
* Layering and masking features

Mecanim is based on the concept of Animation Clips, which contain information about how certain objects should change their position, rotation, or other properties over time. The Animation Clips come from external sources like Max, Maya, motion capture studios or other sources.

Animation Clips are then organised into a structured flowchart-like system called Animator Controller. It acts as a State Machine, which keeps track of which clip should currently be playing and when the animations should change or blend together.

Mecanim also has numerous special features for handling humanoid characters, like the ability to retarget humanoid animation from any source to your own character model, as well as adjusting muscle definitions.

These special features are enabled by Unity Avatar system, where humanoid characters are mapped to a common internal formal.

Each one of these pieces (Animation Clips, Animator Controller and Avatar) are brought together on a GameObject via the Animator Component.

This component has a reference to an Animator Controller and, if required, the Avatar. The Animator Controller contains the references to the Animation Clips it uses.

![](image67.png)

1. The Animation Clips that are imported from an external source
2. The Animation Clips are placed and arranged in an Animator Controller
3. The rigged character model has a specific configuration of bones which are mapped to an Avatar format
4. When managing the character model, it has an Animator component attached, where you can see its properties

The parameters are

* **Controller**, Animator Controller attached
* **Avatar**, Avatar attached
* **Apply Root Motion**, if enable moves the transform to match the root of the animation
* **Update Mode**, controls when and how often the Animator is updated
    * **Normal**, is updated in sync with the Update call
    * **Animate Physics**, is update in sync with the FixedUpdate call
    * **Unscaled Time**, is updated in sync with the Update call, but the animator speed ignores the current timescale and animates at 100% speed
* **Culling Mode**, controls what is updated when the object has been culled
    * **Always Animate**, don't do culling even when offscreen
    * **Cull Update Transforms**, retarget, IK and write of Transforms are disabled when renderers are not visible
    * **Cull Completely**, animation is completely disabled when renderers are not visible