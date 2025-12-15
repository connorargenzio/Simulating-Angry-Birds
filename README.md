# Simulating Angry Birds
My final project for ME-314 Theory of Machines - Dynamics at Northwestern University
## Table of Contents
- [Project Overview](#project-overview)
- [Dynammics Simulation](#dynamics-simulation)
- [Demo](#demo)
## Project Overview

This course studied rigid multibody mechanics, including Lagrangian mechanics, impact dynamics, and variational principles. For my final project, I decided to simulate a system based on the popular mobile game Angry Birds. The system consisted of three rigid bodies: two spheres of equal dimensions, which are the bird and pig, and a rectangular beam on which they sit. This simulation included the dynamics of the multi-body system over time, along with all possible interactions between the three rigid bodies.

All rigid bodies are in gravity, and there are no external, non-conservative forces. The direction of the gravitational force corresponds to the vertical negative y direction. The only other external force is an elastic force from an ideal spring used to accelerate and launch the bird. 

This system has a total of nine degrees of freedom, three for each rigid body. Since this simulation is planar, each rigid body has configuration variables corresponding to its horizontal and vertical positions, namely the x and y coordinates. These coordinates are the position of the centers of mass of each rigid body. In addition, the angle of each rigid body relative to the horizontal x-axis is treated as a configuration variable. While the system exists in three-dimensional space, its z-coordinate is fixed.

The vector of configuration variables as used in the equations and code can be seen below:

$$
\mathbf{q} =
\begin{bmatrix}
x_{\text{bird}} \\
y_{\text{bird}} \\
\theta_{\text{bird}} \\
x_{\text{pig}} \\
y_{\text{pig}} \\
\theta_{\text{pig}} \\
x_{\text{beam}} \\
y_{\text{beam}} \\
\theta_{\text{beam}}
\end{bmatrix}
$$

All rigid bodies initially start at rest. The bird is located at the end of an ideal spring that acts as my simulation’s slingshot. The other end of the spring is fixed at a height of 2m with coordinates (0, 2, 0) in the world frame. The bird and pig are both perfect spheres with radii equal to 0.5m and masses equal to 3kg. The beam, on the other hand, is a rectangular prism with a height of 8m, a width of 0.2m, and a mass of 10kg. The pig sits on top of the beam, which is fixed at a distance of 10m from the origin of the world frame. The bird's initial position can be modified by adjusting the spring's angle and elongation. This produced a different trajectory by launching the bird at various angles with different initial velocities.

My code used homogeneous transformations extensively; thus, I defined four frames in total: three at the center of mass of each rigid body and one at the origin, acting as the world frame. A diagram showing all the relevant frames and the three phases of the simulation can be seen below:


## Dynamics Simulation

## Demo
