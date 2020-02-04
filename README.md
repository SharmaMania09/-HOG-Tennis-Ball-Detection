HISTOGRAM OF ORIENTED GRADIENTS(HOG)

HOG method is one of the famous techniques for object recognition and edge detection. 
This method has been proposed by N. Dalal and B. Triggs in their research paper - "Histograms of Oriented Gradients for Human Detection, CVPR, 2005". 
The method is quite simple to devise and has been first experimented for human detection (that is, pedestrians on roads).
Soon, this technique took it's way to the detection of other objects. 
The method has the reputation of achieving upto 98 % accuracy for human detection.

Feature Extraction Using HOG

The HOG descriptor's code uploaded here, is for detection of tennis ball when trained and test. 
Hog descriptor uses edge detection by gradient calculation and histograms of gradients, with magnitudes as weights. 
The code uses [-1 0 -1] kernel for gradient magnitude and orientation calculation. Gradients are calculated in the range [0,180]. 
Histograms of 8 bins are calculated with magnitudes as weights.
Each image is checked if its of 32X32 size, else its resized. Each 32X32 image pixel matrix, is organised into 8X8 cells and then, histograms are calculated for each cell. 
Then, a 4X4 matrix with 8 bins in each cell is obtained. This matrix is organised as 2X2 blocks(with 50% overlap) and normalised, by dividing with the magnitude of histogram bins' vector.
