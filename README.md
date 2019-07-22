# SHN-based-2D-Face-Alignment-Algorithms

Stacked Hourglass Network for 2D face alignment

This ia an pytorch implemention for face alignment with stacked hourglass network (SHN). We use the normalized mean errors (NME), cumulative errors distribution (CED) curve, area under the curve (AUC), and failure rate to measure the landmark location error.


#### Install
1. Install Pytorch >= 0.4 following the [official instructions](https://pytorch.org/)

Python3

## data
#### Data

1. You need to download the annotations files which have been processed from [OneDrive](https://1drv.ms/u/s!AiWjZ1LamlxzdmYbSkHpPYhI8Ms).

2. You need to download images (300W, AFLW, WFLW) from official websites and then put them into `images` folder for each dataset.

Your `data` directory should look like this:

````
SHN-based-2D-face-alignment
-- experiments
-- data
   |-- 300w
   |   |-- afw
   |   |-- helen
   |   |-- ibug
   |   |-- lfpw
````  

## Training and testing 
* For training, stacks = 2, input resolution = 256 
```sh
python main.py 
```
* Run evaluation to get result.
```sh
python main.py --phase test
```
