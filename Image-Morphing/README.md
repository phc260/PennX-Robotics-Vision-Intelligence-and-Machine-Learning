# Image Morphing via triangulation
A morph is a warp of the image shape and a cross-dissolve of the image colors. The warp is controlled by defining a correspondence between the two pictures. The correspondence maps eyes to eyes, mouth to mouth, chin to chin, ears to ears, etc., to get the smoothest transformation.

First, for each pixel in the intermediate image, determine which triangle it falls inside.

Second, compute the barycentric coordinate for each pixel in the corresponding triangle.
![equation](https://latex.codecogs.com/gif.latex?\small&space;\begin{bmatrix}&space;a_x&space;&&space;b_x&space;&&space;c_x\\&space;a_y&space;&&space;b_y&space;&&space;c_y\\&space;1&space;&&space;1&space;&&space;1&space;\end{bmatrix}&space;\begin{bmatrix}&space;\alpha&space;\\&space;\beta&space;\\&space;\gamma&space;\end{bmatrix}&space;=&space;\begin{bmatrix}&space;x\\&space;y\\&space;1&space;\end{bmatrix})
## Result
<img src="image_morph.png">
<img src="image_morph_triangulation.png">
