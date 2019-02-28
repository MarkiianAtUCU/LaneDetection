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

Original image
<img src="https://github.com/MarkiianAtUCU/LaneDetection/blob/master/content/img_0.png"/>
1. Warp perspective to "bird-eye view"
<img src="https://github.com/MarkiianAtUCU/LaneDetection/blob/master/content/img_1.png" width="300" height="300" border="10" />


2. Detect pixels of lane on the image:
    * Get saturation channel
    * Get yellow and white pixels of image
    * Combine two previous images
    * Threshold image, to get rid of unnecessary details
3. Find delta of 10 frames, to get info about movement
4. Dilate image
    <img src="https://github.com/MarkiianAtUCU/LaneDetection/blob/master/content/Step_2.png"/>

5. Detect Points on lanes
    * Threshold image && Draw histogrames
    * Mark points on road marking and add complement points
6. Fit 2 power polynome
<img src="https://github.com/MarkiianAtUCU/LaneDetection/blob/master/content/img_11.png" width="300" height="300" border="10" />
7. Warp perspective back

License
----

MIT