# Keras implementation of SRCNN


The original paper is [Learning a Deep Convolutional Network for Image Super-Resolution](https://arxiv.org/abs/1501.00092)

![SRCNN]("./SRCNN.png")

My implementation have some difference with the original paper, include:

* use ['he_normal'](https://keras.io/initializations/) for weight initialization
* use Adam alghorithm for optimization
* I use the opencv library to produce the training data 
* I did not set different learning rate in different layer, but I found this network still work.

## Use:
### Create your own data
open **prepare_data.py** and change the data path to your data

Excute:
'python prepare_data.py'

### training and test:
Excute:
'python main.py'


## Result(training for 30 epoches, with upscaling factor 2):

|Method:| Bicubic | SRCNN |
|------|---------|-------|
|PSNR: |24.6971375057|28.6588428245|

Origin Image:
![Origin]("./butterfly_GT.bmp")

Bicubic:
![Bicubic]("./input.jpg")

SRCNN:
![SRCNN]("./pre_adam30.jpg")


