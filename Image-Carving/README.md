# Image Carving
The goal of this project is shrinking the image while preserving the integrity of critical image information.

First, compute energy map by:

![equation](https://latex.codecogs.com/gif.latex?E&space;=&space;\left&space;|&space;\partial&space;I&space;/&space;\partial&space;x&space;\right&space;|&space;&plus;&space;\left&space;|&space;\partial&space;I&space;/&space;\partial&space;y&space;\right&space;|)

Second, or each pixel, calculate cumulative minimum energy ![equation](https://latex.codecogs.com/gif.latex?\small&space;M_x).

![equation](https://latex.codecogs.com/gif.latex?\small&space;M_x(i,j)&space;=&space;E(i,j)&space;&plus;&space;min&space;\left&space;\{&space;M_x(i-1,j-1),&space;M_x(i-1,j),&space;M_x(i-1,j&plus;1)&space;\right&space;\})

Last, the end of the minimal connected vertical seam resides right at the minimum value of the last row in ![equation](https://latex.codecogs.com/gif.latex?\small&space;M_x). And then, backtrack all the way up from this minimum entry on ![equation](https://latex.codecogs.com/gif.latex?\small&space;M_x) to the first row in ![equation](https://latex.codecogs.com/gif.latex?\small&space;M_x) to find the path of the optimal seam.

<p align="center"><i>Original Image</i></p>
<p align="center">
<img src="waterfall.png" height="327">
</p>
<br>
<p align="center"><i>Intermediate Images</i></p>
<p align="center">
<img src="carving_waterfall.png">
</p>
<br>
<p align="center"><i>Shrinked Image</i></p>
<p align="center">
<img src="carved_waterfall.png" height="327">
</p>
