# Generative Dog Images with DCGAN

This project implements a DCGAN-style Generative Adversarial Network (GAN) to generate synthetic dog images using the Kaggle “Generative Dog Images” dataset.

The goals of the project are to:

- Explore the provided dog image dataset  
- Train a DCGAN to learn the distribution of dog images  
- Generate new dog images from random noise  
- Analyze training behavior (loss curves, generated samples)  
- Discuss strengths, limitations, and possible extensions  

Dataset link: https://www.kaggle.com/c/generative-dog-images  
**Note:** The dataset must be downloaded manually and placed inside the `data/` directory.

---

## Project Structure

Recommended repository layout:

generative-dog-images/  
• data/  
 • all-dogs/ (extracted Kaggle images, not tracked)  
• notebooks/  
 • generative-dog-images.ipynb (main notebook)  
• models/ (optional: saved model weights)  
• outputs/ (optional: generated images, plots)  
• venv/ (virtual environment, ignored by git)  
• requirements.txt  
• README.md  

---

## Environment Setup

From the project root:

1. Create a virtual environment (Windows):

    python -m venv venv

2. Activate the virtual environment:

    venv\Scripts\activate

3. Install dependencies (if `requirements.txt` exists):

    pip install -r requirements.txt

A minimal `requirements.txt` for this project could contain:

- torch  
- torchvision  
- torchaudio  
- matplotlib  
- numpy  
- tqdm  
- jupyter  
- pillow  

---

## Data Setup

1. Go to the Kaggle competition page “Generative Dog Images”.  
2. Download `all-dogs.zip`.  
3. Extract it into the `data/` folder so you end up with:

    data/  
    └── all-dogs/  
        ├── image_00001.jpg  
        ├── image_00002.jpg  
        └── ...  

The dataset is **not** committed to the repository due to Kaggle’s terms of use; each user must download it individually.

---

## Running the Notebook

1. Activate the virtual environment (if not already active):

    venv\Scripts\activate

2. Move into the `notebooks/` folder:

    cd notebooks

3. Start Jupyter Notebook:

    jupyter notebook

4. Open `generative-dog-images.ipynb` and run the cells in order:

- Problem description and data overview  
- Exploratory Data Analysis (EDA)  
- Data preprocessing  
- DCGAN model (Generator and Discriminator)  
- Training loop  
- Results and discussion  

---

## Results (High-Level)

- Early epochs produce noisy images (expected for GANs).  
- Later epochs begin to show dog-like shapes, textures, and colors.  
- Generator and Discriminator losses fluctuate but generally indicate adversarial learning.  

The notebook includes:

- Loss curves for the Generator and Discriminator  
- Grids of real vs. generated dog images  
- A written discussion of limitations and potential improvements  

---

## Possible Extensions

Potential directions to extend this project:

- Use more advanced GAN variants such as WGAN or WGAN-GP for more stable training  
- Train at higher resolutions (e.g., 128×128 or 256×256)  
- Incorporate labels or annotations and train a conditional GAN (e.g., by dog breed)  
- Compare DCGAN with more modern architectures such as StyleGAN or diffusion-based models  

Incorporate labels or annotations and train a conditional GAN (e.g., by dog breed).

Compare DCGAN with more modern architectures such as StyleGAN or diffusion-based models.
