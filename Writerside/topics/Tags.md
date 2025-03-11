# Tags

A Tag is a reference word which you can assign to one or more GameObjects and helps to identify them for scripting purposes.

They ensure you don't need to manually add GameObjects to script's exposed properties using drag and drop, thereby saving time when you are using the same script code in multiple GameObjects.

To create tags, navigate to Edit menu of the top navbar → Project Settings → Tags and Layers, and expand the Tag list.

To assign a tag to a GameObject, select the GameObject, and in the GameOBject properties of the Inspector view, expand the Tags dropdown and choose one.

A GameObject can only have one Tag assigned.

Unity includes some built-in Tags which do not appear in the Tag Manager:

* Untagged
* Respawn
* Finish
* EditorOnly
* MainCamera
* Player
* GameController

In a Script, you can use the functions:

* GameObject.**FindWithTag**("tagName"), will return the one GameObject with the tag
* GameObject.**FindGameObjectsWithTag**("tagName"), will return a list with all GameObjects with the tag