

## Shoulder ball-joint-type 
[ProMice prosthesis](index.md#mouse_leg) shoulder is a 3DOF joint from which only $\alpha_1$ is measured.
 $\alpha_2$ and $\alpha_2$ are degrees of freedom coupled by a universal joint. 
 
![Promice universal joint](images/Promice_V1_joints.png){ width=80% .center }

This is a system difficult to instrument if we want to measure the angles. Choosing from the typical encoding 
techniques would mean to instal a sensor on each axe, like a pottentiometer, an optical encoder or a hall sensor for example. 
However, there are Hall-effect sensors that measure the x, y and z components of the magnetic field. This feature
makes it possible to estimate the position of a magnet facing of the sensor.
 

!!! info
    In the [Sensors](sensors.md) section, you can find further details on
    the use of the sensor, such as the component number, data types, angle calculations, sensor-microcontroller connections, etc. 


Building on this idea, we decided to replace the shoulder universal joint by a ball joint. It is a ball-socket configuration that integrates a 3D Hall sensor
inside the housing socket and a disc magnet inlaid in the ball. 

In addition to this, to make all joints instrumented, a second Hall sensor is integrated on the elbow axis. 

![Promice universal joint](images/Promice_V2_joints.png){ width=90% .center }



In order to design such a joint, we first had to take into account the size of the previous version of ProMice as well as that
of the Hall sensor. These two constraints led us to choose the key dimensions. 


![Old ProMice version size](images/old_promice_size.png){width=80% .center}

![Hall sensor size](images/hall_sensor_size.png){width=80% . center}

!!! info
    Hall sensor dimentions are in mm
## Ball joint design

For the design, it was necessary to 3D print a sphere with a rod attached and a socket. We carried out a series of iterations
of 3D printing to determine what would be a reasonable size whilst meeting the dimentions constraints.

Given the limitations of resin 3D printing observed on the spherical surface of the ball as well as on the inside of the socket,
we chose a diameter of $8$ $mm$ for the ball and $3$ $mm$ for the stick.

![Hall sensor size](images/ball_size.png){width=50% .center}

!!! info
    In the assemblings, it is important to allow for a tolerance between pieces.
    In our case, there is a difference of 0.04 mm between the diameter of the sphere and that of the inside of the socket.
    This tolerance also applies to the holes.

### Ampitud of movement of ball joint
The most important parameter when designing the socket that holds the ball is the range of movement
it will allow. We also carried out some simulations to examine the attenuation of the magnetic field depending on
the angle of the arm. The following image shows motion range $\theta_d$ allowed by the sockets geometry. 


![Amplitude](images/Socket_chord.png){ width=38% .center }

We calculated a desired range of motion $\theta_d$ by the following formulas: 

\begin{equation} \label{eq:theta_chord}
    \theta_c = arcsin(\frac{d_s}{2r})+\theta_d
\end{equation}

\begin{equation} \label{eq:chord}
    c = 2*r*sin(\theta_c)
\end{equation}


The next step was to chose the magnet dimentions and the sensor-magnet air gap. From the commercially available magnets wee took three different
sizes to experiment. All of them are disc-type magnets with axial magnetization and $1$ $mm$ thickness. Diameters were $1$, $2$ and $3$ $mm$.

![Magnet placement](images/Ball_magnet_sensor.png){ width=55% .center}

The minimum sensor-magnet air gap has to be calculated in order to avoid colisions between them. 

\begin{equation} \label{eq:AG}
    AG_{min} = l_{a-m}\left(\sqrt{1+(\frac{d_m}{l_{a-m}})^2}-1\right)
\end{equation} 


To chose the size of the magnet and the magnet-sensor gap, we have performed some [Hall sensor simulations](sensors.md#sensor-simulations). 
In the following plot, on the left you can see the magnet density vs tilt angle for the 3 available diameters. As expected, the largest magnet allows 
more tilt sensing, whereas the other two have an important magnetic density drop before the 30 degrees. Therefore we keep the largest magnet.


![Air Gap simulation](images/AG_MD_plot.png){width=95% .center}

The air gap simulation (shown on the right side) was performed using the chosen magnet (3 mm diameter). It is important to remark that the tilt pivots on the $y$ axis, meaning that there should not be 
magnetic density variatins on this axis. However the $1$ $mm$ airgap causes variation on the $y$ axis. This variation is called cross measuring, and It is an intrinsic effect of the sensor's point measurement.
To avoid this effect as much as we can, the $1.5$ $mm$ airgap is the best option. 

We have summarized the design dimensions of the ball joint in the following table.

|  Ball joint design parameters  |         Value        |
|:------------------------------:|:-------------:  |
| Ball radius                    | $r$ = 4 𝑚𝑚        |
| Amplitude of movement          | $𝛼_{2,3}$ = ±35°|
| Magnet diameter                | $𝑑_𝑚$ = 3 𝑚𝑚    |
| Magnet thikness                | $th_m$ = 1 𝑚𝑚
| Magnet-sensor gap              | 𝐴𝐺  = 1.5 𝑚𝑚      |
|Socket-ball tolerance           | $T$ = 0.02 𝑚𝑚   |
| Stick diameter                 | $𝑑_𝑠$ = 3 𝑚𝑚    |
|Socket chord                    | $c$ = 8 𝑚𝑚 |



## Yaw-lock system

The shoulder joint is a ball-and-socket joint in which rotation about the z-axis is transmitted via an upper pulley located above
the ball joint. This decoupling is necessary because it would be impossible to actuate the three degrees of freedom if they were coupled inside the current ball joint's design.

![shoulder rotation on Z](images/z_rotation.png){width=60% .center}

This results in locking the Z-axis rotation of the ball joint. Therefore, the second major stage of the mechanical design consisted of a mechanism
that allows for only two degrees of freedom. This design presented an interesting mechanical challenge, as the 2DOF rotation mechanism
had to be housed inside the ball joint; otherwise, the joint would take up too much space. The proposed solution is what we have called
the Yaw-lock system. It is a tiny mechanism consisting of three mini bearings and a T-shaped rotation shaft. This mechanism allows for
pitch and roll rotations (rotation around the $x$-axis and the $y$-axis) and can be assembled inside the ball of the joint.

![Yaw-lock system](images/yaw_lock_system.png){id="yaw_lock_system" width=70% .center }

The ball bearings have a $1$ $mm$ thickness, an inner diameter of $1$ $mm$ and an outer diameter of $3$ $mm$. The T-shaft was crafted using a steel rod and tin soldering. 

![Yaw-lock system "d"](images/YLS_expanded.png){width=50% .center}

!!! info
    The fabrication of the T-shaft is detailed in [Tutorial](3D_printing.md) -> [Soldering](soldering.md)
