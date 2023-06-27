## Human Activity Recognition

DEMO:  [![Nbviewer](https://github.com/jupyter/design/blob/main/logos/Badges/nbviewer_badge.svg)](https://nbviewer.jupyter.org/github/shejz/Human-Activity-Recognition/blob/main/Human%20Activity%20Recognition/human_activity_recognition.ipynb)

The pre-trained human activity recognition deep learning model was trained on the **Kinetics 400 dataset**.


### Dataset

**This dataset consists of**:

- 400 human activity recognition classes
- At least 400 video clips per class (downloaded via YouTube)
- A total of 300,000 videos

You can view the full list of classes the model can recognize [here](https://github.com/opencv/opencv/blob/master/samples/data/dnn/action_recongnition_kinetics.txt)

To learn more about the dataset, including how it was curated, be sure to refer to Kay et al.’s 2017 paper, [The Kinetics Human Action Video Dataset](https://arxiv.org/abs/1705.06950).


### Model

The model we utilized was ResNet, but with a twist — the model architecture had been modified to utilize 3D kernels rather than the standard 2D filters, enabling the model to include a temporal component for activity recognition. The 3D ResNet is trained on the Kinetics dataset, which includes 400 action classes.

The model we’re using for human activity recognition comes from Hara et al.’s 2018 CVPR paper, [Can Spatiotemporal 3D CNNs Retrace the History of 2D CNNs and ImageNet](https://arxiv.org/abs/1711.09577)

![](https://github.com/shejz/Human-Activity-Recognition/blob/main/Human%20Activity%20Recognition/3D%20ResNet.jpg)

Finally, we implemented human activity recognition using OpenCV and Hara et al.’s [PyTorch implementation](https://github.com/kenshohara/video-classification-3d-cnn-pytorch) which we loaded via OpenCV’s dnn module.


### Sample Output

![](https://github.com/shejz/Human-Activity-Recognition/blob/main/Human%20Activity%20Recognition/output/activities.gif)

![](https://github.com/shejz/Human-Activity-Recognition/blob/main/Human%20Activity%20Recognition/output/flying%20kite.gif)

![](https://github.com/shejz/Human-Activity-Recognition/blob/main/Human%20Activity%20Recognition/output/punching_bag.gif)

![](https://github.com/shejz/Human-Activity-Recognition/blob/main/Human%20Activity%20Recognition/output/surfing.gif)
