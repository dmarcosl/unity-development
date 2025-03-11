# Transitions

Animation transitions allow the State Machine to switch or blend from one animation state to another.

Transitions define not only how long the blend between states should take, but also under what conditions they should activate. You can set up a transition to occur only when certain conditions are true. To set up these conditions, specify values of parameters in the Animation Controller.

To set a transition select the origin State Machine > right click > Make Transition > select the target State Machine

The transition properties can be displayed by selecting a State Machine and selecting a Transition

![](image37.png)

* **Has Exit Time**, enables a special transition that doesn't rely on a parameter, instead, it relies on the normalized time of the state
* **Exit Time**, represents the exact time at which the transition can take effect. It is represented in normalized time. 0.75 means that at the 75% of the animation, the Exit Time condition is true. For looped animations 3.5 means the third and half loop
* **Fixed Duration**, if it checked, the transition time is interpreted in seconds, if not, the transition is interpreted as a fraction of the source state
* **Transition Duration**, duration of the transition, in normalized time/percentage
* **Transition Offset**, offset of the time to begin playing in the destination state which is transitioned to.
* **Interruption Source**, controls the circumstances under which this transition may be interrupted
    * **None**
    * **Current State**
    * **Next State**
    * **Current State then Next State**
    * **Next State then Current State**
* **Ordered Interruption**, determines whether the current transition can be interrupted by other transitions independently of their order
* **Conditions**, parameters that must met before the transition is triggered