# Hardware
Like any robotic system, ProMice comprises actuators, mechanical support structures, articulated structures, a motion transmission system, electronics and instrumentation. Below is a general description of the ProMice hardware. Details regarding materials and assemblies can be found in the section [Tutorial](3D_printing.md).

## Actuators and their suport
The system has four Nema 17 stepper motors as actuators, which are mounted on a 3D-printed rack made from PLA. The motors are fitted with a resin-printed pulley and a tensioning system for the actuation cables.

![Motors and rack](images/motors_rack.jpg){ width=70% .center}
## Transmission and articulations system 
ProMice is a cable-driven robotic mouse paw that uses a Bowden-cable-type system for motion transmission. The actuator wire is a 0.2mm thin [stainless steel wire](https://www.filinox.com/fr/terre-mer-culture/609-o-02-mm-fil-inox-316l-v4a-14404-corde-a-piano-poli-qualite-contact-alimentaire-500-metres-3663431002356.html) and the sheath is [PTFE Tube](https://fr.vwr.com/store/product/576865/null).
The articulated front end is the part represented in the robot model. This is where its four degrees of freedom are located: three at the shoulder (spherical joint) and one at the elbow. 

![Bowden actuation](images/front_bowden.jpg){ width=70% .center}

## Electronics & instruentation 
The robot’s main controller is a Teensy 4.1 board ntegrated into in a custom PCB to manage connections.

![PCB teensy](images/PCB_teensy.jpg){ width=50% .center}

To ensure precise control using servomotion, the stepper motors were fitted with uStepperS32 controllers. Position feedback prevents missed steps and also ensures that an absolute position is always maintained, which is an important aspect in robotic systems.
The following image, taken from beneath the motor rack, shows that only the last three motors have the controller installed, whereas the first one is mounted at the top of the articulated system.
The explanation is that it is more accurate to measure the position of the joint locally; therefore, in our 4-DOF system, the rotation about the shoulder’s z-axis is measured locally by a driver that controls the respective actuator.
![uSteppers](images/uStepper_drivers.jpg){ width=50% .center}

The last two remaining degrees of freedom of the shoulder (spherical joint) are measured using a 3D Hall sensor in a socket-ball configuration. The [Sensors](sensors.md) section details the use of spherical coordinates to estimate both degrees of freedom by measuring the three components of the magnetic field from a magnet embedded in the ball of the joint.
The following image shows the position of the sensor directly above the ball cavity in the socket containing the joint.
![Hall sensors socket and elbow](images/hall_sensors_socket.jpg){width=50% .center}

The final degree of freedom (the elbow) is also measured using a Hall sensor positioned perpendicular to the axis of rotation. This encoding is achieved thanks to its small, meticulously constructed bearing system, which is fitted with a tiny magnet. Its manufacture and installation are described in the section [Assembling & instrumentation - Elbow joint ball bearings] (assembling_instrumentation.md#Elbow joint ball bearings]
