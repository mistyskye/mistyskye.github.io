---
layout: default
title: Shapekeys
nav_order: 6
parent: Workflow
---

# Shapekeys
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

## Introduction
Shapekeys are mesh changes that work off a base, unchanged mesh. Each shapekey basically saves a new position change for each vertex. This is why the Basis shapekey is important: every other shapekey will be relative to the Basis.  

If you're working on a head, you will need to apply your mirror modifier before proceeding.
You can turn on Symmetry (!= mirror modifier!) while working on shapekeys. If the symmetry looks broken, select all (`A`) > `F3` > type `Snap to symmetry`.
You can keep modifiers such as subdivision, but you will need an add-on to apply them and keep your shapekeys. There are various add-ons that have a function for this such as gret, Faceit and other standalone add-ons.

## ARKit (iPhone) shapekeys
### Faceit
I use Faceit to make iPhone ARKit tracking shapekeys. You can use it to align features on your model's face and it will attempt to create the 52 iPhone shapekeys. They are not always great on stylised heads, and I end up remaking most of them but it takes care of the creating and naming step for me. It also keeps them in the same order throughout all my models which is helpful in Unity.

### Shapekeys+
Using Shapekeys+, you get easy access to existing and extra shapekey functions. For example, to copy and mirror a shapekey, just click and hold on the Copy icon and click `Copy Shape Key, Mirrored`.

![](/assets/img/shapekeys-copy-mirror.JPG){: .center-image}

You can also choose where newly added shapekeys appear, and move shapekeys to the top or bottom with one button.

### Testing in Blender
You can learn how iPhone tracking shapekeys work, fix mistakes and test everything all together by using the iFacialMocap add-on for Blender.
You can find the tutorial [here](https://www.ifacialmocap.com/tutorial/blender/). Make sure you set the correct `FaceObjectsName`, and remove the `HeadBone` name if you don't want the head to move in Blender (it reduces lag). If you have different parts in different objects, you can parent them to the Head object in Blender, and just set the Head's object name to `FaceObjectsName`.

### Resources
There are various resources to learn each ARKit shapekey:
- [https://arkit-face-blendshapes.com/](https://arkit-face-blendshapes.com/)
- [Ocuuda has some great resources](https://ocuuda.carrd.co/#resources)