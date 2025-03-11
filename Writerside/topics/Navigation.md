# Navigation

The navigation system allows to create characters that can intelligently move around the game world, using navigation meshes that are created automatically from the Scene geometry.

Dynamic obstacles allow you to alter the navigation of the characters at runtime, while off-mesh links let you build specific actions like opening doors or jumping down from a ledge.

The navigation system needs its own data to represent the walkable areas in a scene. The walkable areas define the places in the scene where the agent can stand and move.

They are build automatically from the geometry in the scene by testing the locations where the agent can stand. Then the locations are connected to a surface laying on top of the scene geometry. This surface is called NavMesh.

![](image26.png)

The NavMesh stores this surface as convex polygons. They are a useful representation, since we know that there are no obstructions between any two points inside a polygon.

In addition to the polygon boundaries we store information about which polygons are neighbours to each other.

![](image60.png)

To find path between two locations in the scene, we first need to map the start and destination locations to their nearest polygons. Then we start searching from the start location, visiting all the neighbours until we reach the destination polygon.

Tracing the visited polygons allows us to find the sequence of polygons which will lead from the start to the destination.

The sequence of polygons which describe the path from the start to the destination polygon is called corridor. The agent will reach the destination by always steering towards the next visible corner of the corridor.

![](image55.png)

When dealing with multiple agents moving at the same time, they will need to deviate from the path when avoiding each other.

Trying to correct such deviations using a path consisting of line segments becomes difficult and error prone.

Since the agent movement in each frame is quite small, we can use the connectivity of the polygons to fix up the corridor in case we need to take a little detour.

The steering logic takes the position of the next corner and based on that figures out a desired velocity, but using it can lead to collisions. Obstacle avoidance chooses a new velocity which balances between moving in the desired direction and preventing future collisions.

![](image36.png)

After steering and obstacle avoidance, the final velocity is calculated.

The agents in Unity are simulated using a simple dynamic model, which also takes into account acceleration to allow more natural and smooth movement.

There are two types of navigation: global and local

![](image10.png)

Global is used to find the corridor across the world. Finding a path across the world is a costly operation requiring quite a lot of processing power and memory.

The linear list of polygons describing the path is a flexible data structure, and it can be locally adjusted as the agent moves.

Local navigation tries to figure out how to efficiently move towards the next corner without colliding with other agents or moving objects.

There are other obstacles than just other agents, like crates or vehicles. They can be handled using local obstacle avoidance or global pathfinding.

When an obstacle is moving, it is best handled using local obstacles avoidance, this way the agent can predictively avoid the obstacle.

When the obstacle becomes stationary, it should affect the global navigation, that is the NavMesh, and must be changed.

![](image9.png)

Changing the NavMesh is called carving. This process detects which parts of the obstacle touches the NavMesh and carves holes into it. It is a computationally expensive operation.

The connections between the NavMesh polygons are described using links inside the pathfinding system. Sometimes it is necessary to let the agent to navigate across places which are not walkable, like jumping a fence.

![](image19.png)

These actions can be annotated using Off-Mesh Links which tell the pathfinder that a route exists through the specified link.

The Navigation Area defines the difficulty of traversing across specific areas and lower costing areas take precedence in pathfinding.