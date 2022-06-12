# crime-rate-prediction-using-SVI

This project is designed and developed as part of masters research thesis. The work aims to predict multiple crime rates from street view images by solving a multioutput regression problem. Resnet-18 loaded with weights trained on [places365](https://github.com/CSAILVision/places365) dataset is used as a building block for a 4-CNN model

The project includes different steps in achieving the desired result
1. Data Preparation
2. Model building
3. Training and Prediction

Data Preaparation is handled in ArcGIS/QGIS softwares and is out of scope of this repository. But the final product of Data Preapration is used to download the street view images and used throughout for training, validation and testing.


Folder heirarchy and structure

```
📦crime-rate-prediction-using-SVI
 ┣ 📂CODES
 ┃ ┣ 📜resnet_results.ipynb
 ┃ ┣ 📜resnet_train.ipynb
 ┃ ┗ 📜svi.ipynb
 ┣ 📂DATA
 ┣ 📂FILES
 ┣ 📂GIS
 ┣ 📂WEIGHTS
 ┃ ┣ 📜resnet18_places365.h5
 ┃ ┗ 📜resnet18_places365.pth.tar
 ┣ 📜.gitignore
 ┣ 📜README.md
 ┗ 📜requirements.txt
 ```

The converted model from pytorch to keras is included. All the other files are specific to the chosen location and type of crimes considered for analysis.

For further imformation on methodology, please refer to [Crime rate prediciton using Street View Images](http://essay.utwente.nl/88644/)

### Setting up the environment. 

Anaconda is used to setup the environment

```conda create -n venv python=3.7```

```pip install -r requirements.txt```

onnx latest version conflicts with the implementation of [pytorch2keras](https://github.com/gmalivenko/pytorch2keras). So, use onnx=1.8.1



