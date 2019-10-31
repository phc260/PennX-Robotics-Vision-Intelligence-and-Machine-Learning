# Image Carving
The goal of this project is shrinking the image while preserving the integrity of critical image information.

First, compute energy map by:

![equation](https://latex.codecogs.com/gif.latex?E&space;=&space;\left&space;|&space;\partial&space;I&space;/&space;\partial&space;x&space;\right&space;|&space;&plus;&space;\left&space;|&space;\partial&space;I&space;/&space;\partial&space;y&space;\right&space;|)

Second, for each pixel, calculate cumulative minimum energy ![equatioin](https://latex.codecogs.com/gif.latex?M_x)
![equation](https://latex.codecogs.com/gif.latex?M_x(i,j)&space;=&space;E(i,j)&space;&plus;&space;min&space;\left&space;\{&space;M_x(i-1,j-1),&space;M_x(i-1,j),&space;M_x(i-1,j&plus;1)&space;\right&space;\})

<img src="waterfall.png" height="327">
<img src="carving_waterfall.png">
<img src="carved_waterfall.png" height="327">
