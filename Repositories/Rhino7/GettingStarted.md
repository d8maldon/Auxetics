[TOC]

# Rhino 7 Tutorial Notes

What is Rhino 7?
- A software that allows the user to create, edit, analyze, document, render,
  animate: surfaces, solids, subdivided geometries, polygon meshes and lots more
- It costs money, but there is a student/teacher discount
- There is also a 90 day free trial
  + After the free trial you can still use the software but are no longer able
  to save anything that you create
- Download Link: https://www.rhino3d.com/download/

What is Grasshopper?
- It is a parametric modeling tool.
- Grasshopper comes with the installation of rhino and it is beneficial since
  since there are many plug-ins that can be used in grasshopper. There is a
  community of people who make lots of plugins: https://www.food4rhino.com/en


How do grasshopper and rhino work together?
- With grasshopper you can change the parameters of the structure
- The tunable parameters can be whatever it is that you define them to be.
- You can see the changes that are made in real time in the Rhino window
- With the tunable parameters you are also able to make an animation

Why is this relevant to auxetics?
- Can visualize the Auxetics in 3D space with different view points
- Allow generation of .dxf files that can be sent  to the laser cutter for manufacturing.
- Has base auxetic cells that can be used to make auxetic structures.


### Plugin
___
Plugin and Paper can be found: https://lgg.epfl.ch/publications/2021/Bass/index.php

What Works?
- Both (aux_cell and bass_cell) builder cells work independently
- Creating a .dxf file from the created structures also works.
- Deployment % slider
  + The slider shows how the structure "will behave" from its undeployed state
  to the deployed state.

Issues with generation_aux_bass file
- Case sensitivity:
  + Mismatch in the capitalization of the word DBPath, this is something that
  needs to be fixed to get the deployable tunable parameters to work.
- Float is can not be iterated
  + Issue in the genPattern function : /
  + This issue impacts the 2021 part of the plugin. I will be emailing the creators if they have
  an updated version of the plugin that will hopefully be less buggy
- In generation_aux_bass there is a parameter that can be changed for the type of auxetic cell that you
  want to use for the auxetic structure.

### Common "Issues" and Fixes
- Issue: The preview of the auxetic structure disappears:
- Fix: You have to click on the preview block so that the structure is displayed in the rhino window

- Issue: When exporting .dxf files there is sometimes additional lines included in the file.
- Fix: This is because in the 2D the there are overlapping surfaces which result in these lines.
To fix this issue what you need to do is select everything and run the command extract wireframe. Then
you can click on the wireframe there will be a prompt of surfaces and curves, you delete all the surfaces.


```
Location Of The Libraries [Just for me (Daniel) to know where the directory is since I keep forgetting]
C:\Users\maldo\AppData\Roaming\Grasshopper\Libraries
```


### Suggestions from Delsin Demo
___
- Creating labels on the blocks in grasshopper that are used to visualize the structure
- Creating like common issues and fixes section
