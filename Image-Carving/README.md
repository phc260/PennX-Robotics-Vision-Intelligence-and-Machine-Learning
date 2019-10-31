# Image Carving
The goal of this project is shrinking the image while preserving the integrity of critical image information.

1. Compute energy map by:

![equation](https://latex.codecogs.com/gif.latex?E&space;=&space;\left&space;|&space;\partial&space;I&space;/&space;\partial&space;x&space;\right&space;|&space;&plus;&space;\left&space;|&space;\partial&space;I&space;/&space;\partial&space;y&space;\right&space;|)

2. For each pixel, calculate cumulative minimum energy ![equation](https://latex.codecogs.com/gif.latex?\small&space;M_x)

![equation](https://latex.codecogs.com/gif.latex?\small&space;M_x(i,j)&space;=&space;E(i,j)&space;&plus;&space;min&space;\left&space;\{&space;M_x(i-1,j-1),&space;M_x(i-1,j),&space;M_x(i-1,j&plus;1)&space;\right&space;\})

3. The end of the minimal connected vertical seam resides right at the minimum value of the last row in ![equation](https://latex.codecogs.com/gif.latex?\small&space;M_x). And then, backtrack all the way up from this minimum entry on ![equation](https://latex.codecogs.com/gif.latex?\small&space;M_x) to the first row in ![equation](https://latex.codecogs.com/gif.latex?\small&space;M_x) to find the path of the optimal seam.



<img src="waterfall.png" height="327">
        Original Image


<img src="carving_waterfall.png">
        Intermediate Image



img src="carved_waterfall.png" height="327">
        Shrinked Image


