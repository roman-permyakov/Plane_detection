###### PlanetScope. Aircrafts

# **Plane Detection in Satellite Imagery** <img src="https://eospatial.kz/images/para/1.png" height="50">

##  <p align="justify"> [Detect aircrafts in Planet satellite image chips](https://www.kaggle.com/datasets/rhammell/planesnet?resource=download)</p> 
 
###  Introduction
<p align="justify">The aim of this dataset is to help address the difficult task of detecting the location of airplanes in satellite images.
Automating this process can be applied to many issues including monitoring airports for activity and traffic patterns, and defense intelligence.
Continusouly updates will be made to this dataset as new Planet imagery released. Current images were collected as late as July 2017.

Dataset is available from here: https://www.kaggle.com/datasets/rhammell/planesnet?resource=download </p>

### Content
<p align="justify">Provided is a zipped directory planesnet.zip that contains the entire dataset as .png image chips.
Each individual image filename follows a specific format: <i>{label} {scene id} {longitude} _ {latitude}.png</i>

* <b>label</b>: Valued 1 or 0, representing the "plane" class and "no-plane" class, respectively
* <b>scene id</b>: The unique identifier of the PlanetScope visual scene the image chip was extracted from. The scene id can be used with the Planet API to discover and download the entire scene
* <b>longitude_latitude</b>: The longitude and latitude coordinates of the image center point, with values separated by a single underscore.

The pixel value data for each 20x20 RGB image is stored as a list of 1 200 integers within the data list.
The first 400 entries contain the red channel values, the next 400 the green, and the final 400 the blue.
The image is stored in row-major order, so that the first 20 entries of the array are the red channel values of the first row of the image.</p>

### Class labels
<p align="justify">The "plane" class includes 8 000 images. Images in this class are near-centered on the body of a single airplane,
with the majority of the plane's wings, tail, and nose also visible. Examples of different aircraft sizes, orientations,
and atmospheric collection conditions are included. Example images from this class are shown below.

<p><img width="548" alt="image" src =https://raw.githubusercontent.com/roman-permyakov/Plane_detection/dd473c8fe15887a7937cd58f3e6dcd3e96c9da9e//img/planes.png></p>

The "no-plane" class includes 24 000 images. A third of these are a random sampling of different landcover features - water, vegetion,
bare earth, buildings, etc. - that do not include any portion of an airplane.

The next third are "partial planes" that contain a portion of an airplane, but not enough to meet the full definition of the "plane" class.

The last third are "confusers" - chips with bright objects or strong linear features that resemble a plane - that have previously been mislabeled by machine learning models.
Example images from this class are shown below.</p>

<p><img width="548" alt="image" src =https://raw.githubusercontent.com/roman-permyakov/Plane_detection/dd473c8fe15887a7937cd58f3e6dcd3e96c9da9e//img/no_plane1.png></p>

Inspired by [@kylepob61392](https://medium.com/@kylepob61392/airplane-image-classification-using-a-keras-cnn-22be506fdb53)
