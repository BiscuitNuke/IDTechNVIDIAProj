
# IDTech Nvidia Vision Project

# THIS SOURCE CODE IS PUBLIC and CAN BE SHARED.

## About

This repository contains the information and trained Resnet-18 Dataset to detect certain types of food.

Video on the training/running:

https://youtu.be/A97BZsB8H7Q

## Deployment Information

This needs to be run on a capable device that can run the training procedure if needed, this will need to have the full dataset downloaded

Dataset here: https://www.kaggle.com/datasets/kmader/food41

### Running this

*the following scripts assume you have a clean environment, adjust if applicable.*

Used to start the training

```
python3 train.py --model-dir=models/images data/food
```

Used to export
```
python3 onnx_export.py --model-dir=models/images
```

Used to use the new model
```
imagenet.py --model=$NET/resnet18.onnx --input_blob=input_0 --output_blob=output_0 --labels=$DATASET/labels.txt $DATASET/test/baklava/3832465.jpg baklava.jpg 
```

Should run here, if it doesn't then something is wrong. 

# Miscellaneous

This code might not run, if not then consult the 
https://github.com/CHETHAN-CS/Nvidia-jetson-inference
libary, and go to where it tells you to train cat/dog, and put the dataset in there. 

© Copyright: None. This source code is *open source*
