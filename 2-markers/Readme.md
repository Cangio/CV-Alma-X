# Readme 2-markers
The section is about recognising markers in image and identify some region-of-interest.
## Aruco recognition
First we have considered that markers used in the competition would be aruco. The choice has been made considering that they are very popular, robust and well documented. Also the native implementation on opencv make them well optimized.\
We first tested already-implemented library functions with photos taken by a smartphone of different arucos printed in A4 sheets.\
We then tried to generalize algorithms to other markers, not considering a specific type (we have no information about markers implemented in competition). In order to do so, we developed a custom marker recognition function working on aruco. The idea is to edit only the part strictly regarding competition's markers.
## Implementing competition constraints
We then took advantage of the gained knowledge to edit test scripts and create a script more suited for the rover needs.\
In fact some considerations regarding the need to handle a video stream has been made, such as timing analysis.\
We also considered known the size of markers in order to be able to compute the distance.
## Dir-tree
Files are organized as follow:
1. [aruco-recognition.ipynb](aruco-recognition.ipynb) : Gain confidence with the environment, implementing library function of aruco recognition;
2. [aruco-performances.ipynb](aruco-performances.ipynb) : rough analysis of performance wrt aruco recognition;
3. [aruco-function-definition.ipynb](aruco-function-definition.ipynb) : just the functions analyzed in 1. pratical for inclusion in other files;
4. [image-transformation-markers.ipynb](image-transformation-markers.ipynb) : edit the image wrt the markers, rotate and cut area around marker and arrange the perspective;
5. [aruco-detection-custom.ipynb](aruco-detection-custom.ipynb) : implement from scratch marker recognition function in order to take advantage of intermediate results. This not aim to be a new exhaustive library function, it will be useful if markers are not exactly aruco or for performance' tests against library function and successive computations;
6. [thresholding-tests.ipynb](thresholding-tests.ipynb) : tune the adaptiveThreshold parameters to better suite our needs, e.g. big aruco wrt the total image size;
7. [camera-position.ipynb](camera-position.ipynb) : evaluate the camera position wrt the marker, estimate distance and angle with the virtual orthogonal line wrt the center of the marker. This is useful to estimate the rough distance from the panel, until it is in range of a more accurate laser or ultrasound sensor (time is crucial, if the arm is far away from the panel can move quicker).