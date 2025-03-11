# Sprite Editor

Sometimes a sprite texture contains just a single graphic element, but it is often more convenient to combine several related graphics together into a single image. Unity makes it easy to extract elements from a composite image by providing a Sprite Editor.

To open the Sprite Editor

* Select the image you want to edit from the Project view
* In the Inspector view, make sure that the image have the Texture type "Sprite (2D and UI)" and the Sprite Mode "Multiple"
* Then click on the Sprite Editor button

## Manual Slicing

The most direct way to use the editor is to identify the elements manually. You can drag the handles or the edges of the rectangle to resize it around a specific element.

The controls in the panel let you choose a name for the sprite graphic and set the position and size of the rectangle by coordinates.

The Trim button will resize the rectangle so that it fits tightly around the edge of the graphic based on transparency.

## Automatic Slicing

Unity can save you work by detecting the graphic elements and extracting them automatically.

If you click on the Slice menu, you will see the Slice panel.

![](image3.png)

With the slicing type set to **Automatic**, the editor will attempt to guess the boundaries of sprite elements by transparency.

There are three methods:

* **Delete existing**, will replace whatever is already selected
* **Smart**, will attempt to create new rectangles while retaining or adjusting existing ones
* **Safe**, will add new rectangles without changing anything

**Grid by Cell Size** or **Grid by Cell Count** options are also available for the slicing type. This is very useful when the sprites have already been laid out in a regular pattern during creation.

To finish the slice or exit without save the changes, just push the Revert or Apply button in the top bar of the Editor.

After slicing a sprite, we can expand the asset in the Project view to watch the slice sprites, selecting them we can edit the name and the rectangle.