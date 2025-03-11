# Bake Settings

## NavMesh

The process of creating a NavMesh is called NavMesh Baking. It collects the Render Meshes and Terrains of all GameObjects which are marked as Navigation Static, and then processes them to create a navigation mesh that approximates the walkable surfaces of the level.

1. Select the Scene geometry that should affect the navigation
2. Check Navigation Static on
3. Adjust in Windows > Navigation > Bake tab the options
    * **Agent Radius**, defines how close the agent center can get to a wall or edge
    * **Agent Height**, defines how low the spaces are that the agent can reach
    * **Max Slope**, defines max steep of the raps
    * **Step Height**, defines how high obstructions are that the agent can step on
4. Click Bake button

![](image72.png)

The resulting NavMesh will be shown as a blue overlay on the geometry.

When baking is complete, the NavMesh will be saved as an asset in a folder with the name of the scene.

Reducing the size increases the accuracy, memory usage and total bake time.