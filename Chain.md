---
layout: default
title: Chain
nav_order: 5
---

## Quick Start

* Drag And Drop VFX Prefab from the "CompleteEffectsPrefabs" folder into your scene.
* Locate the "Chain Points" array variable in the C# script and assign a minimum of 2 transforms.
* Assign an "Auto Scale Anchor" transform, this transform will be used for scaling the effects.
* It is recommended to make the VFX connecter to chain points, you can make each of these points a child of VFX, or vice versa.
* You can check where the points are by enabling the "Preview Chain Points In Editor" parameter.
* With Auto Scale Enabled you can adjust the "Auto Scale Mulriply" or "Master Scale" to scale the VFX Elements.
* After all the above, you can now freely move and scale your mesh.

![s20](/assets/images/11.png)

Most of the additional adjustments come from the Visual Effects Graph parameters and C# script. Many parameters can be changed, you can control the color, speed, overall shape of the strips, noise scale, etc.

### Common Adjustments

* **(Scale)** If AutoScale is enabled, the way you can scale the VFX elements is to just scale the Anchor. The other way is to adjust the "Master Scale" parameter.
* **(Color)** Color can be changed in the Visual Effects Graph parameters. It is separated between each effect element. There is also a master color, so you can set all the element color parameters to white and change the master color to find the right hue.
* **(Speed)** The Speed at which the effect is triggered can be controlled in the C# script, check the "Speed" parameter.

### List Of VFX Graph Parameters

![s20](/assets/images/03.png)

* **Sparks Local Enabled** - Makes the sparks to be spawned in each point Local Space.
* **MASTER** -  These parameters serve as a final layer of adjustments, they just multiply existing parameters by themselves.
* **Dissolve Noise** - Use Dissolve instead of a regular alpha decay for lightning strips.
* **Lightning** - This set of parameters controls the color, gradient transitions, and emission power of VFX elements.
* **Ramp** - Uses the gradient Ramp texture for coloring.
 
Strips:
* **Strips Texture** - Main texture for lightning strips.
* **Strips EoL** - Emission Over Lifetime.
* **Strips SAoL** - Size and Alpha Over Lifetime.
* **Strips UV Stretch and Center UV** - Stretching the UV, and the other parameter is used to center the lightning strips at the Start and the End points.
* **Strips To Center** - Using the "Center UV" helps texture to adjust the UV of the lightning strip, making it more visually pleasing.
* **Strips Noise** - Controls the Offset Noise that makes lightning look like lightning.
* **Strips Noise PoL** - Noise Power (Offset Intensity) over Lifetime.
* **Strips NPoL** - Noise Position over Lifetime.
* **Strips V Mask** - Procedural Mask, used when the Strips Texture is empty to smoothen the edges.

Hit:
* **Hit Texture** - Main texture used for hit effects.
* **Hit SoL** - Size over Lifetime.
* **Hit EoL** - Emission over Lifetime.
* **Hit Move To Camera Fix** - Moves the hit quad sprite in the direction of a Camera. Useful to adjust the world geometry intersection of screen space quads.

Hi3 is a spherical explosion, I apologize for the inconsistent naming:
* **Hit3 SoL** - Size over Lifetime.
* **Hit3 OoL** - Opacity over Lifetime.
* **Hit3 EoL** - Emission over Lifetime.

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

Branched Arc:
* **Branched Arc Offset** - Set of parameters, controlling the vertex offset of lightning arc effect
* **Branched Arc Probability** - Probability for spawning lightning arc for each tick.
* **Branched Arc Noise And Transparency Masks** - Masks used to control noise intensity and transparency along the strip length.

Other Parameters:
* **Sparks2** - Various parameters to control the size and physical properties of Spark effects. Most parameter names are self-explanatory.
* **Transition** - Add a small touch to a lightning strip, making it appear more solid at the start and end points.
* **Disable Parameters** - These are used to disable some parts of VFX, that are not needed.
* **HIDDEN Parameters** - VFX Graph Won't allow hidden parameters to be changed from outside, so these are currently visible, don't change them.

### List Of C# Script Parameters

![s20](/assets/images/12.png)

* **Preview Chain Points In Editor** - Use this to preview the Cell Gizmos in the Editor to adjust the Cell Sizes.
* **VFX Enabled** - This System may be smoothly turned on or off, instead of setting speed to 0, you can just change this bool.
* **Chain Points** - Array of transforms, used to generate chain point positions.
* **Master Scale** - Act like the previous parameter, it scales the VFX elements, I just separated these two for visual clarity.
* **Auto Scale Enabled** - Enabled the AutoScale mode, it is recommended to turn this on at all times.
* **Auto Scale Anchor** - Anchor used to drive the AutoScale of the VFX.
* **Auto Scale Multiply** - Multiply the Auto Scale but this value.
* **Min Number Of Main Strips** - Set the min and max count of spawned Lightning Strips.
* **Man Number Of Main Strips** - Set the min and max count of spawned Lightning Strips.
* **Bonus Branch Probability** - Probability to spawn an additional lightning strip.
* **Speed** - Speed in which the VFX and Raycast are triggered.
* **Speed Variation** - Speed variation curve, to make the VFX appear more natural.
* **Speed Variation Time** - Displayed Variation Time, useful for very dynamic Variation Time curves.
* **Speed Variation Time Speed** - Speed in which Time Variation is changing.
* **Random Branched Circle Min Radius** - Branched strips are triggered using Sphere Raycast, these parameters control min and max radius.
* **Random Branched Circle Max Radius** - Branched strips are triggered using Sphere Raycast, these parameters control min and max radius.



### Support email: sinevfx@gmail.com
