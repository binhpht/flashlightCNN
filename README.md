# FlashLight CNN
<small>Version 1.0.2, 2020-02-02</small>
---
 We propose  a  learning-based  denoising  methodcalled  FlashLight  CNN  (FLCNN)  that  implements  a  deepneural network for image denoising. The proposed approachis based on  deep residual networks and inception  networksand it is able to leverage many more parameters than residualnetworks alone for denoising grayscale images corrupted byadditive  white  Gaussian  noise  (AWGN).  FlashLight  CNNdemonstrates  state  of  the  art  performance  when  comparedquantitatively  and  visually  with  the  current  state  of  the  artimage denoising methods:
 http://arxiv.org/abs/
## Network Architectures!
FlashLightCNN  is  made  up  two  phases:warm up and boost phases,with a residual skip connection between the input and the output.
 The __warmup__ phase uses only __conventional__ convolutional layers and resembles a __typical__  cnn. The __boost__ phase on the other hand, uses much wider residual inception layers that rapidly increase the number of parameters of the network  while avoiding the dimishing feature reuse that would come with it if only conventional convolutional layers would be employed.

<img src="figures/flashlightCNN.png" width="800px"/>

---
The boost phase implements the customized residual inception layers that designed to maintain the learning capacity of great deep neural networks as show in the figure below


<img src="figures/inception_modules.png" width="200"/>



## Evaluation models!
The models used for valuating can be downloaded  [here](./evaluation_models)


### Result
## Gaussian Denoising
**Performance comparison in terms of PSNR and SSIM on [datasets](./datasets): Set12, BSD68 and Urban100 . with noise levels of 15, 25,50. The unavailable values are replaced by ”—”**.

| dataset  | sigma | flashlightcnn PSRN | flashlight SSIM | dncnn PSRN  | dncnn SSIM| ffdnet PSRN| ffdnet SSIM | bm3d PSRN  | bm3d SSIM | ircnn PSRN  | ircnn SSIM | hrlnet | hrlnetssim |
|----------|-------|---------------|-------------------|--------|-----------|--------|------------|--------|----------|--------|-----------|--------|------------|
| set12    | 15    | 32\.97        | 0\.9053           | 32\.87 | 0\.9030   | 32\.77 | 0\.9033    | 32\.41 | 0\.8959  | 32\.77 | 0\.9009   | \-     | \-         |
| set12    | 25    | 30\.66        | 0\.8673           | 30\.44 | 0\.8616   | 30\.45 | 0\.8639    | 30\.00 | 0\.8505  | 30\.38 | 0\.8597   | 30\.46 | 0\.8368    |
| set12    | 50    | 27\.51        | 0\.7955           | 27\.19 | 0\.7822   | 27\.33 | 0\.7896    | 26\.76 | 0\.7660  | 27\.14 | 0\.7795   | 27\.29 | 0\.7369    |
| bsd68    | 15    | 31\.78        | 0\.8928           | 31\.74 | 0\.8908   | 31\.62 | 0\.8902    | 31\.13 | 0\.8741  | 31\.63 | 0\.8881   | \-     | \-         |
| bsd68    | 25    | 29\.33        | 0\.8326           | 29\.23 | 0\.8279   | 29\.19 | 0\.8290    | 28\.61 | 0\.8024  | 29\.14 | 0\.8247   | 29\.14 | 0\.8238    |
| bsd68    | 50    | 26\.40        | 0\.7291           | 26\.23 | 0\.7183   | 26\.30 | 0\.7242    | 25\.69 | 0\.6881  | 26\.18 | 0\.7162   | 26\.16 | 0\.7143    |
| urban100 | 15    | 33\.02        | 0\.9323           | 32\.68 | 0\.9250   | 32\.44 | 0\.9277    | 32\.40 | 0\.9232  | 32\.49 | 0\.9244   | \-     | \-         |
| urban100 | 25    | 30\.53        | 0\.8962           | 29\.97 | 0\.8789   | 29\.95 | 0\.8895    | 29\.77 | 0\.8790  | 29\.82 | 0\.8839   | \-     | \-         |
| urban100 | 50    | 27\.05        | 0\.8183           | 26\.28 | 0\.7864   | 26\.55 | 0\.8060    | 26\.08 | 0\.7797  | 26\.24 | 0\.7927   | \-     | \-         |





