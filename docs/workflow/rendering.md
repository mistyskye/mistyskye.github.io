---
layout: default
title: Rendering
nav_order: 6
parent: Workflow
---

# Rendering
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

## Shortcuts

| Shortcut | Info |
|--|--|
| Ctrl + 0 |  to assign selected camera as render camera|
|F12| to Render image|
|Ctrl+F12| to Render animation|

## Settings
My settings are the following:
### Render Properties:
- `Render Engine`: `Cycles` (you can use Eevee but this will change other available settings).
- `Device`: `GPU Compute` if you have a better GPU than CPU.
- `Sampling`: increase the `Render sampling` if you want.
- `Denoising`: check `Render` and select `OptiX` if available.
- `Film`: Check `Transparent` if you need transparent backgrounds.
- `Performance`: `Tiles`: increase to 256px.
- `Color Management`: make sure `View Transform` is set to `Standard`.

### Output Properties:
- `Dimensions`: `Resolution` X and Y: 2048 px.
- `Output`: File format: `PNG` for images, `PNG` or `FFmpeg` for animations .
	- PNG animation frames will have to be stitched back together later but if Blender crashes during rendering, you won't lose the already rendered frames.

## Stitching PNG sequence to video
- File > New > Video Editing.
- In the Sequencer, click `Add` > `Image/Sequence`.
- Select all your PNGs (press `A` to select all) (this step is skipped for privacy reasons in the gif below).
- On the right, open Transform and set the `Scale` X and Y to 1.
- Change the `Dimensions` to fit, and the n. of frames.
- In `Output` choose `FFmpeg`.
- Render Animation (`Ctrl+F12`) (you can use Eevee for this).
![](/assets/gif/rendering-png2vid.gif){: .center-image}

## Turnaround camera
Using the inbuilt add-on [Animation: Turnaround Camera]({% link docs/addons.md %}): 
- Add a camera.
- Select an object to be the focus of the camera.
- Go to `N` panel > `Animate`.
- Change the `End frame` (you can set it lower, somewhere between 60 and 150 for example).
- Click `Turnaround`.
- In Output properties, you can keep PNG or switch to FFmpeg if you don't want to have to stitch together the PNGs afterwards.