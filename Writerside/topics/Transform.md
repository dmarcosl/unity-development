# Transform

Every object in a scene has a Transform. It's used to store and manipulate the position, rotation and scale of the object.

Every Transform can have a parent, which allows you to apply position, rotation and scale hierarchically. This is the hierarchy seen in the Hierarchy view.

The transform values of a child are relative to the parent. They don't change its position in the space, that is done by the parent transform values, but the relative position of it parent.

**Position**: Position of the Transform in X, Y and Z coordinates  
**Rotation**: Rotation of the Transform around the X, Y and Z axes, measured in degrees  
**Scale**: Scale of the Transform along X, Y and Z axes. Value 1 is the original size.