Generative Dog Images with DCGAN

This project implements a DCGAN-style Generative Adversarial Network (GAN) to generate synthetic dog images using the Kaggle “Generative Dog Images” dataset.

The goals of the project are to:

Explore the dog image dataset.

Train a DCGAN to model the distribution of dog images.

Generate new, realistic-looking dog images from random noise.

Analyze training behavior and discuss strengths and limitations of the approach.

Dataset: https://www.kaggle.com/c/generative-dog-images

(You must download the data yourself and place it in the data/ folder – it is not included in this repo.)

Project Structure

Suggested layout of the repository:

data/ – NOT tracked in git; Kaggle images go here

all-dogs/ – extracted images from all-dogs.zip

notebooks/

gan_dog_images.ipynb – main notebook (EDA, model, training, results)

models/ – optional saved model weights (ignored by git)

outputs/ – optional generated images, plots, etc. (ignored by git)

venv/ – local virtual environment (ignored by git)

README.md – this file

requirements.txt – Python dependencies

Environment Setup

From the project root:

Create a virtual environment (Windows):

python -m venv venv

Activate the virtual environment:

venv\Scripts\activate

Install dependencies (if requirements.txt exists):

pip install -r requirements.txt

A minimal requirements.txt for this project could contain:

torch

torchvision

torchaudio

matplotlib

numpy

tqdm

jupyter

pillow

Data Setup

Go to the Kaggle competition page “Generative Dog Images”.

Download all-dogs.zip.

Extract it into the data/ folder so you end up with:

data/all-dogs/ containing many .jpg / .png image files.

The dataset is not committed to the repository due to Kaggle’s terms of use; each user must download it individually.

Running the Notebook

Activate the virtual environment (if not already active):

venv\Scripts\activate

Move into the notebooks/ folder:

cd notebooks

Start Jupyter Notebook:

jupyter notebook

Open gan_dog_images.ipynb and run the cells in order:

Section 1: Problem description and data overview

Section 2–3: Exploratory Data Analysis (EDA) and preprocessing

Section 4: DCGAN model (Generator and Discriminator)

Section 5: Training loop

Section 6–7: Results and discussion

Results (High-Level)

The DCGAN learns to generate dog-like images from random noise.

Early epochs produce images that look like colored noise; later epochs begin to show dog shapes, colors, and textures similar to the training set.

Training is sensitive to hyperparameters and can show typical GAN instability, but with reasonable settings (DCGAN defaults) the model produces diverse and recognizable samples.

The notebook includes:

Loss curves for the Generator and Discriminator.

Grids of real dog images vs. generated samples.

A written discussion of limitations and potential improvements.

Possible Extensions

Potential directions to extend this project:

Use more advanced GAN variants such as Wasserstein GAN (WGAN) or WGAN-GP for more stable training.

Train at higher resolutions (for example 128×128 or 256×256).

Incorporate labels or annotations and train a conditional GAN (e.g., by dog breed).

Compare DCGAN with more modern architectures such as StyleGAN or diffusion-based models.
