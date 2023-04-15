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
7.  ls 64, lr 0.0005, e 200, decent blacks and white with some gradient but largely same large areas.
8.  ls 64, lr 0.00005, e 50, some variation, some gradiants and bit more spaced out but , very low res looks 8x8 image
9.  ls 64, lr 0.0001, e 500,  increasing epochs not a good idea.
10. ls 32, lr 0.0001. e 75, 64x64, decent results. but mostly white in color with one image having a bit of a mix.
11. ls 64, lr 0.001, e 75, 128x128, much better results compared to the rest. getting some wierd shape of some terrain but low detail
12. ls 128,lr 0.00001 e 75, 128x128, patchy black and white mix color 
    ls 128 not great
13. ls 128,lr 0.0001, e 75, 256x256, decent shapes but nothing good but much better than before
14. ls 128,lr 0.0004, e 75, 256x256, too bright, white is too dominant

NOT BEST ANYMORE
img_shape = 256
input_shape = (img_shape,img_shape,1)
batch_size = 64
ls = 128
e 75
lr 0.001

16. 128, 0.004, 75, 256x256, no all the same and not good
17. 128, 0.002, 75, 256x256, REALLY GOOD 
18. 128, 0.003, 75, 256x256, Nooo, not good.  
19. 128, 0.0009, 75, 256x256, good.  

BEST YET
img_shape = 256
input_shape = (img_shape,img_shape,1)
batch_size = 64
latent_dim = 128
e 200
lr 0.001

