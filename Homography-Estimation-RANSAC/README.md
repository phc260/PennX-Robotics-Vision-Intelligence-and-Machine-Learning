# Homography Estimation: RANSAC
Use a sequence of images from different perspectives to construct a panoramic image.

1. Compute the homography between two images when correspondences are known.
2. Estimate correspondences between two sets of Harris Corners using Nearest Neighbor and the ratio test.
3. Use RANSAC to find the best homography estimate from the estimated correspondences.

## Result
*Images from different perspectives*
<img src="building1.jpg" width="45%"><img src="building2.jpg" width="45%">

*Panoramic Image*
<img src="building_ransac.jpg">
