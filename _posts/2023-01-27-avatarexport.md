---
layout: post
title:  "Avatar Export"
excerpt_separator: <!--more-->
tags: export blender
---

# Avatar Export workflow

Generally, exporting avatars to Unity is tiresome, non-reproducible and destructive. I used to create a copy of my current blend file, apply all modifiers manually, select everything and export. If I had to change something in Blender, I had to go back into the original file, make my changes and then repeat the new file > apply > export cycle.

<!--more-->

--> Using Avatar builder and Better FBX Exporter addons

1) Create new Build settings (and name if you want).
2) Select all objects you want to export (including Armature) and click Add.
   - If everything is in a collection: right click the collection > Select objects.
3) Settings: 
   - Uncheck ignore hidden objects if you need some hidden things (such as toggles), or keep it checked and unhide everything you need.
   - Use Reduce to two meshes to keep model size down: shapekeys increase file size per vertex in the mesh so keeping them separate helps that.
4) In each object's Object Settings:
   - Head and anything with shapekeys: 
     - Change Modifiers > Apply modifiers to Apply with shapes (gret addon)
     - Vertex groups > uncheck Remove non-deform
   - Anything you want to keep separate for toggles or animating: 
     - Object > Check Ignore 'Reduce to two meshes'
     - Object > Change the Built name to the same name to join objects (such as all objects of a jacket to Jacket)
   - You can play with join order if the order of shapekeys and/or material slots is important to you. By default, leaving everything at 10 will mean that the object with the most shapekeys will be first.
5) Click Build Avatar.
6) Select everything, File > Export > Better FBX Exporter
7) FBX Exporter (you can set these as a preset top right for future exports):
   - Check Selected objects only
   - Scroll down and uncheck Ignore Armature Node
   - Name your FBX and press export
