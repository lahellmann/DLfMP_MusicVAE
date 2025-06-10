# Demo Code for the MusicVAE by [Adam Roberts, Jesse Engel, Colin Raffel, Curtis Hawthorne, Douglas Eck](https://github.com/hoofcas2/MusicVAE)
This repository is a demo code for the course "Deep Learning for Music Processing" at the University of Osnabureck in the summer term 2025.


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
