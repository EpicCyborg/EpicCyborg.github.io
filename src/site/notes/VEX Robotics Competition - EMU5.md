---
{"dg-publish":true,"permalink":"/vex-robotics-competition-emu-5/"}
---

<iframe src="https://drive.google.com/file/d/1cfxwr6lNmaejW4-UDuXCwfzXaNF5_f3I/preview" width="640" height="480" allow="autoplay"></iframe>
For the VEX season 2022-2023 game "Spin Up", team EMU5 built a catapult robot to score 3 discs at a time. I designed custom components for 2D CNC milling and 3D printing in SOLIDWORKS and Fusion 360 alongside assemblies and technical drawings.
# 2D Components
![Assets/VEX_PolycarbonateChassis.png](/img/user/Assets/VEX_PolycarbonateChassis.png)
*Polycarbonate chassis for reinforcement on C-channels*
This was my first exposure to CAD in Fusion 360 and SOLIDWORKS, contributing to a disc shooting robot with remote-control and autonomous capability. I started contributing with 2D designs for custom parts fabricated using CNC milling on polycarbonate and aluminium. I learned to work closely with the more experienced builders on the team to understand the CAD thought process, then move on to 3D components. [[#Technical Drawings|Technical drawings]] were made alongside the components as part of the project log book.
# 3D Printed Components
To optimise for 3D printing, I took into account print orientation, overhang angles, and plate contact area. Examples were gears and the tracking wheel mount that used springs to keep the tracking wheel on the ground at all times.

| ![Assets/VEX26Gear.webp](/img/user/Assets/VEX26Gear.webp) | ![Assets/VEX3DPrint.webp](/img/user/Assets/VEX3DPrint.webp) | ![Assets/VEXTrackingWheelUp.webp](/img/user/Assets/VEXTrackingWheelUp.webp) | ![Assets/VEXTrackingWhellDown.webp](/img/user/Assets/VEXTrackingWhellDown.webp) |
| -------------------------- | --------------------------- | ----------------------------------- | ------------------------------------- |
## Motor Mounts
One of the most important components was the motor mount. They had to be robust to withstand the force and heat of the motors, while also allowing them to be replaced easily since they would often overheat or wear out. I designed and iterated upon the motor mount to optimise for the following:
>[!abstract] Requirements
>- Mechanically secure attachment to robot
>- Easy to take off and replace
>- Minimise footprint

| ![Assets/VEXMotorMountV1.webp](/img/user/Assets/VEXMotorMountV1.webp) | ![Assets/VEXMotorMountV1Fit.webp](/img/user/Assets/VEXMotorMountV1Fit.webp) |
| -------------------------------- | ----------------------------------- |

Version 1 of the custom motor mount was printed and used on the 2022-2023 robot. To improve upon the design further, for 2023-2024, I worked on an improved version that took less space, using a horizontal locking pin to detach and reattach them easily. The first revision was too tall, but I identified a lower space for the pin to go through by analysing the cross section. The final motor mount successfully optimised for space:

| ![Assets/VEXMotorMountV2.webp](/img/user/Assets/VEXMotorMountV2.webp) | ![Assets/VEXMotorMountV3.webp](/img/user/Assets/VEXMotorMountV3.webp) | ![Assets/VEXMotorMountV3Model.webp](/img/user/Assets/VEXMotorMountV3Model.webp) |
| -------------------------------- | -------------------------------- | ------------------------------------- |
# SOLIDWORKS Assemblies

| ![Assets/VEXDromaiusIntake.webp](/img/user/Assets/VEXDromaiusIntake.webp) | ![Assets/VEX_ChassisAssembly.webp](/img/user/Assets/VEX_ChassisAssembly.webp) |
| ---------------------------------- | ------------------------------------ |

I was tasked with creating the SOLIDWORKS assemblies and subassemblies since this would help us create our Bill of Materials. However, we realised that time constraint meant that parts had to be cut from the digital recreation, such as the overwhelming number of nuts, bolts and chains that took time to place, and caused the assembly file to lag the computer. Therefore, larger parts like C-channels, wheels and gears were prioritised, and mirroring was used for efficiency.

The disc intake module on the left was assembled independently based off physical prototypes,  and combined to the main chassis assembly on the right.

Through this experience, I learned how to make assemblies in SOLIDWORKS using "mates", and that each component required multiple mates to be fixed in place. The C-channels at right angles would require three coincident mates, while the gears and wheels on axles would only require one concentric and one coincident mate.
# Calculations for Pathfinding
$$
\begin{align}
a_{c} &= \sqrt{ (X''(t))^{2} + (Y''(t))^{2} } \\
F_{c} &= m\sqrt{ (X''(t))^{2} + (Y''(t))^{2} }
\end{align}
$$
I also assisted in calculations and implementation for the pathfinding algorithm, which used quintic spline. Centripetal force $F_{c}$ needed to be minimised in the autonomous pathfinding algorithm to reduce error. The robot's odometry used cartesian coordinates, and was able to determine this by taking double derivatives of $x$ and $y$ coordinates. $F_c$ would be minimised for the pathfinding algorithm. 

# Technical Drawings
![Assets/VEXCatapultArm.webp](/img/user/Assets/VEXCatapultArm.webp)

| ![Assets/Catapult Platform500.webp](/img/user/Assets/Catapult%20Platform500.webp) | ![Assets/Intake Brace500.webp](/img/user/Assets/Intake%20Brace500.webp) |
| ------------------------------------- | -------------------------------- |
| ![Assets/Intake Frame500.webp](/img/user/Assets/Intake%20Frame500.webp)      | ![Assets/Roller Tower500.webp](/img/user/Assets/Roller%20Tower500.webp) |
