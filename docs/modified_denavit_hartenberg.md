This section documents the direct geometric model implemented in `model.h`. The model uses the Modified Denavit--Hartenberg (MDH)
convention to calculate the end-effector Cartesian position from the four active joint angles.
## 1. MDH convention

!!! list "MDH convention"

    - Twist angle $\alpha_{i-1}$ is the angle between $z_{i-1}$ to $z_i$ measured about $x_{i-1}$
    
    - Link length $a_{i-1}$ is the distance from $z_{i-1}$ to $z_i$ measured along $x_{i-1}$
    
    - Offset length $d_{i-1}$ is the distance from $x_{i-1}$ to $x_i$ measured along $z_i$
    
    - Joint anglze $\theta_i$ is the angle between $x_{i-1}$ to $x_i$ measured about $z_i$

![Denavit hartenber model](images/MDH_model.png){width=500 .center}


The third coordinate frame is an auxiliary frame used to represent the spherical-joint rotations while satisfying the MDH frame constraints,
such as $\forall x$, $x_i$ $\perp$ $z_{i+1}$ . It is modelled as a fixed joint between frames 2 and 4.

The table below describes the six transformations in the kinematic chain. The model has four active joints; rows 3 and 6 are fixed
transformations.


!!! table "MDH table"
    |   Link  |    \(\theta_{i}\)(deg)   | \(\alpha_{i-1}\)(deg) | \(a_{i-1}\)(cm) | \(d_i\)(cm) |Join type |
    |:-------:|:------------------------:|:---------------------:|:---------------:|:-----------:|----------|
    | 1       | \(q_0 + \theta_{off,0}\) |  $180°$               |$0$              |$1.5$        |Revolute  |
    | 2       | \(q_1 + \theta_{off,1}\) |  $-90°$               |$0$              |$0$          |Revolute  |
    | 3       | $90°$                    |  $180°$               |$0$              |$0$          | Fixed    |
    | 4       | \(q_2 + \theta_{off,3}\) |  $90°$                |$0$              |$0$          |Revolute  |
    | 5       | \(q_3 + \theta_{off,4}\) |  $0°$                 |$1.3$            |$0$          |Revolute  |
    | 6       | \(0 + \theta_{off,5}\)   |  $90°$                |$2.0$            |$0.55$       | Fixed    |                                         


The joint-angle offsets are:
$$
\theta_{\text{off}} = \bigl[0,\; 0,\; -,\; 0,\; 90^\circ,\; 0\bigr]
$$


The angles supplied to the model are in **radians**. The table above
expresses the link dimensions in centimetres, while the C++ constants
store lengths in **millimetres**.

## 3. Homogeneous MDH transformation

For each row, the transformation from frame (i-1) to frame (i) is
computed using the MDH matrix:

$$
{}^{i-1}T_i =
\begin{bmatrix}
\cos\theta_i & -\sin\theta_i & 0 & a_{i-1} \\
\sin\theta_i\cos\alpha_{i-1} & \cos\theta_i\cos\alpha_{i-1} & -\sin\alpha_{i-1} & -d_i\sin\alpha_{i-1} \\
\sin\theta_i\sin\alpha_{i-1} & \cos\theta_i\sin\alpha_{i-1} & \cos\alpha_{i-1} & d_i\cos\alpha_{i-1} \\
0 & 0 & 0 & 1
\end{bmatrix}
$$


