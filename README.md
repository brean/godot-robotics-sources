# Godot Robotics
Sources, Links and Information on using the Godot Game Engine in Robotics.

## Use cases
### Simulation
There is already some very advanced and open source Robotics simulation systems out there, for example [Gazebo](http://gazebosim.org/) or [MARS](https://github.com/rock-simulation/mars), but its always good to have alternatives.

### Create User interfaces for Web and other devices
Godot is already used in the industry for use in Robot for exactly that, but tutorials for exactly that use case is missing.

## Benefits from using Godot in Robotics
- Fast and Realistic 3D Graphics including lighting (especially with Godot 4 - important for Robot Perception/Computer Vision training)
- Interfaces for different physics engines, an own physics engine as another alternative for bullet/ODE in MARS/Gazebo/pybullet.
- HTML5-export to create robot control user interfaces on modern mobile devices
- A scripting language to easily interface with the enviroment that is also very good documented (GDScript / C#), existing programming documentation
  - allows the implementation of complex behavior without the need of additional dependencies (non-robotic actors, think of for example workers in a production scenario)
- Multiple importers for 3D-Models and animations with an existing store, so its easy to let an entity in the simulation be controlled by a human (for example use the [Open 3D Mannequin](https://github.com/GDquest/godot-3d-mannequin))
- easy VR/AR integration

## Existing Software
- [**Godot-Sim**](https://github.com/plaans/gobot-sim) - a simple 2D robot simulator for Godot, also implementing jobshop for planning
- [**ROS Websocket interface for godot**](https://github.com/rudyvic/ROS-Websocket) - an interface to use the ROS WebSuite
- [**Godot ROS pcviz**](https://github.com/ymd-stella/godot_ros_pcviz) loads and visualize recorded bag-files
- [**Godot ROS**](https://github.com/flynneva/godot_ros) rclcpp (ROS2) example implementation to connect to a ROS2-node from within Godot using C++

## What's missing?
- an importer for URDF and SDF for Gazebo models (https://app.ignitionrobotics.org/fuel/models)
  - you can import models into blender using [Phobos](https://github.com/dfki-ric/phobos) and then export to OBJ or FBX and import in Gazebo but a direct import would be nice
- an interface similar to Gazebo
  - the default Node-based Gazebo-interface is already close
- ROS-Godot interface that allows to create ros-nodes from GDScript (ideally from both, the web suite and ROS directly so we can run a heavy simulation locally but also a user interface form a web browser where both have a similar API and both run in Godot?)
- documentation specifically for robotics / a "robotics bundle" or general entrypoint for robotics enthusiasts
  - real-live examples!
  - Demo scenes and more robots!
