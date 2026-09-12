# 3D printing 


![prothesis full](images/Prosthesis_full.png){width=70% .center}

ProMice is made up mostly of 3D-printed parts. Two very common prototyping techniques are used:
PLA filament printing and resin printing. 
In this section we will describe each of the 3D-printed parts and their function. In each description we wil share the print orientation for quality and functional results.

## Resin-printed parts
Resin-printed parts are those that require the highest level of detail and quality; they are also the smallest parts.
To print the resin parts, we used the [Form 4 Printer](https://formlabs.com/3d-printers/form-4/) and the
general-purpose [gray resin](https://formlabs.com/products/grey-resin/). This resin offers a good balance of mechanical properties, particularly
a soft response to friction and a detailed finish.

The printer settings for layer height are the default ones.

![layer thickness](images/layers_thickness.png){ width=70% .center }

![grey resin](images/grey_resin.png){ width=50% .center }


The image below shows the 3D model of the parts that are printed in resin. These are: the frontal structure where the joints are located and the pulleys with their
tensioning system for the actuating cables.

![Resin parts](images/resin_parts.jpg){width=70% .center}



### The forearm 

![forearm 3D](images/forearm_3D.png){width=60% .center}

The forearm is the end effector of the system, and there is no wrist joint. It was created by scanning a real mouse leg. The fingertips serve as the end effector. On the fingers, you can see small recesses for the wires of a capacitive sensor; the idea is to be able to detect touch at specific points.

The rear section has a recess for fitting the [Hall sensor](https://www.ti.com/product/TMAG5273?qgpn=tmag5273) or encoder. The cavity
is aligned with the elbow’s axis of rotation, and directly at the height of the axis are the grooves for inserting the
elbow ball bearings. Perpendicular to the joint’s axis of rotation are the two holes through which the actuating cables pass

![forearm labels](images/forearm_labels.png){width=60% .center}

Regarding the orientation for printing, it can be placed vertically as depicted below, or horizontally. A vertical position improves the details
of the capacitive sensor cavities, but the holes for the actuating cables could get clogged, so they should be done manually. 
The horizontal position does not present the clogged holes sproblems, but trades with the surface and capacitive sensor details. 
In both cases you will obtain a functional piece.

![forearm resin](images/forearm_resin.jpeg){width=30% .center}
 
![forearm printing](images/forearm_printing.png){width=30% .center}




### The ball-arm of the ball joint


This ball-arm is divided into two parts; the larger section has chambers for integrating what we call the [Yaw-lock system](mechanical_design.md#yaw_lock_system).
The rest is a sort of cover to complete the sphere. The design of the piece and its dimensions are detailed in the [Mechanical design](mechanical_design.md) section.

![ball arm 3D](images/ball_arm_3D.png){width=60% .center}

This piece was made to be actuated in two degrees of freedom; therefore, the arm of the ball is a stalk with a sort of mini-platform at the lower end featuring eight holes, all of which are used to insert and attach the actuating cables. The four outer holes are for the main actuation; the remaining four are intended to actuate the component during
a Hall sensor linearisation phase. On the top there is a cavity to integrate a magnet, there is also a longitudinal cavity in the stalk into which a small rod is inserted to support the elbow joint.

![ball arm labels](images/ball_arm_labels.png){width=70% .center}

Resin printing is also a layer-by-layer printing technique. This results in ovalisation of cylindrical cavities and holes if they are printed horizontally.
Given that the geometry of the ball-arm contains both horizontal and vertical cylindrical cavities, priority must be given to those requiring greater printing precision.
The magnet cavity is the top priority, as any printing distortion there would result in unwanted displacement and misalignment of the magnet, which would cause asymmetry
in its positioning relative to the Hall sensor in the socket. It is therefore advisable to print the ball-arm in a vertical position.

![ball_arm_printing](images/ball_arm_printing.png){width=50% .center}
![ball arm resin](images/ball_arm_resin.jpeg){ width=30% .center}

 
### The socket



The socket is also divided into two parts so that it can be assembled with the ball, and we use a ring to hold the two parts together.
![socket 3D](images/socket_3D.png){width=60% .center}

On both parts, we can see various grooves and cavities. The larger part has 9 cylindrical cavities, 8 of which are
arranged radially and symmetrically, whilst one is in the centre.
The sheath for the Bowden cable is inserted into the 8 radial cavities. The spherical cavity that houses the ball has a housing into which a mini bearing is inserted; this forms part of the [Yaw-lock system](mechanical_design.md#yaw_lock_system).
Directly in the centre, above the spherical cavity, is the cavity for the ball joint Hall sensor, which will measure the movement of the joint. This cavity is
connected to the ninth cylindrical cavity to allow the sensor cables to pass through.
The second part of the socket is symmetrical to the lower part of the first, except that it does not house a bearing.
Its function is to hold the ball in place together with part one.

![socket labels](images/socket_labels.png){width=60% .center}

Given that we must avoid creating supports within the spherical cavity during the printing process and ensure that the cylindrical cavities remain free from deformation, the printing orientation must be vertical.
![socket_printing](images/socket_printing.png){width=70% .center}
![Socket parts](images/socket_parts.jpeg){ width=40% .center } 
  



### Shoulder ball bearing housing

![shoulder ball bearing housing 3D](images/shoulder_ball_bearing_housing_3D.png){width=80% .center}

This section consists of three parts. It houses the shoulder Z-axis rotation system. It has housings for two ball bearings and two recesses for the Bowden cable. The largest part is the
component that supports the front of the prosthesis; the following image shows the front support hole marked, which is used to secure the prosthesis to a
[Flex arm](https://www.amazon.fr/SMALLRIG-Articul%C3%A9-Friction-R%C3%A9glable-Moniteur/dp/B08B63WXWN/ref=sr_1_1?crid=36M1VY295M2MQ&dib=eyJ2IjoiMSJ9.KGiIRm_QPLJhUIhU1N34kqAYeY66ar65T2RxIAyC5f-uMuk5aTKTYd3H7nni7IM6WjRBQcNbQ9WdEJuWjIoZFVrEm2gYyOMpcHyqmOA4SWdRUADsrTYoYQMwC7yEsQ6xcVR144ers6Tz1gCvJFgjxIjzeC-KBF_7Zjg-uiVb4PxhTXkaV829QS1jBANfmplZqVrv-mAeqohvgv2w3wQRbfktaMZ0KMstzPFnAle9ixHhLMXd_0YWc8hwDBu47y6c5cgRjOTXP1nDM0HJygyaWxgcuB6_G2oyH0hdsHEWegw.Qr0gYVoHgxusC7XTGdkxMi8Gfpx3oLuNlquboS8tCac&dib_tag=se&keywords=bras%2Bmagique&qid=1786965479&sprefix=braz%2Bma%2Caps%2C147&sr=8-1&th=1).
The two remaining pieces are complementary parts designed to hold the bearings and to hold the Bowden cable.
 
![shoulder ball bearing housing labels](images/shoulder_ball_bearing_housing_labels.png){width=70% .center}




![shoulder case 2 resin](images/shoulder_case_2_resin.jpeg){ width=40% .center }


 
 Orientation for 3D printing :
  INSERER IMAGE
![shoulder ball bearing housing](images/shoulder_ball_bearing_housing.png){width=70% .center} 


### Shoulder rotatory pieces 
![shoulder rotatory pieces 3D](images/shoulder_rotatory_pieces_3D.png){width=60% .center}

This is a set of three components that transmit Z-axis rotation from the shoulder to the rest of the prosthesis. The top component is inserted into the pulley and has a recess for a magnet situated directly beneath an encoder used to measure rotation. The actuating cables are attached to the pulley, as shown by the red line in the figure below. The bottom component forms the connection between the pulley and the socket.

![shoulder rotatory pieces labels](images/shoulder_rotatory_pieces_labels_v2.png){width=85% .center}
 
Orientation for 3D printing :
  
![shoulder rotatory pieces printing](images/shoulder_rotatory_pieces_printing.png){width=70% .center} 
### Top encoder base. 
![top encoder base 3D](images/top_encoder_base_3D.png){width=60% .center}

Esta ultima pieza sostiene un uStepper driver para medir la rotacion del hombre en el eje Z 

![top encoder base](images/top_encoder_base.png){width=45% .center}

![top encoder base](images/top_encoder_base_resin.jpeg){width=45% align=left}

![top encoder base printing](images/top_encoder_base_printing.png){width=45% .center}

\\
### Pulleys
![pulley views](images/pulley_views.png){width=75% .center}



<p style="color: #999999;">There are four pulleys in total, each mounted on a motor. They are used to transmit the motors’ rotation to the prosthesis, allowing it to move along its different axes. Motion is transmitted via wires, which are attached to the end of the prosthesis on one side and wound around the pulley on the other, as shown below:</p>

![pulley cable](images/pulley_cable.png){width=75% .center}

<p style="color: #999999;">The tension of the wires can be adjusted by turning the corresponding screw: turning it clockwise increases the tension on the wire, while turning it counterclockwise decreases it.</p>


![pulley screw](images/pulley_screw.png){width=75% .center}
 
Orientation for 3D printing :
 
![pulley printing](images/pulley_printing.png){width=70% .center}

## impresion con PLA

The motors rack and PCB housing are printed in PLA, this pieces do not require a high level of precision. PLA also produces less brittle parts, which is essential for supporting the weight of the motors.
![PLA parts](images/PLA_parts.jpg)

Orientation for 3D printing :
![motors suport](images/motors_suport_printing.png){width=70% .center}
 
![teensy suport printing](images/teensy_suport_printing.png){width=50% .center}
