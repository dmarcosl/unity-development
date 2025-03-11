# Slider

The Slider allows the user to select a numeric value from a predetermined range by dragging the mouse.

The Slider is created with several childs that it will need in its functionality, those are the **Background image**, **Fill image** and **Handle image**

The Slider share some properties with the Button.

![](image20.png)

* **Transition**, same as Button, only affect the Handle
* **Fill Rect**, the graphic used for the fill area of the control (Fill child)
* **Handle Rect**, the graphic used for the sliding "handle" part of the control (Handle child)
* **Direction**, direction in which the slider's value will increase when the handle is dragged
* **Min Value**, the value of the extreme lower end
* **Max Value**, the value of the extreme higher end
* **Whole Numbers**, check if the slider be constrained to integer values
* **Value**, initial value
* **On Value Changed()**, a UnityEvent that is invoked when the current value of the Slider has changed. You can attach a GameObject and select a value of a component, generally from a Script

The Fill change the size by keeping a reference to the Handle's Rect Transform.