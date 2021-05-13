# Fast Monte Carlo Rendering via Multi-Resolution Sampling

### Paper | Data

PyTorch implementation of fast Monte Carlo rendering via multi-resolution sampling.<br><br>
Fast Monte Carlo Rendering via Multi-Resolution Sampling, <br>
 [Qiqi Hou](https://hqqxyy.github.io/) \*<sup>1</sup>,
 Zhan Li\*<sup>1</sup>,
 Carl S Marshall<sup>2</sup>,
 Selvakumar Panneer<sup>2</sup>,
 [Feng Liu](http://web.cecs.pdx.edu/~fliu/) <sup>1</sup>, <br>
 <sup>1</sup>Portland State University, <sup>2</sup>Intel 
 
in Graphic Interface 2021.

<img src="figures/fig1-a.png"> 


## What is a MSSPL?

MultiScale-SamPLing (MSSPL) is a hybrid rendering method to speed up Monte Carlo rendering algorithms.
Our method first generates two versions of a rendering: one at a low resolution 
with a high sample rate (LRHS) and the other at a high resolution with a low sample rate (HRLS). 
We then develop a deep convolutional neural network to fuse these two renderings into a high-quality image 
as if it were rendered at a high resolution with a high sample rate. Specifically, we formulate this fusion task 
as a super resolution problem that generates a high resolution rendering from a low resolution input (LRHS), 
assisted with the HRLS rendering. The HRLS rendering provides critical high frequency details which are difficult 
to recover from the LRHS for any super resolution methods. 

Traing a MSSPL takes between five days and one week and only requires a single GPU. 
Denoising an 1024*1024 image from an optimized MSSPL takes about 0.12 second for our x4 model on a Titan Xp.

<img src="figures/net.png"> 

### Training 
We will release our training code.

### Inference Demo
We will release a demo code for inference.

### Replicating the paper results
We will release our code, models and our results. 

## BCR Dataset
We will release the whole dataset as well as the compared results on our dataset.

<img src="figures/bcr.png"> 

## Citation
```
@inproceedings{hou2021msspl,
  title={Fast Monte Carlo Rendering via Multi-Resolution Sampling},
  author={Qiqi Hou, Zhan Li, Carl S Marshall, Selvakumar Panneer, Feng Liu},
  year={2021},
  booktitle={Graphic Interface},
}
```

## Acknowledgments
The source models in figures are used under a Creative Commons License from kujaba, 
darkst0ne, cczero, LukeLiptak, Christophe Seux, nickbrunner, samytichadou, MarcoD, Jay-Artist, 
jgilhutton, Oldfrizt, Ndakasha, GyngaNynja, racingfoli, Kless and PepSu. 
This project is supported by a gift from Intel. Thanks for their help.