## I experimented with different size of calibration dataset and here what I got

Full dataset - 64 photos. Randomly took 5,10..60 photos ( with step=5 ) from the dataset and calibrate the camera on the ‘new’ set. Then compare them with GT.
The ground truth intrinsic parameters - what we have from the full dataset (64 photos).

checkerboard patterns = 19x14 chessboard

Error = GT - new parameter

<img src="/charts/fx_error.png" width="440" height="350"/>        <img src="/charts/cx error.png" width="440" height="350"/> 
<img src="/charts/fy error.png" width="440" height="350"/>        <img src="/charts/cy error.png" width="440" height="350"/> 

Error decreases respectively with the new dataset. I think dataset = 60-70 is enough to get ‘good’ parameters. Bigger dataset is not boost well and it’s hard to find new angles and requirement distance to monitor (good homorgaphies). If we take a photo from 3 meters - we probably don’t find our pattern.


### Little trick. 

Use the monitor with the full screen checkerboard pattern and take photos/record video in front of a monitor. This way is more convenient instead of paper pattern.

## General conclusion:

  1. Calibrate photo and video modes on your camera separately
  2. 2 similar cameras have different intrinsics ( due to manufacturing defects )
  3. More complex pattern gives better parameters.
