.. _doc_porting_from_unity:

High Level Comparison to Unity3D
=========================

Something about the arch differences


Node Differences
=========================

In godot our base class for everything is Node, and in unity it was MonoBehaviour.

MonoBehaviour has:
- MonoBehaviour() becomes _init() 
- Start() which becomes _ready()
- Update() which becomes _update(delta)
- FixedUpdate() becomes _physics_process(delta)
- OnGUI() - doesn't exist.
- OnDisable/Enable - is a notification OR a signal on visibility changed.


Does Godot have components?
=========================

Not really, components are just an extra node. One "node" can only contain a single script.
This simplifies the code for users.

Porting your existing C# to Godot
=========================

While this is possible to do, you might find it easier to copy your classes and remove the MonoBehaviour.
You will need to change MonoBehaviour to an internal Godot type.


Platforms supported using C#
=========================

Something about the arch differences

**Every game engine is different and fits different needs.**
Some things and stuff


Links to concepts:
=========================

UI - How to create a simple user interface (similar to unity rect system)
Procedural mesh creation - SurfaceTool page
Physics - How to configure physics nodes
Networking