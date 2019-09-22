---
layout: post
title: How to convert an Allegro .brd PCB to Altium .PCBDoc File
bigimg: img/post-allegro-altium/allegro-altium.png
layout: post
tags: [allegro, altium-designer]
---


I came up with this task while trying to import  .brd files hosted by Analog Devices into my Altium Designer. I only got the .brd no other files from the project. But importing the layout at least gave me the footprints of the components which saves a lot of time. However, following the instructions by the [Altium Designer documentation](https://www.altium.com/documentation/18.1/display/ADES/((Allegro+Import))_AD) was not successful to me. The problem was that Altium Designer needs the **extracta.exe** from OrCAD/Allegro PCB editor.

As a workaround I downloaded a [free trial version from OrCAD](https://www.orcad.com/free-trial) which is limited to 15 days. After the installation of the trial version make sure to add the path of **extracta.exe** ( C:\Cadence\SPB_17.2\tools\bin\) to the environment variables of your windows system otherwise Altium can’t find the the **extracta.exe**.

I tried to use the import wizard for Allegro .brd files which comes with Altium Designer 18, but it failed despite the fact that I run an Intel I9 with 32Gb RAM…. But using the instructions form the Altium Designer documentation finally worked for me.

Copy the files **Allegro2Altium.bat** and **AllegroExportViews.txt** located in the Altium installation path (C:\Program Files\Altium\AD18\System) into the project folder containing the example.brd  (Allegro binary format).
Run the CMD command in the explorer of your project folder to open a terminal.
Run the command **Allegro2Altium.bat example.brd** to start conversion from .brd format to .alg (ASCII format)
Run the Altium Designer import wizard for Allegro and start importing the example.brd.alg file.
This generated me a .PcbDoc file hopefully it also works for you 🙂
