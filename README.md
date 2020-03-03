# FlashLight CNN
<small>Version 1.0, 2020-02-02</small>
---
Preliminary version: https://arxiv.org/abs/2003.00762

 We propose  a  learning-based  denoising  method called  FlashLight  CNN  (FLCNN)  that  implements  a  deep neural network for image denoising. The proposed approach is based on  deep residual networks and inception  networks and it is able to leverage many more parameters than residual networks alone for denoising grayscale images corrupted by additive  white  Gaussian  noise  (AWGN).  FlashLight  CNN demonstrates  state  of  the  art  performance  when  compared quantitatively  and  visually  with  the  current  state  of  the  art image denoising methods:

## Network Architectures!
FlashLightCNN  is  made  up  two  phases:warm up and boost phases,with a residual skip connection between the input and the output.
 The __warmup__ phase uses only __conventional__ convolutional layers and resembles a __typical__  cnn. The __boost__ phase on the other hand, uses much wider residual inception layers that rapidly increase the number of parameters of the network  while avoiding the dimishing feature reuse that would come with it if only conventional convolutional layers would be employed.

<img src="figures/flashlightCNN.png" width="800px"/>

---
The boost phase implements the customized residual inception layers that designed to maintain the learning capacity of great deep neural networks as show in the figure below


<img src="figures/inception_modules.png" width="400"/>



## Evaluation models!
The models used for valuating can be downloaded  [here](./evaluation_models)


### Result
## Gaussian Denoising
**Performance comparison in terms of PSNR and SSIM on [datasets](./datasets): Set12, BSD68 and Urban100 with noise levels of 15, 25,50. The unavailable values are replaced by ”—”**.
<img src="figures/table1.png" width="900px"/>



