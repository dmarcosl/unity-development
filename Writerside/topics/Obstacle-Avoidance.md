# Obstacle Avoidance

## NavMesh Agent

Nav Mesh Agent components help you to create characters which avoid each other while moving towards their goal. Agents reason about the game world using the Nav Mesh and they know how to avoid each other as well as other moving obstacles.

![](image64.png)

Agent Size

* **Radius**, radius of the agent, used to calculate collisions between obstacles and other agents
* **Height**, the height clearance the agent needs to pass below an obstacle overhead
* **Base offset**, offset of the collision cylinder in relation to the transform pivot point

Steering

* **Speed**, maximum movement speed
* **Angular Speed**, maximum rotation speed
* **Acceleration**, Maximum acceleration
* **Stopping distance**, the agent will stop when this close to the goal location
* **Auto Braking**, when enabled, the agent will slow down when reaching the destination, disable this for where the agent should move smoothly between multiple points

Obstacle Avoidance

* **Quality**, obstacle avoidance quality. If you have high number of agents, you can save CPU time by reducing the obstacle avoidance quality. Setting to none, will only resolve collision, but will not try to actively avoid other agents or obstacles
* **Priority**, agents of lower priority will be ignored by this agent when performing avoidance. The value should be between 0-99 where lower is higher priority

Path Finding

* **Auto Traverse OffMesh Link**, set true to automatically traverse off-mesh links. You should turn this off when you want to use animation or some specific way to traverse off-mesh links
* **Auto Repath**, when enabled, the agent will try to find path again when it reaches the end of a partial path. Where is no path to the destination, a partial path is generated to the closest reachable location to the destination
* **Area Mask**, describes which area types the agent will consider when finding a path

The agent is defined as a cylinder whose size is specified by the Radius and Height properties. The cylinder moves with the object but always remains upright even if the object itself rotates.

The shape of the cylinder is used to detect and respond to collisions between other agents and obstacles.

## NavMesh Obstacle

The NavMesh component allows you to describe moving obstacles that NavMesh Agents should avoid while navigating the world.

While the obstacle is moving, the NavMesh Agent do their best to avoid it. When the obstacle is stationary, it carves a hole in the NavMesh that the Agent will avoid.

![](image61.png)

* **Shape**, the shape of the obstacle
    * Box
    * Capsule
* **Carve**, when the Carve checkbox is ticked, the NavMesh Obstacle creates a hole in the NavMesh
    * **Move Threshold**, Unity treats the NavMesh Obstacle as moving when it has moved more than the distance setted
    * **Time to Stationary**, the time in seconds to wait until the obstacle is treated as stationary
    * **Carve Only Stationary**, when enabled, the obstacle is carved only when it is stationary

If Carve is not enabled, the Agent can get stuck in cluttered environments.