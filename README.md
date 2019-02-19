# twb_gazebo

Simulation with TeleWorkBench model and 5 Jai Spark 5000{m/c} cameras.

* starting:
* * TWB-World ```roslaunch twb_gazebo twb.launch``` 
* * Gazebo-Models ```roslaunch twb_gazebo gazebo_models.launch``` 
* * TWB-World with Gazebo-Models ```roslaunch twb_with_gazebo_models twb.launch``` 


# gazebo_models

Models for Gazebo. Tested with Gazebo 7.

Most of the original resources are exported from Blender to .obj and .mtl files and then converted to .dae using Meshlab.

To use the models in Gazebo you have to add this folder to your path, e.g. `GAZEBO_MODEL_PATH="PATH/TO/gazebo_models:$GAZEBO_MODEL_PATH" gazebo`, or copy the models into a folder that's in your `GAZEBO_MODEL_PATH`.

Some resources are not allowed to be redistributed. Therefore the `download-resources.sh` scripts downloads them from their respective sources.

## Steps to reproduce (for office_desk)

1. Export model from Blender v2.78c to .obj.
2. Open in MeshLab v1.3.2
3. Filters -> Texture -> Parametrization: Trivial Per-Angle (you may need to increase Texture Dimension)
4. Filters -> Color Creation and Processing -> Transfer Color: Face to Vertex
5. Filters -> Texture -> Vertex Color to Texture (Check 'Assign texture')
6. File -> Export Mesh As... : .dae file (You should see the texture in the right list.)
7. Done

## Steps to reproduce (for desk set)

1. Export model from Blender v2.78c to .obj. Set 'Forward' to 'X Forward' and 'Up' to 'Z Up'. Check 'Selection only', 'Triangulate Faces'.
2. Open in MeshLab v1.3.2
3. Filters -> Texture -> Parametrization: Trivial Per-Angle (you may need to increase Texture Dimension)
4. Filters -> Color Creation and Processing -> Transfer Color: Face to Vertex
5. Filters -> Texture -> Vertex Color to Texture (Check 'Assign texture')
6. File -> Export Mesh As... : .dae file (You should see the texture in the right list.)
7. Done


## Original resources

- [Office desk](http://www.blendswap.com/blends/view/66643) ([CC-BY-SA](https://creativecommons.org/licenses/by-sa/3.0/) aditiapratama)
- [Desk set](http://www.blendswap.com/blends/view/14877) ([CC Zero](http://creativecommons.org/publicdomain/zero/1.0/) MattMump)
- [PET soft drink bottle](http://www.blendswap.com/blends/view/69117) ([CC Zero](http://creativecommons.org/publicdomain/zero/1.0/) tastykle3d)
- [Herman Miller Ergon 3 Work Chair](https://3dwarehouse.sketchup.com/model/uf86c8d78-97aa-4920-a1ef-e76999a30b3a/Herman-Miller-Ergon-3-Work-Chai) ([3D Warehouse: General Model License Agreement](https://3dwarehouse.sketchup.com/tos.html#license))
- [Simple hand rig](http://www.blendswap.com/blends/view/75824) ([CC-BY](http://creativecommons.org/licenses/by/3.0/) UP3D)
- [Lcd_Monitor](http://www.blendswap.com/blends/view/68813) ([CC-BY](http://creativecommons.org/licenses/by/3.0/) bheema)
- [Computer mouse](http://www.blendswap.com/blends/view/61128) ([CC-BY](http://creativecommons.org/licenses/by/3.0/) neogen22)
- [USB plug](http://www.blendswap.com/blends/view/82995) ([CC-BY](http://www.blendswap.com/blends/view/82995) LucasPL)
- [Light Wood Texture](http://www.publicdomainpictures.net/view-image.php?image=26031&picture=light-wood-texture) ([CC Zero](http://creativecommons.org/publicdomain/zero/1.0/) Petr Kratochvil)
- [Modern Office Chair](https://www.blendswap.com/blends/view/73454) ([CC-BY](https://www.blendswap.com/blends/view/73454) MLDP)

## Links

- [Working With Meshes in Gazebo](https://github.com/ethz-asl/rotors_simulator/wiki/Working-With-Meshes-in-Gazebo)
