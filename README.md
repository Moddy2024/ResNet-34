# ResNet-34

# Dependencies
* [PyTorch](https://pytorch.org/)
* [Matplotlib](https://matplotlib.org/)
* [PIL](https://pypi.org/project/Pillow/)
* [Numpy](https://numpy.org/)
* [OS](https://docs.python.org/3/library/os.html)
* [fast.ai](https://www.fast.ai/)
* [Torchvision](https://pytorch.org/vision/stable/index.html)
* [torchinfo](https://github.com/TylerYep/torchinfo)
Once you have these dependencies installed, you can clone the Custom ResNet-18 repository from GitHub:
```bash
 https://github.com/Moddy2024/ResNet-34.git
```
# Key Files
# Features
This custom ResNet-18 includes the following features:

* Support for multiple image sizes and aspect ratios
* Option to fine-tune the model on a specific dataset
* Ability to save and load trained models
# Training and Validation Image Statistics
The dataset used to train the model is CIFAR-10. The CIFAR-10 dataset consists of 60,000 32x32 color training images and 10,000 test images. Each image is labeled with one of 10 classes: airplane, automobile, bird, cat, deer, dog, frog, horse, ship, and truck. There are 6,000 images of each class in the training set, and 1,000 images of each class in the test set. CIFAR-10 is a popular choice for benchmarking because it is a well-defined and widely-used dataset, and the images are small enough that it is possible to train relatively large models on a single machine.
# Dataset
The  CIFAR-10 dataset (Canadian Institute For Advanced Research) can be downloaded from [here](https://www.cs.toronto.edu/~kriz/cifar.html). It can also be downloaded from PyTorch Datasets.
```bash
# Load the CIFAR10 dataset
train_dataset = torchvision.datasets.CIFAR10(root='./data', train=True, download=True, transform=transforms.ToTensor())
test_dataset = torchvision.datasets.CIFAR10(root='./data', train=False, download=True, transform=transforms.ToTensor())
```
In this repository the dataset has been downloaded using fast.ai as seen below.
```bash
from fastai.data.external import untar_data, URLs
data_dir = untar_data(URLs.CIFAR)
data_dir = str(data_dir)
```
