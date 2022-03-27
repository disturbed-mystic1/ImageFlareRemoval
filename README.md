# ImageFlareRemoval

## Introduction

Photographs of scenes taken under a strong light source usually result in some undulating artifacts called lens flares. Lens flares have long been a problem for photographers and engineers with many great attempts at eliminating the problem but rather falling quite short. With the advent of deep learning, novel techniques have been proposed to tackle this issue. Our project proposes a simple Image-to-Image translation model trained to generalize on previously unseen data and compare it with other models.Photographs of scenes taken under a strong light source usually result in some undulating artifacts called lens flares. Lens flares have long been a problem for photographers and engineers with many great attempts at eliminating the problem but rather falling quite short. With the advent of deep learning, novel techniques have been proposed to tackle this issue. Our project proposes a simple Image-to-Image translation model trained to generalize on previously unseen data and compare it with other models.

## Problem Definiton

This project aims to tackle the issue of image flaring normally seen in daylight photos. These flare patterns depend on the optics of the lens, size of the aperture, and imperfections. This leads to a diverse pattern of flares, which are usually difficult to tackle. Previously used image-processing techniques naively relied on template matching and intensity thresholding to localize the flare artifact.

## Objectives

• To collect natural and synthetic flare-free images and apply artificial flare artifacts to them using image processing and blending techniques. Make matching paired   images (ground-truth, mask) using python file management libraries
• To use transfer learning to extract features and help the algorithm to localize flares and not just the light source. To train our GAN to help remove flares.
• To compare our work using metrics such as PSNR/SSIM with preexisting techniques.

## Methodology

• Creating a Synthetic Dataset with paired ground truth and flared images and loading the images together.
• Applying Pre-Processing techniques to resize the images into the right format and apply transformation and sampling techniques
• Extracting Features from the flared image using transfer learning techniques like ResNet/VGG-16 to prevent losing features like sunlight or other light sources and     just eliminating the flares.
• These extracted features are then fed as an input to an Encoder-Decoder Model called U-net using Patch GAN as a discriminator. The generated images are compared with   the ground truth images with metrics like PSNR and SSIM. Further, these results are compared with other models.

## References

[1]
Wu, Y., He, Q., Xue, T., Garg, R., Chen, J., Veeraraghavan, A., & Barron, J. T. (2021). How to train neural networks for flare removal. In Proceedings of the IEEE/CVF International Conference on Computer Vision (pp. 2239-2247).
[2]
Chen, L. C., Zhu, Y., Papandreou, G., Schroff, F., & Adam, H. (2018). Encoder-decoder with atrous separable convolution for semantic image segmentation. In Proceedings of the European conference on computer vision (ECCV) (pp. 801-818).
[3]
Mehri, A., Ardakani, P. B., & Sappa, A. D. (2021). MPRNet: Multi-path residual network for lightweight image super resolution. In Proceedings of the IEEE/CVF Winter Conference on Applications of Computer Vision (pp. 2704-2713).
[4]
Qin, X., Wang, Z., Bai, Y., Xie, X., & Jia, H. (2020, April). FFA-Net: Feature fusion attention network for single image dehazing. In Proceedings of the AAAI Conference on Artificial Intelligence (Vol. 34, No. 07, pp. 11908-11915)
[5]
Chen, L., Lu, X., Zhang, J., Chu, X., & Chen, C. (2021). HINet: Half instance normalization network for image restoration. In Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition (pp. 182-192).
[6]
Lee, Y. W., Wong, L. K., & See, J. (2020, October). Image Dehazing With Contextualized Attentive U-NET. In 2020 IEEE International Conference on Image Processing (ICIP) (pp. 1068-1072). IEEE.
[7]
Qiao, X., Hancke, G. P., & Lau, R. W. (2021). Light Source Guided Single-Image Flare Removal From Unpaired Data. In Proceedings of the IEEE/CVF International Conference on Computer Vision (pp. 4177-4185).
[8]
Fan, Q., Yang, J., Hua, G., Chen, B., & Wipf, D. (2017). A generic deep architecture for single image reflection removal and image smoothing. In Proceedings of the IEEE International Conference on Computer Vision (pp. 3238-3247).
[9]
Zhang, X., Ng, R., & Chen, Q. (2018). Single image reflection separation with perceptual losses. In Proceedings of the IEEE conference on computer vision and pattern recognition (pp. 4786-4794).
[10]
Demir, U., & Unal, G. (2018). Patch-based image inpainting with generative adversarial networks. arXiv preprint arXiv:1803.07422.
[11]
Cho, K., Van Merriënboer, B., Bahdanau, D., & Bengio, Y. (2014). On the properties of neural machine translation: Encoder-decoder approaches. arXiv preprint arXiv:1409.1259.
