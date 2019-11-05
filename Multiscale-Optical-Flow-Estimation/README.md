# Multiscale Optical Flow Estimation: Lucas-Kanade Method
Optical flow is defined as the pattern of apparent motion of image objects between two consecutive frames caused by the movement of object or camera. It can be presented as a 2D vector field where each vector is a displacement vector describing the motion of pixels from the first frame to the second.

## Optical Flow Estimation
Consider a image ![equation](https://latex.codecogs.com/gif.latex?I(x,y,t)), it takes dt time to move to (dx,dy). Since for those pixel value do not change. So that, ![equation](https://latex.codecogs.com/gif.latex?I(x,y,t)=I(x&plus;dx,y&plus;dy,t&plus;dt))

Apply taylor expansion on the right-hand side

![equation](https://latex.codecogs.com/gif.latex?I(x&plus;dx,y&plus;dy,t&plus;dt)=I(x,y,t)&plus;\frac{\partial&space;I}{\partial&space;x}dx&plus;\frac{\partial&space;I}{\partial&space;y}dy&plus;\frac{\partial&space;I}{\partial&space;t}dt&plus;O(n^2))

Therefore, 

## Lucas-Kanade Method


## Result
<img src="optical_flow.jpg">
