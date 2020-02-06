# FlashLight CNN
**Version 1.0.2, 2020-02-02**
---
 We proposes  the  learning-based  denoising  methodcalled  FlashLight  convolutional  neural  network  (CNN)  or  Flash-Light  CNN  that  implements  deep  neural  networks  for  image  de-noising.  The proposed approach is based on deep convolution andinception  networks  that  are  employed  to  exploit  the  learning  capacity  of  training  very  deep  neural  networks  for  image  Gaussian denoising  problems.   The  quantitative  and  visual  performance  ofproposed  method  are  also  evaluated  and  compared  with  standardand current state of the art method
Preliminary version of the paper: http://arxiv.org/abs/
## Network Architectures!
FlashLightCNN  is  made  up  two  phases:warm up and boost phases,with a residual skip connection between the input and the output.
 The __warmup__ phase uses only __conventional__ convolutional layers and resembles a __typical__  cnn. The __boost__ phase on the other hand, uses much wider residual inception layers that rapidly increase the number of parameters of the network  while avoiding the dimishing feature reuse that would come with it if only conventional convolutional layers would be employed.

<img src="figures/flashlightCNN.png" width="800px"/>

---
The boost phases are composed by two type of residual inception layers that called  inception version  A  and  B.  The  version  B  is based  on  version  A,  with  an  extra  branch  with  adding  one more branch and kernels drawn as dashed boxes showed in the figure below.

<img src="figures/inception_modules.png" width="200"/>



## Evaluation models!
The models used for valuating can be downloaded  [here](./evaluation_models)


### Result
## Gaussian Denoising
**The average PSNR(dB) results of different methods on the set12, BSD60, Urban100 [datasets](./datasets).**

| Dataset  | Sigma | BM3D  | DnCNN | FFDNet | Flashlight CNN |
|----------|-------|-------|-------|--------|----------------|
| Set12    | 15    | 32.41 | 32.87 | 32.77  | 32.97          |
| Set12    | 25    | 30.00 | 30.44 | 30.45  | 30.61          |
| Set12    | 50    | 26.76 | 27.19 | 27.33  | 27.72          |
| BSD68    | 15    | 31.13 | 31.74 | 31.62  | 31.78          |
| BSD68    | 25    | 28.61 | 29.23 | 29.19  | 29.32          |
| BSD68    | 50    | 28.61 | 29.23 | 29.19  | 29.32          |
| Urban100 | 15    | 32.40 | 32.68 | 32.44  | 32.99          |
| Urban100 | 25    | 29.77 | 29.97 | 29.95  | 30.50          |
| Urban100 | 50    | 20.68 | 26.28 | 26.55  | 26.89          |





### Acknowledgements
