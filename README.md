# bot3x55

A modular humanoid robot.

<details><summary>External Software Used</summary>
  It's the goal to stick with FOSS applications as much as possible.
  The mechanics and modules are designed in FreeCAD.
  Shells will be created using FreeCAD and Blender.
  Electronics should be designed with KiCAD.
</details>

## Mechanics

To make the robot modular, it has 14 standardized interfaces, connecting 15
modules that form the robot. Each module can exist in many differen version, but it
must conform to certain size restrictions and use the given interface to make it
interchangable between robots.

<details><summary>Example</summary>
  The size and interface of an Elbow module is well defined. Any Elobow module
  must provide and upper arm connector, a lower arm connector, and have two degrees
  of freedom (elbow, rotate upper arm). The elbow joint must be implemented within 
  the bounds of a 50mm x 50mm cylinder, and all hardware must be within bounds.
</details>

Modules ideally implement no more than two rotations. They should be big enogh
for a variety of machanical implementations.

Currently, those modules are: 
 - 2x hand and lower arm: implements the axial rotation of the lower arm, the wrist joint, and finger motion
 - 2x elbow: implements the elbow joint and the radial rotation of the upper arm
 - 2x shoulder: implements one ball joint with two degrees of freedom
 - 2x foot and lower leg: implements the toes, ankle, and axial rotation
 - 2x knee: implements the knee rotation and the axial rotation of the upper leg
 - 2x half hip: implements one ball joint with two degrees of freedom
 - body: implements up to three degrees of rotation above the hip as a spine joint
 - neck: implements up to three degrees of freedom for the head
 - head: implements eye and jaw movement

The modules are assembled using standardised connectors. Connectors provide mechanical
stability, power and bus connections, and are easy to disconnect and reconnect.

Currently, those connectors are:
 - 2x lower arm: connecting the hand/arm module with the elbow module
 - 2x upper arm: connecting the elbow aith the shoulder
 - 2x left and right body: connecting the shoulders with the body
 - 2x bottom left and right body: connectiong each half hip with the body below the spine joint
 - 2x upper leg: connecting the knee to the hip halves
 - 2x lower leg: connecting the foot to the knee
 - neck: connect the neck to the body
 - head: connect the head to the neck

## Shells

Quick thoughts:

Our robot does not come with predefined looks. Just as 3x55 only defines the basic
interfaces between modules and module sizes, it defines the interface of shells with 
modules, and a minimum and maximum physical size for shells.

It is important to separate mechanical engineering from the outer appearance
of the final product. Users generally don't care how a robot works internally,
but are likely to prefer certain looks.

As long as shell designs stay within the specs, any 3x55 shell should fit on
ant 3x55 robot without modifications.

## Sensors

TBD.

## Power

TBD.

## Bus

TBD.

## Protocols

TBD.

## Software

TBD.


