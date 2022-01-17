# godot-kuwahara

This is a gdshader implementation of the [Kuwahara filter](https://en.wikipedia.org/wiki/Kuwahara_filter), tuned to produce an oil-painting aesthetic.
It is available as both a canvas_item and spatial shader.

## 2D Gallery

### Parliament Hill, Ottawa 
![](https://github.com/PeterEve/godot-kuwahara/blob/main/screenshots/ottawa_before.jpg)
![](https://github.com/PeterEve/godot-kuwahara/blob/main/screenshots/ottawa_after.png)
(https://commons.wikimedia.org/wiki/File:Tulip_festival_in_Ottawa_-_2019_(47925742658).jpg)

### Le Mont-Saint-Michel
![](https://github.com/PeterEve/godot-kuwahara/blob/main/screenshots/lemont_before.jpg)
![](https://github.com/PeterEve/godot-kuwahara/blob/main/screenshots/lemont_after.png)
(https://commons.wikimedia.org/wiki/File:Mont-Saint-Michel_vu_du_ciel.jpg)

### Dallol
![](https://github.com/PeterEve/godot-kuwahara/blob/main/screenshots/dallol_before.jpg)
![](https://github.com/PeterEve/godot-kuwahara/blob/main/screenshots/dallol_after.png)
(https://commons.wikimedia.org/wiki/File:The_hydrothermal_system_of_Dallol.png)

### Chateau de Chillon and Dents
![](https://github.com/PeterEve/godot-kuwahara/blob/main/screenshots/chateau_before.jpg)
![](https://github.com/PeterEve/godot-kuwahara/blob/main/screenshots/chateau_after.png)
(https://commons.wikimedia.org/wiki/File:001_Chateau_de_Chillon_and_Dents_du_Midi_Photo_by_Giles_Laurent.jpg)

## 3D Gallery
### Godot Third Person Shooter Demo
![](https://github.com/PeterEve/godot-kuwahara/blob/main/screenshots/third_person_demo_1.png)
![](https://github.com/PeterEve/godot-kuwahara/blob/main/screenshots/third_person_demo_2.png)
![](https://github.com/PeterEve/godot-kuwahara/blob/main/screenshots/third_person_demo_3.png)
![](https://github.com/PeterEve/godot-kuwahara/blob/main/screenshots/third_person_demo_4.png)
(https://godotengine.org/asset-library/asset/678)

## Notes
### Changing Kernel Size
The shader comes with 4 pre-made circular kernels to choose from: 3, 4, 5 and 6 pixels wide. The examples above were captured using the default 4 pixel kernel.
To use a different kernel size, rename at lines 15, 17 and 55.
The larger the kernel, the slower the shader.

### Use in Spatial Scenes
Follow the Full Screen Quad instructions found in [this](https://docs.godotengine.org/en/stable/tutorials/shading/advanced_postprocessing.html) tutorial.
The shader has undergone significant optimisation and should be able to achieve 1920x1080 60fps on any modern computer at the supplied kernel sizes.

### Modifications to the Basic Algorithm
* Circular kernels to reduce block artifacts
* Approximate standard deviation to improve performance 