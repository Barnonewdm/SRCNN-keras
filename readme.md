# Keras implementation of SRCNN


The original paper is [Learning a Deep Convolutional Network for Image Super-Resolution](https://arxiv.org/abs/1501.00092)

<p align="center">
  <img src="https://github.com/MarkPrecursor/SRCNN-keras/blob/master/SRCNN.png" width="800"/>
</p>

My implementation have some difference with the original paper, include:

* use ['he_normal'](https://keras.io/initializations/) for weight initialization
* use Adam alghorithm for optimization
* I use the opencv library to produce the training data 
* I did not set different learning rate in different layer, but I found this network still work.

## Use:
### Create your own data
open **prepare_data.py** and change the data path to your data

Excute:
`python prepare_data.py`

### training and test:
Excute:
`python main.py`


## Result(training for 30 epoches, with upscaling factor 2):

|Method:| Bicubic | SRCNN |
|------|---------|-------|
|PSNR: |24.6971375057|28.6588428245|

Origin Image:
<p align="left">
  <img src="https://github.com/MarkPrecursor/SRCNN-keras/blob/master/butterfly_GT.bmp" width="200"/>
</p>

Bicubic:
<p align="left">
  <img src="https://github.com/MarkPrecursor/SRCNN-keras/blob/master/input.jpg" width="200"/>
</p>

SRCNN:
<p align="left">
  <img src="https://github.com/MarkPrecursor/SRCNN-keras/blob/master/pre_adam30.jpg" width="200"/>
</p>




