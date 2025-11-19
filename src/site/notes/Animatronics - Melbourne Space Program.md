---
{"dg-publish":true,"permalink":"/animatronics-melbourne-space-program/"}
---


| ![assets/DinoFinal.webp](/img/user/assets/DinoFinal.webp)<br>![assets/dinoskin.gif](/img/user/assets/dinoskin.gif) | ![assets/dinoani.gif](/img/user/assets/dinoani.gif)<br>![assets/dinonod.gif](/img/user/assets/dinonod.gif) |
| ------------------------------------------------------ | -------------------------------------------------- |
# Dinosaur Animation (Blender)
| ![assets/dinoanimationblender300.gif](/img/user/assets/dinoanimationblender300.gif) | ![assets/dinowakeup300.gif](/img/user/assets/dinowakeup300.gif) |
| --------------------------------------- | ----------------------------- |

One of the requirements for the animatronic was to have expressive animations. My task was to create a seamless and efficient workflow, so I did the following: 
>[!info] Process
>1. Export .fbx files of the mechanisms from CAD software (Fusion 360)
>2. Import the models into Blender
>3. Rigging: Align armature joints with those on the mechanisms (pushrods, servo motors)
>4. Add controllers for orientation of head, eyes, eyelids and tail, moving servo motors via inverse kinematics
>5. Create animations by moving controllers and adding keyframes
>6. Export servo motor angles into C++ arrays using python plugin 

Using the software developed by other members of the team, animations were able to be translated quickly into the physical prototype.

# CAD (Fusion 360)

| ![assets/dinobody.gif](/img/user/assets/dinobody.gif) | ![assets/DinoBodyFab.webp](/img/user/assets/DinoBodyFab.webp) | ![assets/DinoTailCAD300.webp](/img/user/assets/DinoTailCAD300.webp) |
| ------------------------ | ---------------------------- | ------------------------------- |

I was responsible for designing the structural parts for the tail, body and head in Fusion 360. Laser cutting was the primary fabrication method to cut down on fabrication time and cost for rapid prototyping. Mounting holes were placed so other parts, such as the 3D-printed neck mechanism. All geometry used the 3D model made by the team sculptor as a reference.
3D-printed shells were made to capture the organic geometry of the dinosaur, such as the belly above, or parts for the head shown below. Since the silicone skin would go over, low polygon count was used to speed up the CAD software. 

| ![assets/dinohead.gif](/img/user/assets/dinohead.gif) | ![assets/DinoHead.webp](/img/user/assets/DinoHead.webp) |
| ------------------------ | ------------------------- |
# Animatronic Quokka
For the second animatronic, the quokka, I was Team Lead, in charge of administrative tasks such as team meetings, organising events and inventory management. I ensured that all work was integrated between software, electrical and hardware subsystems.

![assets/blockdiagram.webp](/img/user/assets/blockdiagram.webp)

I mentored team members in technical skills and to help them integrate the components above, while continuing technical work in 3D modelling, mechanical design, 3D printing and circuit design.

![assets/QuokkaHeadBlender.webp](/img/user/assets/QuokkaHeadBlender.webp)
*Early quokka head 3D model in Blender*

![assets/quokkafinger.gif](/img/user/assets/quokkafinger.gif)
*Print-in-place quokka finger mechanism CAD*

The following was the team's resulting head mechanism prototype: 
![assets/QuokkaPrototype500.jpg](/img/user/assets/QuokkaPrototype500.jpg)
*Quokka head prototype*