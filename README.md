# Food101

Dataset food101 (original source link: https://data.vision.ee.ethz.ch/cvl/datasets_extra/food-101/) consists of 101 food categories, 
with 101000 images. Based on this data were conducted different experiments using both Kaggle GPU ('gpu-food-101.ipynb' notebook) and
TPU ('tpu-food101.ipynb' notebook). Specifically in TPU case raw images were converted into the efficient TFRecord format ('tfrecords-from-raw-images.ipynb' notebook). Food101 dataset is also available at TensorFlow Datasets project (was used for training on GPU).

## gpu-food-101.ipynb 
tensorflow.data.Dataset was used to manipulate the data. Model training stage - Transfer Learning technique. As a base model was picked EfficientNetB3
with 'noisy-student' weights. The best model was found by gradually increasing number of layers to unfreeze and simultaneously optimizing model's learning rate. That model was later analyzed for any signs of nonoptimal run using TensorFlow Profiler.

## tpu-food101.ipynb
TPUs enabled much more efficient training in terms of both training time and final performance. Data augmentation methods applied here are
tf.image stateless random transformation and advanced pixel-level transformation. There were also used Supervised Contrastive Learning as well as
OOF Training.
