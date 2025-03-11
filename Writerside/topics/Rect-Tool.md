# Rect Tool

The Rect Tool is located in the Transform Tools in the Toolbar view. It can be used to move, resize and rotate UI elements.

Once you have selected a UI element, you can move it by clicking anywhere inside the rectangle and dragging. You can resize it by clicking on the edges or corners and dragging. The element can be rotated by hovering the cursor slightly away from the corners until the mouse cursor looks like a rotation symbol. You can then click and drag in either direction to rotate.

Rect Tool uses the current pivot mode and space, set in the Toolbar.

## Rect Transform

The Rect Transform is a transform component that is used for all UI elements instead of the regular Transform component.

![](image59.png)

It has position, rotation and scale like the regular Transform, but it also has a width and height, used to specify the dimensions of the rectangle.

## Pivot

Rotations, size and scale modifications occur around the pivot so the position of the it affects the outcome.

When the Toolbar Pivot button is set to Pivot mode, the pivot of a Rect Transform can be moved in the Scene View.

## Anchors

Rect Transform include a layout concept called anchors. They are shown as four small triangular handles in the Scene view and anchor information is also shown in the Inspector.

![](image71.png)

If the parent of a Rect Transform is also a Rect Transform, the child Rect Transform can be anchored to the parent Rect Transform in various ways, like to the center of the parent or to one of the corners.

The anchoring also allows the child to stretch together with the width or height of the parent. Each corner of the rectangle has a fixed offset to its corresponding anchor. This way, the different corners of the rectangle can be anchored to different points in the parent rectangle.

The position value of the anchors can be found clicking the Anchors expansion arrow, under the Anchor Presets. The positions of the anchors are defined in fractions (percentages) of the parent rectangle width and height.

* 0.0 (0%) corresponds to the left or bottom
* 0.5 (50%) corresponds to the middle
* 1.0 (100%) corresponds to the right or top

But anchors are not limited to the sides and middle, they can be anchored to any point within the parent rectangle.

You can drag each of the anchors individually, or if they are together, you can drag the together by clicking in the middle in between them and dragging.

If you hold down Shift key while dragging an anchor, the corresponding corner of the rectangle will move together with the anchor.

## Anchor Presets

In the Inspector, the Anchor Preset button can be found in the left of the Rect Transform component. Clicking it brings up the Anchor Preset dropdown.

![](image48.png)

From here you can quickly select from some of the most common anchoring options.

The anchor Presets buttons displays the currently selected preset option if there is one.