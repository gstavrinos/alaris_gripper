# alaris_gripper
ROS related packages for the ALARIS (https://www.alaris.kz) 3D printable underactuated gripper. For more info on the gripper, refer to the related paper:
https://ieeexplore.ieee.org/abstract/document/7109102

<img src="https://raw.githubusercontent.com/gstavrinos/alaris_gripper/master/alaris_gripper/alaris_gripper.png" width="50%"/><img src="https://raw.githubusercontent.com/gstavrinos/alaris_gripper/master/alaris_gripper/alaris_gripper_gazebo.png" width="50%"/>

# Disclaimer :warning:
* The simulation is **VERY** inaccurate:
  - The phalanx2 joint is not working properly, in the sense that does not move when phalanx1 cannot move anymore. I was planning to create a simple script to move them manually but I cannot find a way to read the state of the mimic joints. Hit me up with an issue or PR if you have an idea. 
  - The inertias, masses and CoMs are all wrong. I tried to calculate the inertias using the meshes' bounding boxes, using this: https://github.com/gstavrinos/calc-inertia
  - The whole gripper is jumping around when in heavy contact with an object. This can be avoided by "gently" touching objects.
* Drivers for the real hardware are not included:
  - When (if) I get my hands on the real thing, I will update this repo with some extra stuff.
* Dependencies have not been included yet. 
