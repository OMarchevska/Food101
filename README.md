# Food101

Dataset food101 (original source link: https://data.vision.ee.ethz.ch/cvl/datasets_extra/food-101/) consists of 101 food categories, 
with 101000 images. Based on this data were conducted different experiments using both Kaggle GPU ('gpu-food-101.ipynb' notebook) and
TPU ('tpu-food101.ipynb' notebook). Specifically in TPU case raw images were converted into the efficient TFRecord format ('tfrecords-
from-raw-images.ipynb' notebook). Food101 dataset is also available at TensorFlow Datasets project (was used for training on GPU).
