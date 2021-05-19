# Convolutional Neural Networks in High Energy Physics

Welcome to the repository for the PHY 506 final project. The primary aim of this project is to employ Neural Network algorithms to correctly categorize and differetiate signal jets from background QCD jets produced during experiments at the Large Hadron Collider.

## Implementation

This entire model was taken from **https://github.com/ubcms-xai/AdversarialNetworks** and will be used to gain a better understanding of neural networks in high energy physics; it is located in the ```Convolutional Neural Networks``` folder, which contains two sub-folders.

The first of these folders is ```1D CNN``` and contains the files ```makeFourVectors.ipynb``` and ```1D_CNN.ipynb``` in its directory. Running ```makeFourVectors.ipynb``` creates a ```data``` folder where ```.npz``` data files are saved. These files are then fed into ```1D_CNN.ipynb``` which contains the CNN implementation used for jet classification.   

Similarly, the ```2D CNN``` folder contains the files ```makeJetImages.ipynb``` and ```2D_CNN.ipynb``` in its directory. It runs exactly as ```1D CNN```, however the CNN used here trains on a 2-dimensional 16 X 16 image rather than a 1-dimensional list.

An explanation of the physics and the CNN for this project can be found at ```Final Presentation.pdf```.  

## Requirements

In order to run this program, Python 3.4 or higher is necessary. Besides the usual numpy, matplotlib, etc. installation, this project makes extensive use of TensorFlow along with Keras. A list of the required software can be found in the ```requirements.txt``` file.

This project is also meant to run on a Raspberry Pi model 4B; the most recent version of Raspbian 64-bit OS is recommended. Instructions for installing Tensorflow on a Raspberry Pi can be found at **https://qengineering.eu/install-tensorflow-2.4.0-on-raspberry-64-os.html**. Note that the "Intalling from Scratch" procedure may take over 48 hours to complete. Due to the computaional limitations of this hardware, some it the parameters such as epochs, particle number, and number of events may have to be re-adjusted. 

## Video Link

A video presentation of this project can be found at: https://youtu.be/xmD2GJmbwCI
