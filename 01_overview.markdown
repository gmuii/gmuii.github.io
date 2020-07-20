---
layout : page
title : Overview
permalink : /overview/
---

The NAME is a dataset specialized for Copy-Move forgeries. It contains 
automatically generated tampered ID documents. 
At the time of writing, a base of 304 documents were used to produce 893 tampered images.
Those number might evolve over time but the structure will stay the same.
There will be one tampering only per images, and no post-processing were
applied.
The following section will give a brief overview of the dataset.

<h2>Structure</h2>

The dataset is decomposed into three main folder. The ***ref***, ***gt*** and ***tampered*** folders.
The ***ref*** folder contains the pristine images used to produce the forgeries, the ***gt*** folder contains
the ground truth binary mask and the ***tampered*** folder contains the tampered images.

<h1>Ref folder</h1>

Inside the ***ref*** folder, images will be named following this convention  :

***NAME_X***

With ***NAME*** being an ID document identifier such as ***BEL_P_N*** for the national belgium passport. 
And  ***X*** a numerical index (starting from 0) representing a unique photo of one ID document.
One ID document can be present multiple times in the dataset. For example, if there were 18 pictures of 
the national belgium passport. Then, the 5<sup>th</sup> image of this document will be named :

***BEL_P_N_4***

<h1>Ground  truth and tampered folders</h1>

Inside the ***tampered*** folder, images will be named following this convention : 

***NAME_X_Y***

With ***NAME_X*** the name of the reference image used. And  ***Y*** a numerical index (starting from 0)
representing a unique tampering of image ***NAME_X***.

Inside the ***gt*** folder, the binary mask will have the same name as the tamperd images. 
So for the tampered image ***tampered/BEL_P_N_2_1.png***, the corresponding binary mask
will be find at ***gt/BEL_P_N_2_1.png***.


<h1>Ground truth format</h1>

The ground truth masks will be provided as **RGB** images to allow source/target identification.

The localisation of the source element will be in the green channel and the localisation of the target 
will be in the red channel. The blue channel will always be empty (i.e. filled with zeros).

![Example of tampering](/img/example.jpg)

On the above example, we can see the tampered image on the left and the ground truth mask on the right. 
The mask indicates that the caracter at the location of the green patch has been copy and move at the red
patch location.


