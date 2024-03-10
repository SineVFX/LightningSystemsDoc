---
layout: default
title: Introduction and Important Notes
nav_order: 1
---

## About the Asset

This Asset consists of 4 main Lightning Systems, constructed with a combination of C# script and Visual Effects Graph. Each system is slightly different in workflow, but overall they are pretty similar in terms of how they work. If you want to test the Effects right away, check the quick start pages for each system, they contain quick instructions on how to apply the VFX to your project.

![s20](/assets/images/01.png)

### Important Notes

* **(Engine)** Asset is using Visual Effects Graph, so it requires GPU Compute Shaders, however, Unity has plans to add CPU simulation

* **(HDRP)** VFX Prefabs for the HDRP version were built with Exposure set to 13.5. Change the Emission Power for darker scenes.

* **(HDRP, URP)** This VFX Asset looks much better in "Linear" Color Space, but if you using "Gamma" Color Space, you need to slightly decrease the Final Power (Emission Power) material parameter of each effect. You can check it in the "Edit > Project Settings > Player" TAB.
* **(HDRP, URP)** Image Effects are necessary in order to make a great-looking game, as well as our asset. Be sure to use "ACES Tone Mapping" and "Bloom".



### How To Use

* First of all, check the three scenes "DemoScene", "DemoSceneManualVFXSpawnExamples", and "DemoSceneUseCasesAndExamples" in the Scenes folder. The First one contains complete effect compositions. The second one contains an example of how you can call manual VFX Spawn functions for point and mesh Raycast systems. The third one contains various examples of how to use the effects.
* Read the corresponding docs page on each system to learn how to add the effects to your scene.



### Support email: sinevfx@gmail.com
