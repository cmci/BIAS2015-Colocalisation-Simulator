# BIAS2015-Colocalisation-Simulator

*BIAS2015 Colocalisation Simulator is an ImageJ plugin aimed at generating synthetic images to teach co-localisation methods.*

## Simulation mode
*Several scenario are available (not all implemented, yet):*
* **Random:**
  * Channel 1 and 2 images are generated independently.
* **Pure co-localisation:**
  * Channel 2 is the exact copy of channel 1: parameters entered under the channel 2 section are not taken into account. 
* **Exclusion:**
  * TO BE IMPLEMENTED. 
* **Inclusion:**
  * Channel 1 describes hollow elements, channel 2 elements that will fit into the emptied part of channel 1's objects.

## Parameters

*This section contains all global parameters conditionning the plugin's output*

* **Image dimensions:**
  * Width, height and depth of the output image, in pixels.
* **Chromatic shift:**
  * Parameters of the translation vector to apply on the image generated for channel2: a number of pixel in XYZ for the shift.
* **Field non-homogeneity:**
  * Generates an image of a gaussian, centred on the input XY coordinates. This image will be multiplied onto images from channel 1 and 2 to corrupt them.
* **Bleedthrough:**
  * Two parameters will define the percentage of signal from channel 1 that will be seen in channel 2 and the reverse way round. Basically, the result image for channel 1 will be the original channel1 + xxx% from channel 2. 

## Shapes
Its purpose is to generate basic shapes in 3D:

* **Parallelepiped:**
  * Parameters: number of elements to draw, width/height/depth of the bounding box.
  * Orientation: will depend on the dimensions.
* **Ellipsoid:**
  * Parameters: number of elements to draw, width/height/depth of the bounding box. Each dimension will impose the diameter in the repestive dimension.
  * Orientation: will depend on the dimensions.
* **Cylinder:**
  * Parameters: number of elements to draw, width/height/depth of the bounding box.
  * Orientation: might be oriented along XY, XZ or YZ.
* **Cone:**
  * Parameters: number of elements to draw, width/height/depth of the bounding box.
  * Orientation: might be oriented along XY, XZ or YZ.
* **Torus:**
  * Parameters: number of elements to draw, width/height/depth of the bounding box, overal radius (R), radius of the torus section (r).
  * Orientation: might be oriented along XY, XZ or YZ.
* **Helix:**
  * Parameters: number of elements to draw, width/height/depth of the bounding box, overal radius (R), radius of the helix section (r), step size of the helix.
  * Orientation:oriented along XY, XZ or YZ.
