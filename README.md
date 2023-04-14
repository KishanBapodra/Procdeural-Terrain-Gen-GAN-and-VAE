# Honors-Project
Repository for Procedural Terrain Generation using Machine Learning project

GAN:
1.  Tried with 100 epoch 32x32: batch size 64: and learning rate .0001
2.  switched models to use 64x64:
3.  tried 150 epoch:


switched model to use 32x32 with 150 epoch

VAE tried with 
1.  latent space 2 , learning rate default, epochs = 50, got blank image and nan losses tooo high billions 
2.  latent space 2 , learning rate 0.0001, epochs = 50, got some images but very different and losses around 300 and kl loss arouns 0-->5-->6
3.  ls 32, lr 0.0001, e 50, similar results as (2.)
4.  ls 32, lr 0.0001, e 200, not great results, with some almost blank images, and some extremely low res black area white area together images
5.  ls 32, lr 0.001, e 200, decent results compared to before but still not any variation and large patches of either white or black areas and no gradient of those.
6.  ls 128,lr 0.001, e 200, all images were the same. same gray color low res.