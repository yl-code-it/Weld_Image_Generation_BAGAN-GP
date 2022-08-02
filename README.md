# Weld_Image_Generation_BAGAN-GP
Deep Learning on Weld Image Generation using DCGAN and BAGAN-GP

Good/Bad Weld image generation was explored using both DCGAN [1] as baseline model, and a newly proposed BAGAN-GP model in 2021 [2]. As a background, the collected weld images from the automotive production floor were imbalanced and relatively small-scale for defective image dataset. Also, the difference bewteen them are at the local weld seam area. The images could be similar if not pay enough attention.

As a term project attempt of Deep Learning course, deep convolutional Generative adversarial networks (DCGANs) is applied to generate artificial weld data samples. From the testing, for the majority good weld images of size of 900, the DCGANs was able to generate not perfect but quite promissing images. But the DCGANs was not able to generate meaningful images for the minority defetive weld images due to very limit sample size of 117 images. To solve minority and similar image generation problem, therefore, the newly proposed balancing GAN and gradient penalty (BAGAN-GP) in 2021 is utilized herein to generate the minority-class but similar bad weld images.

The main contributions of BAGAN-GP are: using a 'supervised' autoencoder with an intermediate embedding model to disperse the labeled latent vectors, which helps the autoencoder learn the label information directly. Then, use it to initialize the GAN training, which gives the GAN a common knowlege of all classes, even when the different class images are similar, 2. improve the loss function of BAGAN with gradient penalty and build the corresponding architecture of the generator and the discriminator (BAGAN-GP), which ensures a balanced training for each class [2].

References

[1]. Deep Convolutional Generative Adversarial Network. https://www.tensorflow.org/tutorials/generative/dcgan

[2]. Huang, G., Jafari, A.H. Enhanced balancing GAN: minority-class image generation. Neural Comput & Applic (2021). https://doi.org/10.1007/s00521-021-06163-8
