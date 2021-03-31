# Anomaly Detection Neural Network

This is the repository for the PHY 506 final project - it will be routinely updated throughtout the remainder of the semester until the project is complete. The primary aim of this project is to employ Machine Learning (ML) algorithms to detect anomalies in experiments performed at the Large Hadron Collider (LHC).

As we know, collisions between protons give rise to hadron jets composed in partly of quarks and gluons. However, due to color confinement, these particles cannot be directly observed and their properties must be analyzed indirectly. To this end, we will develop a Generative Adversarial Network (GAN) to train generator/discriminator neural network pairs to generate physically sound models. This is essentially the same procedure used differentiate images of cats and dogs, however here we shall distinguish between signal and background jet sources in the hopes of finding new physics beyond the standard model.

## Implementation

This repository is far from complete, however at the present we have a simple yet intuitive toy model that we can train. This entire model was taken from **https://github.com/ubcms-xai/AdversarialNetworks** and has been used to gain a better understanding of neural networks in high energy physics; it is composed of two notebooks. The first of these notebooks is ```makeFourVectors.ipynb``` which creates a series of four-vectors with gaussian and exponential distributions for signal and background jets, respectively. These are then saved in the ```data``` folder as ```.npz``` files.

The ```toy_adversarial_1dcnn.ipynb``` notebook then takes these four-vectors as inputs, and trains two adversarial networks to produce accurate synthetic data. The training period is held over 10 epochs. We note that these notebooks are part of the XIA for ML repository at UB, and it is the author's desire to use them as a stepping stone for constructing a program for anomally detection once a better understanding on this is obtained.

## Requirements

In order to run this program a version of Python 3.6 or higher is required, along with the usual ```numpy```, ```matplotlib```, and ```jupyter notebook``` modules. Furhtermore, ```h5py```, and ```neural-structured-learning``` were also necessary and may be installed through a ```pip``` command. A complete list of requirements can be found in the ```requirements.txt`` file.

This project is also meant to run on a Raspberry Pi model 4B. The most recent version of the Raspbian 64-bit OS and Tensorflow are recommended. Instructions for installing Tensorflow on a Raspberry Pi can be found at **https://qengineering.eu/install-tensorflow-2.4.0-on-raspberry-64-os.html**. Note that the "Intalling from Scratch" procedure may last over 48 hours of compilation time. 

