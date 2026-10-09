# Sharp-EA-129C-Clone
DIY clone of the Sharp EA-129C cable to connect two Sharp 11-pin pocket computers

# Connecting Sharp Pocket Computers

Sharp had released a cable to connect their pocket computers of the serier PC-12xx, PC-13xx, PC-14xx to transfer programs and data between two of these machines via the CLOAD and CSAVE commands, the Sharp EA-129C. Nowadays these cables are very rare and subsequently quite expensive. 

Fortunately the cable is no rocket science and can be easily self confected. As the CLOAD and CSAVE mechanisms are used, basically three connections are necessary. Ground (**pin 3** of the 11 pin connector) is directly routed from one pocket computers IO-connector to the other. The other two lines used are of course the pins 6 (XIN) and 7 (XOUT) of the 11 pin connector. These two contacts need to be cross cabled. So **pin 6 on one side goes to pin 7 on the other side** and **pin 7 on one side goes to pin 6 on the other side**. That's all, so begging to become a DIY project.

There are now two options, one is to patch these connection each time you need them with these breadboard connector cables (male-male). So more or less a quick and dirty workaround. The option i am targeting is to create a more or less professional cable with real plugs and not too much cable length.

## Housing for the Cable Plugs

As i own a 3D printer but unfortunately have almost no skills in 3D design with a CAD software, i decided to make use of Gemini AI to create the housings for the plugs. The results are one FreeCAD file and two STL files. 

The pin pitch of Sharp's 11-pin connector is 2.54mm (1/10th of an inch), which is pretty much standard for Arduino/ESP32 headers. So i cut two of these headers down to 11 contacts. 

The 11 pin header has to be glued into the lower part of the housing. There is enough space inside, so solder the three wires. I created two electrical versions, one with 51K resistors on pins 6 and 7 and one without. The resistors are only on one side.

I used a cable with a diameter of 4mm, so the channel for the cable also has a 4mm diameter. As the FreeCAD file is included in the package, you may want to change it according to your needs.

My recommendation is to use PETG and not PLA. PETG is more stable for that purpose. Also make sure to use a layer hight of 0.12mm. My printer is a BambuLab P2S with a 0.4mm nozzle. Also print with supports.

The lower part of the housing is 5mm high, the upper part is 3.5mm high. 

## Materials

The 3D printed housing is already mentioned. For each housing you also need 2 tiny screws to hold the two parts together. The design works perfekt with **M2x6mm** cylinder head screws.

The 11 pin connector is a simple **2.54mm pitch header bar** which are used for Arduino etc.

The cable i used wasn't a special purchase. I was just in my drawer for cables. The diameter is 4mm, you need a minimum of **three wires** in your cable. My cable does not have a shielding. As it works, i would say you might not need a cable with shielding, however, i 

I used **two component glue** to fit the header bar into the lower part of the housing.

**Optionally** you can put **two 51K 'til 100K resistors** onto the bill of material. But really these are optional. See later in text. 

## Soldering

Before i started soldering the wires to the header i glued the **header bar into the lower part** of the housing. That makes handling easier. Be 100% sure that you cross cable pins 6 and 7! 

The pins 3 of both sides just need to be connected directly as this is the ground wire.

## Final Assembly

After soldering the wires you might want to test your soldering knowledge and transfer a program before you assemble the top part of the housing with the two screws. If you trust your soldering knowledge, just put the top onto the bottom part and fix the two screw.

One comment here: you may want to fix the cable into the housing. Use glue, cable ties, whatever you think is appropriate to keep the cable inside.

## License

Copyright (c) 2026 Christian Becker

This work is licensed under the Creative Commons Attribution-NonCommercial 4.0 International License.
To view a copy of this license, visit http://creativecommons.org/licenses/by-nc/4.0/ 
or send a letter to Creative Commons, PO Box 1866, Mountain View, CA 94042, USA.


## Famous Last Words

Somewhere in the internet i found an article stating that it might be useful to add a resistor to each of the data lines. As already mentioned, i created two versions, one with, one without resistors. I used **SMD 0603 51K** resistors as they were avaialable (see picture *EA-129C_with_resistors.jpg*). A bit bigger won't be the worst decision. If you just want to transfer from one type of pocket computer to the same type of pocket computer, i won't create a version with resistors. The original EA-129C does not have any resistors inside.

In the "Images" subfolder you'll find some pictures of my build and final product. I also added a "wiring diagram" to make clear, how the soldering must be done (if that is not already very clear).

I hope i did not forget important parts in this readme. Have fun!




