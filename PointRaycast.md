---
layout: default
title: Point Raycast
nav_order: 2
---

## Quick Start

Drag And Drop VFX Prefab from the "CompleteEffectsPrefabs" folder into your scene. Enable the "Preview Gizmos In Editor" bool in the attacked C# script to see the range of the effect. Now you can adjust various parameters to match your project design. There are two modes for this System, Spherical, and Cone. Check the list of the adjustable parameters below.

Most of the adjustments come from the Visual Effects Graph parameters and C# script. Many parameters can be changed, you can control the color, speed, overall shape of the strips, noise scale, etc.

### Common Adjustments

* **(Scale)** To scale the effect after dropping it into your scene you can adjust the "Max Distance" parameters. The effect elements will be scaled too, because by default "Max Distance Auto Scale" is enabled.
* **(Color)** Color can be changed in the Visual Effects Graph parameters. It is separated between each effect element. There is also a master color, so you can set all the element color parameters to white and change the master color to find the right hue.
* **(Speed)** The Speed at which the effect is triggered can be controlled in the C# script, check the "Speed" parameter.

### List Of VFX Graph Parameters

* MASTER -  These parameters serve as a final layer of adjustments, they just multiply existing parameters by themselves.
* Dissolve Noise - Use Dissolve instead of a regular alpha decay for lightning strips.
* Lightning - This set of parameters controls the color, gradient transitions, and emission power of VFX elements.

### List Of C# Script Parameters

* 



### Support email: sinevfx@gmail.com
