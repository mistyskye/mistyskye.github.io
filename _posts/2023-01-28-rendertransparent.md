---
layout: post
title:  "Rendering transparent"
excerpt_separator: <!--more-->
tags: ["render", "blender"]
---

# Rendering a transparent video using Blender

This is a quick step-by-step guide on how to render an animation with a transparent background using Blender.
<!--more-->

1) Render Properties > Film > Transparent.

2) Render an animation as a PNG sequence with **RGBA**.

3) Open a new Blender project with the Video Editor preset.

4) Click Add > Image sequence and add your PNG images.

5) Set the correct frame duration.

6) Set the resolution, FPS etc.

7) Set File format to `FFmpeg Video`.

8) In Encoding, set the Container to `Quicktime`.

9) In Encoding > Video, set the Video Codec to `QT rle / QT Animation`.

10) Scroll back up to just below the File Format and select RBGA.

11) Render Animation.

{: .note }

In Blender Video Editor, if the scale of the video is too small:
Bottom tab > Transform > set Scale to 1.