# Lane detection with OpenCV
Main goal of this project was to detect and track road lane only with one camera
### Demo
<a href="http://www.youtube.com/watch?feature=player_embedded&v=Cr9Jy1n9ZdU
" target="_blank"><img src="http://img.youtube.com/vi/Cr9Jy1n9ZdU/0.jpg" 
alt="IMAGE ALT TEXT HERE" width="240" height="180" border="10" /></a>
### Dependencies
* Python >= 3.6 
* OpenCV
* numpy

### Pipeline
1. Warp perspective to "bird-eye view"
2. Detect pixels of lane on the image:
    * Get saturation channel
    * Get yellow and white pixels of image
    * Combine two previous images
    * Threshold image, to get rid of unnecessary details
3. Find delta of 10 frames, to get info about movement
4. Dilate image
5. Detect Points on lanes
    * Threshold image
    * Draw histogrames
    * Find lanes
6. Fit 2 power polynome
7. Warp perspective back

License
----

MIT