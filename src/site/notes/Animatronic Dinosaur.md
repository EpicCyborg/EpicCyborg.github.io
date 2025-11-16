---
{"dg-publish":true,"permalink":"/animatronic-dinosaur/"}
---

# Dinosaur Animation (Blender)

| ![Assets/DinoAnimationBlender.gif](/img/user/Assets/DinoAnimationBlender.gif) | ![Assets/DinoWakeUp300.gif](/img/user/Assets/DinoWakeUp300.gif) |
| ------------------------------------ | ----------------------------- |


One of the requirements for this project was to have expressive animations. My task was to create a seamless workflow . I had prior experience modelling and rigging characters in Blender, so I applied it to this project through the following steps:
1. Export .fbx files of the mechanisms from CAD software (Fusion 360)
2. Import the entire model into Blender
3. Rigging: Align armature joints with those on the model
4. Add inverse kinematics and ring objects that control orientation of head, eyes, and tail
5. Export servo motor angles into C++ arrays using plugin 

Using the software developed by other members of the team, this animation was able to be translated quickly into the actual model.

# CAD (Fusion 360)

>[!tip] Laser-Cut Body Frame Design 
![Assets/DinoBody2023.png](/img/user/Assets/DinoBody2023.png)


# 