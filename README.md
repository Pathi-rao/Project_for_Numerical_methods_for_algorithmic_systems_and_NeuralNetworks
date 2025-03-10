# MVTEC Image Similarity Estimation using Siamese Neural Networks

<!-- TABLE OF CONTENTS -->
## Table of Contents
  - [About the Project](#about-the-project)
  - [Installation](#installation)
  - [References](#references)

## About the Project
This project is aimed to implement an image similarity estimation model using deep learning that will be able to generalize the difference between two given images and output a similarity metric.

This similarity metric could be any distance measure. For the sake of simplicity and also since it has been effective in different research papers, we have chosen Euclidean distance as our distance metric as it is also bergman divergence.

We have used the [dataset](https://www.mvtec.com/company/research/datasets/mvtec-ad) from MVTec AD which contains good and anomaly samples from 15 classes and trained the model using Siamese Neural Networks. We were able to do that by pairing images from same and different classes such that the model can learn the similarity metric. 

We have trained the model for 100 epochs on a NVIDIA 3060Ti GPU which took around 3.5 hours. 
During the test time, we have compared images from same class and as well as images from other class and obtained their distance metric, which helped us analyze the performance of our model.


## Installation

1. Clone the repo using the following command:
```bash
git clone https://github.com/Pathi-rao/Project_for_Numerical_methods_for_algorithmic_systems_and_NeuralNetworks 
```
2. Download the data from the provided link in [data](https://github.com/Pathi-rao/Image-Similarity-Estimation-using-Siamese-Neural-Networks/tree/main/data) folder and extract it. Also, please make sure to update the file paths if necessary.

3. Create a virtual environment with Python(For this step I will assume that you are able to create a virtual environment with `virtualenv`, but in any case you can check an example [here](https://realpython.com/python-virtual-environments-a-primer/).)

 - Activate the virtual environment and `cd` into the project directory

4. Install requirements using `pip`:
```bash
pip install -r requirements.txt
```
5. Run `train.py` to start training the model and use `testing_image_pair.py` to do inference on any two images
## References

* Paul Bergmann, Kilian Batzner, Michael Fauser, David Sattlegger, Carsten Steger: The MVTec Anomaly Detection Dataset: A Comprehensive Real-World Dataset for Unsupervised Anomaly Detection;
in: International Journal of Computer Vision, January 2021 [pdf](https://link.springer.com/content/pdf/10.1007/s11263-020-01400-4.pdf)

* Paul Bergmann, Michael Fauser, David Sattlegger, Carsten Steger: MVTec AD – A Comprehensive Real-World Dataset for Unsupervised Anomaly Detection;
in: IEEE Conference on Computer Vision and Pattern Recognition (CVPR), June 2019 [pdf](https://www.mvtec.com/fileadmin/Redaktion/mvtec.com/company/research/datasets/mvtec_ad.pdf) 

* Siamese Neural Networks for One Shot Image Recognition [pdf](https://www.cs.cmu.edu/~rsalakhu/papers/oneshot1.pdf)

