# Prefabs

A prefab is a type of asset that allows you to store a GameObject (and its childs) with its components and properties as an asset to reuse it multiple times.

There are two ways to create a prefab

* Draw and drop theobject from the Hierarchy view to the Project view
* Asset menu of the top navbar → Create → Prefab, then draw and drop the object from the Hierarchy view to the prefab in the Project view

When a prefab is updated from the Project view, or from the Inspector view and the changes are applied to the prefab, all the instances of the prefab are also updated.

But you can also edit an instance individually without update the prefab.
If you edit a component property, it is marked as bold.

![](image8.png)

If you add a new child in the hierarchy, it is shown black instead of blue.

![](image33.png)

To apply this changes to the prefab and all its instances, when selecting any item of the instance in the Hierarchy, in the Inspector we can found a new option at the bottom of the GameObject properties.

![](image31.png)

* **Select**, selects the prefab object in the Project view
* **Revert**, discard the changes
* **Apply**, update the prefab and all its instances

When you expand a Prefab in the Project view, only the first layer of children is visible.