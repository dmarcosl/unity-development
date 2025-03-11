# States

Animation States are the basic building blocks of an State Machine.

Each state contains an individual animation sequence (blend tree) which will play while the character is in that state.

When an event triggers a state transition, the character will be left in a new state whose animation sequence will then take over.

![](image68.png)

* **Speed**, default speed of the animation
* **Motion**, animation clip assigned
* **Foot IK**, if should foot IK be respected for this state
* **Write Defaults**, if AnimatorStates writes back the default values for properties that are not animated by its Motion
* **Mirror**, if should the state be mirrored, it is only applicable to humanoid animations
* **Transitions**, list of transitions originating from this state

The default state, displayed in brown, is the state that the machine will be in when it is first activated. You can change it by rick click > Set As Default.

A new state can be added by right click on an empty space and selecting Create State > Empty, or by drag and drop an animation.

Any State is a special state which is always present. It exists for the situation where you want to go to a specific state regardless of which state you are currently in. It cannot be the end of a transition.