https://user-images.githubusercontent.com/50581102/168311846-fbde9eaf-d8be-42dd-8546-99ec5464ac20.mp4

# VDB to Density Mask
A **Houdini** template file that converts meshes to VDB, outputs volume texture and composites it into **Unity's HDRP** density mask texture.

# Versions supported
Unity: **2019.4**, **2020.3**, **2022.1+** (3D texture support is required)

Houdini: **19.0+**

# How to use

1) Open **VDBConverter.hip**
2) Open **VDBConverter** geometry node and plug your mesh in. Avoid large meshes for better performance, keep scale within 10 Houdini units. 
3) Open **Process3DTexture** COP network, select Output node and hit render. If you have changed Volume Texture dimensions, select sppimport1 node and click Set Resolution From SOP
4) Import texture to Unity
5) Prepare the texture: **Set shape to 3D**; **Set rows and columns**; **Set Wrap Mode to Clamp**; **Set Format to RGBA 32 bit**
6) Plug your texture in Local Density Mask Texture

https://user-images.githubusercontent.com/50581102/168315250-f6d5731b-ea98-4416-b044-1e56e460d5ce.mp4

