# Stacked Hourglass Network for 2D face alignment

This ia a PyTorch implemention for face alignment with stacked hourglass network (SHN). We use the normalized mean errors (NME), cumulative errors distribution (CED) curve, area under the curve (AUC), and failure rate to measure the landmark location performance. This work (SHN-based) has achieved outstanding performance on 300-W and WFLW datasets. 

<div align=center><img src="https://github.com/face-alignment-group-of-ahucs/SHN-based-2D-face-alignment/blob/master/image/1.jpg" width="150" height="225" /><img src="https://github.com/face-alignment-group-of-ahucs/SHN-based-2D-face-alignment/blob/master/image/2.jpg" width="150" height="225" /><img src="https://github.com/face-alignment-group-of-ahucs/SHN-based-2D-face-alignment/blob/master/image/3.jpg" width="150" height="225" /><img src="https://github.com/face-alignment-group-of-ahucs/SHN-based-2D-face-alignment/blob/master/image/4.jpg" width="150" height="225" /><img src="https://github.com/face-alignment-group-of-ahucs/SHN-based-2D-face-alignment/blob/master/image/5.jpg" width="150" height="225" /></div>

## Performance

### 300W

| NME(inter-pupil) | *common*| *challenge* | *full* | *test*|
|:--:|:--:|:--:|:--:|:--:|
|2-HG-flip | 4.0 | - | - | - |

### WFLW

| NME(inter-ocular) |  *test* | *pose* | *illumination* | *occlution* | *blur* | *makeup* | *expression* |
|:--:|:--:|:--:|:--:|:--:|:--:|:--:|:--:|
|2-HG-flip | 5.41 | 10.03 | 5.56 | 5.54 | 6.03 | 7.00 | 6.25 |

## Install

* `Python 3`

* `Install Pytorch >= 0.4 following the official instructions (https://pytorch.org/).`

## data

You need to download images (e.g., 300W) from official websites and then put them into `data` folder for each dataset.

Your `data` directory should look like this:

````
SHN-based-2D-face-alignment
-- data
   |-- afw
   |-- helen
   |-- ibug
   |-- lfpw
````  

## Training and testing 
* For training, stacks = 1, input resolution = 128 
```sh
python main.py 
```
* Run evaluation to get result.
```sh
python main.py --phase test
```
## Citation
If you find this work or code is helpful in your research, please cite:
````
@inproceedings{Xiang2018Score,
  title={Score-Guided Face Alignment Network Under Occlusions},
  author={Xiang Yan and Huabin Wang and Qi Wang and Jinjie Song and Liang Tao},
  booktitle={Chinese Conference on Pattern Recognition and Computer Vision (PRCV)},
  year={2018},
}
````
