# SVNH CNN

Using TensorFlow (Keras) to classify house numbers in the [Street View House Numbers (SVHN) Dataset](http://ufldl.stanford.edu/housenumbers/).

![](http://ufldl.stanford.edu/housenumbers/examples_new.png)

## Demo
Please check this [Jupyter Notebook](https://nbviewer.jupyter.org/github/dyckia/SVHN-CNN/blob/master/SVHN.ipynb) for the model pipline and performance.

## Network Architecture 

| Layer (type)        | Output Shape           | Param #  |
| ------------- |:-------------:| -----:|
| conv2d (Conv2D)      | (None, 30, 15, 32) | 896 |
| conv2d_1 (Conv2D)       | (None, 28, 13, 32) | 9248 |
| max_pooling2d (MaxPooling2D)      |  (None, 14, 6, 32) | 0 |
| dropout (Dropout)      | (None, 14, 6, 32) | 0 |
| conv2d_2 (Conv2D)      | (None, 12, 4, 64) | 18496 |
| conv2d_3 (Conv2D)      | (None, 10, 2, 64) | 36928 |
| max_pooling2d_1 (MaxPooling2      | (None, 5, 1, 64) | 0 |
| dropout_1 (Dropout)      | (None, 5, 1, 64) | 0 |
| flatten (Flatten)      | (None, 320) | 0 |
| dense (Dense)      | (None, 512) | 164352 |
| dropout_2 (Dropout)      | (None, 512) | 0 |
| dense_1 (Dense)      | (None, 10) | 5130 |

Total params: 235,050
Trainable params: 235,050
Non-trainable params: 0
