# Overview
Abnormality detection in chest x-ray imags using deep learning


For more details contact: 
Monib Sediqi (monib.korea@gmail.com)

[[Home]](http://monibsediqi.github.io) 

# Flow Diagram

<p align='center'>
  <img src="https://user-images.githubusercontent.com/42628945/184998200-40221f8c-f225-436c-87c1-3aa6de9c6a9e.jpg" width=1000)
</p>  

# Code Desc

* Binary classification and abnormality detection in chest x-ray images

* Normality and abnormality detection of the following classes in a chest x-ray images.
1. Rib fracture
2. Pneumothorax
3. Tension pneumothorax
4. Hemothorax
5. Pericardial effusion
6. Mediastinum abnormality
7. Pleural effusion

* Input: X-ray image (1024x1024x3)
* Outputs:
    1. Probability score
    2. PNG image with CAM


### Data Augmentation
* Random horizontal flip 
* Random rotation (10 degrees)
![](images/cda_augmentation.JPG)

## Install
1. [Tensorflow >= 2](https://www.tensorflow.org/) (Note: The code is tested in an environment with `python=3.8, cuda=10.1`)
2. Download **grad_GAM**
   ```
   git clone https://github.com/Monibsediqi/grad_CAM.git
   cd grad_CAM
   ```
3. Install Requirements
   ```
   nose
   tqdm
   scipy
   cython
   requests
   ```

## Open Jupyter Notebook and execute the xception_CAM notebook

# Results

## Numerical Results
| Class | Accuracy | AUC |
|:----|:----|:----|
| Rib fracture | 0.826 |  0.71 |
| Pneumothorax | 0.9235 | 0.58 |
| Tension pneumothorax| 0.9945 | 0.70 |
| Hemothorax| 0.9563 | 0.70 |
| Pericardial effusion | 0.9322 | 0.82 |
| Mediastinum abnormality | 0.9812 | 0.72  |
| Pleural effusion | 0.9301 |  0.82 |
### 
## Visual Results
|Class|Normality|Original | CAM | 
|:----|:---:|:---:|:---:|
|Rib fracture| Normal |![](Assets/rib/orig/8_res.jpg)| ![](Assets/rib/norm/Serial_No8.jpg) |
|Rib fracture| Abnormal |![](Assets/rib/orig/154_res.jpg)| ![](Assets/rib/abnorm/Serial_No154.jpg) |
|Pneumothorax| Normal |![](Assets/pneumo/orig/6_res.jpg)| ![](Assets/pneumo/norm/Serial_No6.jpg) |
|Pneumothorax| Abnormal |![](Assets/pneumo/orig/165_res.jpg)| ![](Assets/pneumo/abnorm/Serial_No165.jpg) |
|Tension pneumothorax| Normal |![](Assets/ten/orig/11_res.jpg)| ![](Assets/ten/norm/Serial_No11.jpg) |
Tension pneumothorax| Abnormal |![](Assets/ten/orig/148_res.jpg)| ![](Assets/ten/abnorm/Serial_No148.jpg) |
|Hemothorax| Normal |![](Assets/homo/orig/36_res.jpg)| ![](Assets/homo/norm/Serial_No36.jpg) |
|Hemothorax| Abnormal |![](Assets/homo/orig/429_res.jpg)| ![](Assets/homo/abnorm/Serial_No429.jpg) |
|Pericardial effusion| Normal |![](Assets/peri/orig/1_res.jpg)| ![](Assets/peri/norm/Serial_No1.jpg) |
|Pericardial effusion| Abnormal |![](Assets/peri/orig/399_res.jpg)| ![](Assets/peri/abnorm/Serial_No399.jpg) |


### Citation
```
  @misc{Monib Sediqi Grad-CAM,
    author = {Monib Sediqi},
    title = {Class Activation Map (CAM) Tensorflow},
    year = {2022},
    howpublished = {\url{https://github.com/Monibsediqi/srcGradCam_pub},
  }
```

## License
Copyright (c) 2022 Monib Sediqi. Contact me (monib.korea@gmail.com) for commercial use (or rather any use that is not academic research). Free for academic research use only, as long as proper attribution is given and this copyright notice is retained.
