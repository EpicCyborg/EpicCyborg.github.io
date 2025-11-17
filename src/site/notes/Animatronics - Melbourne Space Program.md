---
{"dg-publish":true,"permalink":"/animatronics-melbourne-space-program/"}
---


| ![Assets/DinoFinal.webp](/img/user/Assets/DinoFinal.webp)<br>![Assets/DinoSkin.gif](/img/user/Assets/DinoSkin.gif) | ![Assets/DinoAni.gif](/img/user/Assets/DinoAni.gif)<br>![Assets/DinoNod.gif](/img/user/Assets/DinoNod.gif) |
| ------------------------------------------------------ | -------------------------------------------------- |

# Dinosaur Animation (Blender)
| ![Assets/DinoAnimationBlender300.gif](/img/user/Assets/DinoAnimationBlender300.gif) | ![Assets/DinoWakeUp300.gif](/img/user/Assets/DinoWakeUp300.gif) |
| --------------------------------------- | ----------------------------- |

*Wake-up animation of dinosaur rig on blender (left), animation execution on dinosaur (right)*
One of the requirements for the animatronic was to have expressive animations. My task was to create a seamless and efficient workflow for many animations. 
>[!info] Process
>1. Export .fbx files of the mechanisms from CAD software (Fusion 360)
>2. Import the entire model into Blender
>3. Rigging: Align armature joints with those on the model
>4. Add inverse kinematics and ring objects that control orientation of head, eyes, and tail
>5. Export servo motor angles into C++ arrays using plugin 

Using the software developed by other members of the team, animations were able to be translated quickly into the actual model.

# CAD (Fusion 360)

| ![Assets/DinoBody.gif](/img/user/Assets/DinoBody.gif) | ![Assets/DinoBodyFab.webp](/img/user/Assets/DinoBodyFab.webp) | ![Assets/DinoTailCAD300.webp](/img/user/Assets/DinoTailCAD300.webp) |
| ------------------------ | ---------------------------- | ------------------------------- |

*Dinosaur body and tail development using sculpture as reference*
I was responsible for designing the structural parts for the tail, body and head in Fusion 360. Laser cutting was the primary fabrication method to cut down on fabrication time and cost for rapid prototyping. Mounting holes were placed so other parts, such as the 3D-printed neck mechanism. All geometry used the 3D model made by the team sculptor as a reference.
3D-printed shells were made to capture the organic geometry of the dinosaur, such as the belly above, or parts for the head.

![Assets/DinoHead.gif](/img/user/Assets/DinoHead.gif)
*Dinosaur head development from original sculpture*

# Animatronic Quokka
For the second animatronic, the quokka, I was the team lead in charge of administrative tasks for project management such as team meetings, organising events and inventory management. I also designed some mechanisms, such as this print-in-place finger:
![Assets/QuokkaFinger.gif](/img/user/Assets/QuokkaFinger.gif)
*Quokka finger mechanism CAD*

The following was the team's resulting head mechanism prototype: 
![Assets/QuokkaPrototype500.jpg](/img/user/Assets/QuokkaPrototype500.jpg)
*Quokka head prototype*