# Demo Code for the MusicVAE by [Adam Roberts, Jesse Engel, Colin Raffel, Curtis Hawthorne, Douglas Eck](https://github.com/hoofcas2/MusicVAE)
This repository is a demo code for the course "Deep Learning for Music Processing" at the University of Osnabureck in the summer term 2025.

## Introduction to MusicVAE
MusicVAE is a machine learning model developed by researchers at Google (Magenta) that uses a variational autoencoder (VAE) to generate and transform music.
It learns a compressed (latent) representation of music. With this it can then generate new music, reconstruct music, or interpolate between two musical sequences.
It works especially well with long-term musical structure, like full melodies or multi-instrument tracks.

Music VAE trains on MIDI data to learn musical patterns, then encodes sequences into a latent space (like musical DNA) and afterwards decodes those latent vectors back into music.
this gives opportunity to be able to interpolate between songs, or manipulate style, tempo, structure, etc.

## Available google colab by Roberts et al.
This is a [copy](https://colab.research.google.com/drive/1tScO5apGPsOnqscjA_IMRyVdkr8uE8qn?usp=sharing) of the provided google colab that I debugged for easy usage.

## Setup Instructions

### 1. Clone the Base Repository

```bash
git clone https://github.com/hoofcas2/MusicVAE.git
cd MusicVAE
```

### 2. Set Up Python Environment

#### Option A: Using `venv`

```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
pip install --upgrade pip
pip install -r requirements.txt
```

#### Option B: Using `conda`

```bash
conda create -n musicvae python=3.7 -y
conda activate musicvae
pip install -r requirements.txt
```

### 3. Install Magenta

```bash
pip install magenta
```

### 4. Download Pretrained Model

```bash
mkdir -p MusicVAE/checkpoints/hier-mel_16bar
cd MusicVAE/checkpoints/hier-mel_16bar
wget https://storage.googleapis.com/magentadata/models/music_vae/checkpoints/hier-mel_16bar.tar
tar -xvf hier-mel_16bar.tar
```

## Usage

Open `main.ipynb` to start using pretrained models or training your own. It uses the provided modules:
- `generate.py`
- `train.py`
- `preprocess.py`
 ## References
 [1] Roberts, A., Engel, J., Raffel, C., Hawthorne, C., & Eck, D. (2019). A Hierarchical Latent Vector Model for Learning Long-Term Structure in Music. arXiv [Cs.LG]. Retrieved from http://arxiv.org/abs/1803.05428
