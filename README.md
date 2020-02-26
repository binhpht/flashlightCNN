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
