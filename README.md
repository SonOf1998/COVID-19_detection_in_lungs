### Team: Brave Metropolitans
- Máté Levente Kis
- Nándor Réfi
- Miklós Bendegúz Szócska

# Datasets used in the project:  
- X-Ray Image Dataset: https://github.com/muhammedtalo/COVID-19/tree/master/X-Ray%20Image%20DataSet  
- nabeelsajid917: https://www.kaggle.com/nabeelsajid917/covid-19-x-ray-10000-images  
- chest_xray: https://www.kaggle.com/paultimothymooney/chest-xray-pneumonia  
- COVID-19 Dataset: https://data.mendeley.com/datasets/8h65ywd2jr/3  

# Current state of development:
Our goal is to detect efficiently non-infected, bacterial infected or COVID-19 infected lungs on chest xrays. We decided to use transfer learning to reach our goal.
  
We are working with 3 labels:
* no_findings: no detected infection
* covid_19: infected with COVID-19
* pneumonia: bacterial infection
    
Datasets used for learning and evaluation:
* train
  * covid_19(370)
  * no_findings(449)
  * pneumonia(450)
* test
  * covid_19(37)
  * no_findings(50)
  * pneumonia(50)

So far we used transfer learning on the following models:  
| Model  | Branch | File  | Validation accuracy | Test accuracy  |
| ------------- | ------------- | ------------- | ------------- | ------------- |
| VGG19 with ImageNet | mate_workspace_vgg19 | COVIDDetector.ipynb | Validation accuracy: 87.3% | Test accuracy: 85.4% |
| ResNet34 with ImageNet | mate_workspace_resnet34 | COVIDDetector.ipynb | Validation accuracy: 83% | Test accuracy: 83.2% |
| Inception v3 with ImageNet | mate_workspace | COVIDDetector.ipynb | Validation accuracy: 82.2% | Test accuracy: 81.8% |
| ResNet152 v2 with ImageNet | nandor_workspace | ResNet152V2_covid.ipynb | Validation accuracy: 75.9% | Test accuracy: 81.0% |
| SEResNet152 with ImageNet | mate_workspace_seresnet152 | COVIDDetector.ipynb | Validation accuracy: 88.14% | Test accuracy: 83.94% |
| DenseNet201 with ImageNet | miki_workspace_densenet | COVIDDetector.ipynb | Validation accuracy: 86.95% | Test accuracy: 83.94%|
  

# How to use:  
Open any notebook in Google Colab and run cells. The notebook will automatically download the prepared datasets from this repository.   
