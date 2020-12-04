# Readme 2-markers
The section is about recognising markers in image and identify some region-of-interest.
## Aruco recognition
First we have considered that markers used in the competition would be aruco. The choice has been made considering that they are very popular, robust and well documented. Also the native implementation on opencv make them well optimized.\
We first tested already-implemented library functions with photos take by a smarphone of different arucos printed in A4 sheets.
## Implementing competition constraints
We then took advantage of the gained knowledge to edit test scripts and create a script more suited for the rover needs.\
In fact some considerations regarding the need to handle a video stream has been made.
## Dir-tree
Files are organized as follow:
1. [aruco-recognition.ipynb](aruco-recognition.ipynb) : Gain confidence with the environment, implementing library function of aruco recognition;
2. [aruco-performances.ipynb](aruco-performances.ipynb) : rough analysis of performance wrt aruco recognition;
3. [aruco-function-definition.ipynb](aruco-function-definition.ipynb) : just the functions analyzed in 1. pratical for inclusion in other files;
4. [image-transformation-markers.ipynb](image-transformation-markers.ipynb) : edit the image wrt the markers, cut area around marker and arrange the perspective;
5. [marker-finder.ipynb](marker-finder.ipynb) : implement from scratch marker recognition function in order to take advantage of intermediate results;
6. [thresholding-tests.ipynb](thresholding-tests.ipynb) : tune the adaptiveThreshold parameters to better suite our needs, e.g. big aruco wrt the total image size.