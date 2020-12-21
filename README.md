# Keras Conv Visualizer
> Package allows visualize convolutional layers from keras models.

## Table of contents
* [General info](#general-info)
* [Libraries](#libraries)
* [Setup](#setup)
* [Documentation](#documentation)
* [PyPi](#pypi)
* [TODO](#todo)
* [Development](#development)
* [Status](#status)
* [Contact](#contact)

## General info
This package is a set of tools for visualizing convolutional layers from keras models. At this moment includes:
* [Filters visualization](#filters-visualization)
* [Grad-CAM activation visualization](#grad-cam)
* [Intermediate activations visualization](#intermediate-activations-visualization)

## Libraries
- NumPy - version ?
- TensorFlow - version ?
- OpenCV - version ?
- Matplotlib - version ?
- Keras - version ?

## Setup
* Install from PyPi: `pip install keras-conv-visualizer`

## Documentation
#### Status: _in progress_
### Filters visualization
```python
from keras_conv_visualizer.filters import FilterVisualization
import matplotlib.pyplot as plt
from tensorflow.keras.applications import VGG16

model = VGG16(weights="imagenet", include_top=False)
layer_name = "block5_conv3"

# First parameter - trained keras model, second - input_size
fv = FilterVisualization(model, (224, 224, 3))
# First parameter - layer feature index (ex. block1_conv1 has (224, 224, 64) index is from 0 to 63)
# Second parameter - layer name
loss, img = fv.visualize_filter(0, layer_name)
plt.imshow(img)
```
Result:

[![filters.png](https://i.postimg.cc/YCxdK1nP/filters.png)](https://postimg.cc/Mnv71j80)

<h3 id="grad-cam">Grad-CAM activation visualization</h3>


### Intermediate activations visualization

## PyPi
[keras-conv-visualizer](https://pypi.org/project/keras-conv-visualizer/)

## TODO
- Add shap values
- Automatically recognition input size for FilterVisualization

## Development
Want to contribute? Great!

To fix a bug or enhance an existing module, follow these steps:

* Fork the repo
* Create a new branch (`git checkout -b improve-feature`)
* Make the appropriate changes in the files
* **Verify if they are correct**
* Add changes to reflect the changes made
* Commit changes
* Push to the branch (`git push origin improve-feature`)
* Create a Pull Request

## Status
Library is: _in progress_

## Contact
albert.lis.1996@gmail.com - feel free to contact me!
