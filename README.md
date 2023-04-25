# Dissertation Project on Generative Deep Learning models for Procedural Terrain Generation

## Packages required:  

All the python packages required are given in requirements.txt. Run the below code to install them all. 

```python
pip install -r requirements.txt
```

## Data Pre-processing
Data preprocessing is done [here](./data-processing.ipynb). Images are deleted if their size is less than 305KB, or if they contain more than 50% pixels of extremely dark color (almost black). There is also code for resizing images to test the SSIM scores.

## Terrain Generation

### Deep Learning models:  

#### DCGAN  
The DCGAN code is located in the [DCGAN](./DCGAN.ipynb) file. It consists of importing the packages, initializing hyperparameters, along with different architectures used, most of which have been commented out, followed by adding loss functions and then training the DCGAN. The models trained are saved using the TensorFlow's ``save()`` method.  
There are also code cells for loading the model and generating images using the loaded model for performance testing.  

#### VAE
The VAE code is located in the [VAE](./VAE.ipynb) file. Follows similar pattern of DCGAN.

### Traditional Method
#### Perlin noise
The code for perlin noise is located [here](./PerlinNoise.ipynb). perlin_noise library has been installed which is referenced in the disseration report. Multiple images are generated and plotted which are then used to create 3d models of terrain and for some comparative analysis.

## Testing SSIM Score  
The code for SSIM testing can be found [here](./Similiarity_score.ipynb). The generated images from VAE and DCGAN are located in the test folders (in VAE_generated_images and GAN_generated_images) which are compared to the resized images [located here](./dataset_resized/) from original dataset [located here](./dataset_1/)

