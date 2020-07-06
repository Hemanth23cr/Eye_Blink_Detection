# Eye blink detection using dlib and OpenCV

## What is eye aspect ratio (EAR)?

From the last project - Detecting facial landmarks - we know that we can apply facial landmark detection to localize important regions of the face, including eyes, eyebrows, nose, ears, and mouth. This also implies that we can extract specific facial structures by knowing the indexes of the particular face parts. In terms of blink detection, we are only interested in two sets of facial structures — the eyes.

## LIBRARIES REQIURED

     pip install opencv-python
     pip install numpy
     pip install dlib
     

## Download the DAT.file using the below link

 *  http://dlib.net/files/shape_predictor_68_face_landmarks.dat.bz2
 
 # SUMMARY
 
 Detect if eye blink or not An eye is blinking when: The eyelid is closed We can’t see the eyeball anymore Bottom and upper eyelashes connect together

We detected the eye, we also detected two lines: an horizontal line and a vertical line crossing the eye. The size of the horizontal line is almost identical in the closed eye and in the open eye while the vertical line is much longer in the open eye in coparison with the closed eye. In the closed eye, the vertical line almost disappears.

On python then we create a function to detect the blinking ratio where we insert the eye points and the facial landmark coordinates. We will then use the ratio number later to detect and we can finally define when the eye is blinking or not. In this case I found ratio number 5.7 to be the most reiable threshold, at least for my eye.

 
 
