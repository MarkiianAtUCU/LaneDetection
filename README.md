# Lane detection with OpenCV
Main goal of this project was to detect and track road lane only with one camera
### Demo
<a href="http://www.youtube.com/watch?feature=player_embedded&v=Cr9Jy1n9ZdU
" target="_blank"><img src="http://img.youtube.com/vi/Cr9Jy1n9ZdU/0.jpg" 
 width="640" height="320" border="10" /></a>
### Dependencies
* Python >= 3.6 
* OpenCV
* numpy

### Pipeline
1. Warp perspective to "bird-eye view"
<img src="https://github.com/MarkiianAtUCU/LaneDetection/blob/master/content/img_1.png" width="300" height="300" border="10" />
2. Detect pixels of lane on the image:
    * Get saturation channel
    <img src="https://github.com/MarkiianAtUCU/LaneDetection/blob/master/content/img_2.png" width="300" height="300" border="10" />
    * Get yellow and white pixels of image
    <img src="https://github.com/MarkiianAtUCU/LaneDetection/blob/master/content/img_3.png" width="300" height="300" border="10" />
    * Combine two previous images
    <img src="https://github.com/MarkiianAtUCU/LaneDetection/blob/master/content/img_4.png" width="300" height="300" border="10" />
    * Threshold image, to get rid of unnecessary details
    <img src="https://github.com/MarkiianAtUCU/LaneDetection/blob/master/content/img_5.png" width="300" height="300" border="10" />
3. Find delta of 10 frames, to get info about movement
<img src="https://github.com/MarkiianAtUCU/LaneDetection/blob/master/content/img_6.png" width="300" height="300" border="10" />
4. Dilate image
<img src="https://github.com/MarkiianAtUCU/LaneDetection/blob/master/content/img_7.png" width="300" height="300" border="10" />
5. Detect Points on lanes
    * Threshold image
    * Draw histogrames
    * Find lanes
6. Fit 2 power polynome
<img src="https://github.com/MarkiianAtUCU/LaneDetection/blob/master/content/img_11.png" width="300" height="300" border="10" />
7. Warp perspective back

License
----

MIT