# MonoBehaviour API

A script in Unity does not run continuously in a loop until it completes its task. Unity passes control to a script intermittently by calling certain functions that are declared within it. Once a function has finished executing, control is passed back to Unity.

These functions are known as event functions since they are activated by Unity in response to events during the gameplay.

Unity uses a naming scheme to identify which function to call for a particular event. The more common are:

* **Awake()**, is called when the script is being loaded, before Start. It is used to initialize any variables or game state before the game starts
* **Start()**, is called when the script is enable
* **Update()**, is called every frame if MonoBehaviour is enabled
* **FixedUpdate()**, is called every fixed interval defined in Edit > Project Settings > Time > Fixed Timestep if MonoBehaviour is enabled, and it's used internally for physics and for framerate independent things
* **LateUpdate()**, is called after Update if MonoBehaviour is enabled
* **OnGUI()**, is called for rendering and handling GUI events
* **OnDisable()**, is called when the behaviour becomes disabled or inactive
* **OnEnable()**, is called when the behaviour becomes enabled or active