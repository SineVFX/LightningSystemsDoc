---
layout: default
title: Point Raycast
nav_order: 2
---

## Quick Start

* Drag And Drop VFX Prefab from the "CompleteEffectsPrefabs" folder into your scene.
* Enable the "Preview Gizmos In Editor" bool in the attached C# script to see the range of the effect.
* Now you can adjust various parameters to match your project design.
* There are two modes for this System, Spherical, and Cone. Check the list of the adjustable parameters below.

![s20](/assets/images/05.png)

Most of the adjustments come from the Visual Effects Graph parameters and C# script. Many parameters can be changed, you can control the color, speed, overall shape of the strips, noise scale, etc.

### Common Adjustments

* **(Scale)** To scale the effect after dropping it into your scene you can adjust the "Max Distance" parameters. The effect elements will be scaled too, because by default "Max Distance Auto Scale" is enabled.
* **(Color)** Color can be changed in the Visual Effects Graph parameters. It is separated between each effect element. There is also a master color, so you can set all the element color parameters to white and change the master color to find the right hue.
* **(Speed)** The Speed at which the effect is triggered can be controlled in the C# script, check the "Speed" parameter.

### List Of VFX Graph Parameters

![s20](/assets/images/03.png)

* **MASTER** -  These parameters serve as a final layer of adjustments, they just multiply existing parameters by themselves.
* **Dissolve Noise** - Use Dissolve instead of a regular alpha decay for lightning strips.
* **Lightning** - This set of parameters controls the color, gradient transitions, and emission power of VFX elements.
 
Strips:
* **Strips Texture** - Main texture for lightning strips.
* **Strips EoL** - Emission Over Lifetime.
* **Strips SAoL** - Size and Alpha Over Lifetime.
* **Strips UV Stretch and Center UV** - Stretching the UV, and the other parameter is used to center the lightning strips at the Start and the End points.
* **Strips To Center** - Using the "Center UV" helps texture to adjust the UV of the lightning strip, making it more visually pleasing.
* **Strips Noise** - Controls the Offset Noise that makes lightning look like lightning.
* **Strips Noise PoL** - Noise Power (Offset Intensity) over Lifetime.
* **Strips NPoL** - Noise Position over Lifetime.

Hit:
* **Hit Texture** - Main texture used for hit effects.
* **Hit SoL** - Size over Lifetime.
* **Hit EoL** - Emission over Lifetime.
* **Hit Move To Camera Fix** - Moves the hit quad sprite in the direction of a Camera. Useful to adjust the world geometry intersection of screen space quads.

Hi3 is a spherical explosion, I apologize for the inconsistent naming:
* **Hit3 SoL** - Size over Lifetime.
* **Hit3 OoL** - Opacity over Lifetime.
* **Hit3 EoL** - Emission over Lifetime.
* **Source** - Parameters to adjust the source Hit effects.

Main Strip:
* **Main Strip Lifetime and Hit Lifetime** - Lifetime in seconds of the Main Strip and Main Strip Hit effects.
* **Main Strip Profile** - Thickness profile of a lightning strip.
* **Main Strip Noise Mask Profile** - Profile that controls the amount of Offset Noise applied to a lightning strip.
* **Main Strip EoL** - Emission over Lifetime.
* **Main Strip AoL** - Alpha over Lifetime.
* **Main Strip B** - Parameters that control the overall shape and emission of the second and third Main Strips. The amount of Main Strips can be changed in a C# script, check the "Min and Max Numbers Of Main Strips" parameters.

Branched Strip:
* **Branched Lifetime and Hit Lifetime** - Lifetime in seconds of the Branched Strip and Branched Strip Hit effects.
* **Branched Profile** - Thickness profile of a lightning strip.
* **Branched EoL** - Emission over Lifetime.
* **Branched AoL** - Alpha over Lifetime.
* **Branched Start Min and Max** - Adjust the initial point from which the Branched Strip can be branched.
* **Branched Noise Blend** - Blends between Main and Branched Offset Noises, don't change too much.

Other Parameters:
* **Sparks2** - Various parameters to control the size and physical properties of Spark effects. Most parameter names are self-explanatory.
* **Transition** - Add a small touch to a lightning strip, making it appear more solid at the start and end points.
* **Disable Parameters** - These are used to disable some parts of VFX, that are not needed.
* **HIDDEN Parameters** - VFX Graph Won't allow hidden parameters to be changed from outside, so these are currently visible, don't change them.

### List Of C# Script Parameters

![s20](/assets/images/02.png)

* **Preview Gizmos In Editor** - Use this to preview Gizmos in the Editor to adjust the Max Distance.
* **Modes** - Two self-explanatory modes, Spherical and Cone.
* **Hemisphere Distance** - Exclude the possible Raycasts from a Spherical Shape.
* **Max Distance** - Maximum Raycast distance.
* **Max Distance Auto Scale Enabled** - Enabled the AutoScale based on the maximum distance, disable it if you want to scale the distance in real-time, but no the effect itself.
* **Max Distance Affected By Anchor** - Link the AutoScale to a Local Scale of a selected Transform.
* **Max Distance Anchor Multiply** - Multiply the Anchor AutoScale value.
* **Auto Scale Multiply** - Multiply the AutoScale value.
* **Cone Mode Circle Min Radius** - Minimum Radius of a frustum circle of a cone.
* **Cone Mode Circle Max Radius** - Maximum Radius of a frustum circle of a cone.
* **Maximum Number Of Attempts** - Control the number of failed Raycast attempts, use low value for better optimization.
* **Maximum Number Of Branched Attempts** - Control the number of failed Raycast attempts, use low value for better optimization.
* **Min Number Of Main Strips** - Set the min and max count of spawned Lightning Strips.
* **Man Number Of Main Strips** - Set the min and max count of spawned Lightning Strips.
* **Min Number Of Branched Strips** - Set the min and max count of spawned Lightning Strips.
* **Man Number Of Branched Strips** - Set the min and max count of spawned Lightning Strips.
* **Speed** - Speed in which the VFX and Raycast are triggered.
* **Speed Variation** - Speed variation curve, to make the VFX appear more natural.
* **Speed Variation Time** - Displayed Variation Time, useful for very dynamic Variation Time curves.
* **Speed Variation Time Speed** - Speed in which Time Variation is changing.
* **Random Branched Circle Min Radius** - Branched strips are triggered using Sphere Raycast, these parameters control min and max radius.
* **Random Branched Circle Max Radius** - Branched strips are triggered using Sphere Raycast, these parameters control min and max radius.



### Support email: sinevfx@gmail.com
