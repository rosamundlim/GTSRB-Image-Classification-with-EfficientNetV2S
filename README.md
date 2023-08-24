# GTSRB-Image-Classification-with-EfficientNetV2S
Applying EfficientNet2VS to achieve 98% test accuracy on GTSRB images

**Background:** The German Traffic Sign Benchmark (GTSRB) is a multi-class, single-image classification challenge, read more [here](https://www.kaggle.com/datasets/meowmeowmeowmeowmeow/gtsrb-german-traffic-sign) at the dataset page. 

**Dataset:** There are 43 classes in total, and more than over 50,000 images. There are 39,209 training examples and 12,630 test examples. 

**EDA**: The classes are imbalanced, for instance, there are way more training examples for "Speed Limit 50 km/h" than for the "dangerous curve left" category. Training images are blurry and many of them are in low light conditions.

**Approach**: i) To address low quality images, increase the contrast of the images, thanks to the suggestion in this article by [Thomas Tracey](https://medium.com/@thomastracey/recognizing-traffic-signs-with-cnns-23a4ac66f7a7) ii) To address class imbalance, include class weights in the model fitting process iii) Implement transfer learning using the EfficientNetV2S architecture which touts  faster training speed and better parameter efficiency than previous models ([source](https://arxiv.org/abs/2104.00298)). 

**Results**: weighted-averaged F1 score of 99% on validation set. weighted-averaged F1 score of 98% on test set. This demonstrates that the model has learned well and is able to generalize to the test set.
