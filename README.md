# Devboard

Welcome to the open source repository for a custom designed RP2040 Devboard, with GPIO headers and a USB A port.
This product has a USB-A port and lots of GPIO Headers, for input, ooutput, grounding etc.  
This guide and the files are open source and completely free to distribute, use, or modify but you are not allowed to sell these files.
Discaimer: This project most likely has lots of bad practices and things that are wrong, please do not trust this project blindly. I am just a beginner making projects.
Please confirm that everything checks out and I am not liable for any problems with this project.  
I have made this to the best of my ability and there may be mistakes.  
Please make an issue in the tabs above for any problems you find.  
This guide will only show you how to order online and how to modify this proejct for yourself but not soldering or printing yourself since even I do not know how to do these.  
  
  
## Files
1. PCB.zip is a gerber file which is going to be used to tell the Manufacturing service how the PCB should be made.
2. Enclosure.obj is an object file which is a 3D Model and it is going to be used to 3D Print the Enclosure.
3. Source.epro is the PCB source file for any further modifications that you would want to do.
4. Model.blend is the Blender source file for any further modifications that you would want to do.
  
 
  
  
## Modification
This part of the guide is going to be divided into two parts.  
1. The PCB
2. The Enclosure
  
First of all we are going to start with how you can modify the PCB.  
1. First of all, these PCB files are meant for EasyEdaPro and if you are using other software, please check if these files work with your software.
2. Now, you can head to [EasyEdaPro](https://easyeda.com/) and make an account or login.
3. Then you can click Design Online and then Pro edition since it is a lot easier.
4. Now you can click File -> Import -> EasyEDA(Standard).
5. Now you can select Source-Project.epro which will give you the option to modify and change the Schematics and the PCB.
6. Some things you can add are lights for when a usb is plugged in, Add more Ports, or upgrade the ports from USB 2.0 to 3.0.
7. After you are done modifying, You can press Check DRC in the bottom tab.
8. If there are any things that pop up in the DRC zone, that means there is an error. You can search online, use AI to fix these, or use your brain to fix these.
9. Now we need to export the files in Gerber Format so that we can order the PCB.
10. For exporting, press File -> Export -> PCB Fabrication File (Gerber) -> Export Gerber -> No, continue exporting.
11. Now you have your Gerber files which are the same as PCB.zip but include your changes (you can use these files instead of PCB.zip, i mean).
  
Now we are going to do the Enclosure
1. Warning, I used Blender to design this enclosure which is not the standard, it might not be even meant for this use.
2. First you can go to Blender, press
3. If you have modified the size of the PCB, please continue reading, if not please skip to Step 9.
4. Now, you will need to import the PCB into this blender project so that you can fix the size according to the PCB.
5. For this, in EasyEda pro, you can go ahead and press File -> Export -> 3D File.
6. Now you can press OBJ and then export.
7. Back in blender, you can press File -> Import -> Wavefront(.obj) and select this file.
8. Now you have the PCB inside blender so you can make the measurements.
9. After you are done modifying the Enclosure, you can position both Base, Lid and any other parts that you have, Flat side down at the same height.
10. Please just check that these things are alright (Manifolds, Geometry, Normals, and Scale).
11. To check if everything is Manifold / Watertight, select all the Enclosure Meshes (not the PCB) and go to edit mode.
12. Once There, Go to Select underneath the Ribbon with File and Edit, then press Select All by Trait, and then Non-Manifold.
13. If Anything is highlighted, please fix it here.
14. To check that there is no loose geometry, select all the Enclosure Meshes (not the PCB) again and go to edit mode.
15. Once there, Go to Select underneath the Ribbon with File and Edit, then press Select All by Trait, and then Loose Geometry.
16. If anything is highlighted, please fix it here.
17. To check for Internal Faces, Press Z and Wireframe in Object mode.
18. Check if there are any faces inside the Meshes.
19. Then Press A -> M -> By Distance.
20. Now, in Object mode, you need to go to the circles at the top right of the viewport, there are two overlapping circles near it, press the circles and then enable Face Orientation.
21. Everythings should be Blue, if anything is red, You need to flip it,
22. To Flip any Faces, Go to Edit Mode, Select the Face and press Shift + N, and then Flip.
23. Do this for all red Faces.
24. If you have used any Booleans, Mirrors, or even Unions, Apply the Booleans, and try to fix the self-intersections, if not possible, rebuild the area or search for different ways to make that part.
25. Finally, just make sure your Project is set to millimeters in Inspector -> Scene -> Units -> Length -> Millimeters.
26. Now you are done checking your model for problems.
27. Then you can delete any things that you do not need, and then press File -> Export -> Wavefront(.obj) and save the file
28. Now this file is basically Eclosure.obj but with your modifications, you can use this instead of Enclosure.obj.

