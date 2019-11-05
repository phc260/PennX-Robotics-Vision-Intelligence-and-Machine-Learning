# Multiscale Optical Flow Estimation: Lucas-Kanade Method
Optical flow is defined as the pattern of apparent motion of image objects between two consecutive frames caused by the movement of object or camera. It can be presented as a 2D vector field where each vector is a displacement vector describing the motion of pixels from the first frame to the second.

## Optical Flow Estimation
Consider a image ![equation](https://latex.codecogs.com/gif.latex?I(x,y,t)), it takes dt time to move to (dx,dy). Since for those pixel value do not change. So that, ![equation](https://latex.codecogs.com/gif.latex?I(x,y,t)=I(x&plus;dx,y&plus;dy,t&plus;dt))

Apply taylor expansion on the right-hand side

![equation](https://latex.codecogs.com/gif.latex?I(x&plus;dx,y&plus;dy,t&plus;dt)=I(x,y,t)&plus;\frac{\partial&space;I}{\partial&space;x}dx&plus;\frac{\partial&space;I}{\partial&space;y}dy&plus;\frac{\partial&space;I}{\partial&space;t}dt&plus;O(n^2))

Therefore, 

![equation](https://latex.codecogs.com/gif.latex?\frac{\partial&space;I}{\partial&space;x}dx&plus;\frac{\partial&space;I}{\partial&space;y}dy&plus;\frac{\partial&space;I}{\partial&space;t}dt=0)

Divide both side by ![equation](https://latex.codecogs.com/gif.latex?dt),

![equation](https://latex.codecogs.com/gif.latex?\frac{\partial&space;I}{\partial&space;x}\frac{dx}{dt}&plus;\frac{\partial&space;I}{\partial&space;y}\frac{dy}{dt}&plus;\frac{\partial&space;I}{\partial&space;t}\frac{dt}{dt}=0)

or, 

![equation](https://latex.codecogs.com/gif.latex?I_xu&plus;I_yv&plus;I_t=0)

## Lucas-Kanade Method
The Lucas–Kanade method assumes that the displacement of these two frames is small. And the image flow (u,v) must satisfy

<img src="eq1.gif">

where ![equation](https://latex.codecogs.com/gif.latex?q_1,q_2\hdots,q_n) are pixels.

Thus, the system has more equations than unknowns. The Lucas–Kanade method applies least square to get a compromise solution.

<img src="eq2.gif">

## Result
<img src="optical_flow.jpg">
