# Animation Controller Asset

When you have an animation clip ready to use, you need to use an Animator Controller to bring them together.

The Animator Controller asset is created within Unity and allows you to maintain a set of animations for a character or object.

![](image34.png)

Animator Controller assets are created from the Assets menu.

In most situations it is normal to have multiple animations and switch between them when certain game conditions occur.

The controller manages the various animation states and the transitions between them using a so-called State Machine, which could be thought of as a kind of flowchart, or simple program written in visual programming language within Unity.

![](image45.png)

The Animator Controller is applied to an object by attaching an Animator component that references them.

## Animation Layers

Animations Layers are for managing complex state machines for different body parts.

![](image69.png)

On each layer, you can specify the mask (part of the animation model) and the Blending type.

Override means information from other layers will be ignored, while Additive means that the animation will be added on top of previous layers.

## Animation Parameters

Animation Parameters are variables that are defined within an Animator Controller that can be accessed and assigned values from scripts.

Default parameter values can be setup using the Parameters section of the Animator

![](image18.png)

The data types are

* Int
* Float
* Bool
* Trigger

## State Machines

The basic idea is that a character is engaged in some particular kind of action at any given time.

The actions available will depend on the type of gameplay, but typical actions include things like idling, walking, running, jumping, etc. These actions are referred to as states.

The character will have restriction on the next state it can go to rather that being able to switch immediately from any state to any other.

The options for the next state that a character can enter from its current state are referred to as State Transitions.

Taken together, the set of states, the set of transitions and the variable to remember the current state, form a State Machine.

![](image58.png)

The importance of State Machines for animation is that they can be designed and updated quite easily with relatively little coding.