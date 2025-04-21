# 🎨 Monet Style Transfer using CycleGAN

This project is part of a weekly mini-project focused on generative deep learning using GANs. The goal is to convert real-world photos into Monet-style paintings using a CycleGAN model.

## 🚀 Project Overview

- **Competition**: [Kaggle - GANs Getting Started (Monet Paintings)](https://www.kaggle.com/competitions/gan-getting-started)
- **Goal**: Transform photo images into Monet-style artwork using CycleGAN.
- **Evaluation Metric**: MiFID (Memorization-informed Fréchet Inception Distance)

---

## 📁 Dataset Structure

Kaggle provides four folders:

├── monet_jpg # Contains 1072 Monet images ├── photo_jpg # Contains 6,287 real photo images ├── monet_tfrecord # TFRecord version of Monet images ├── photo_tfrecord # TFRecord version of photo images

yaml
Copy
Edit

All images are `256x256` JPGs.

---

## 📊 Exploratory Data Analysis (EDA)

- Displayed samples from both domains (Photo & Monet)
- Verified dimensions, file counts, and image shapes
- Checked normalization and preprocessing strategies

---

## 🧠 Model Architecture

### CycleGAN

CycleGAN is used to learn mappings between two image domains **X** (Photos) and **Y** (Monet paintings) without paired examples. It uses:

- **Two Generators**: `G: X → Y` and `F: Y → X`
- **Two Discriminators**: `D_Y` and `D_X`
- **Cycle Consistency Loss**: Ensures that translating from one domain and back yields the original image
- **Identity Loss**: Helps preserve color and content when needed

---

## 🏋️ Training Strategy

- Image normalization to `[-1, 1]`
- Batched datasets
- Trained for multiple epochs using Adam optimizer
- Used adversarial loss, cycle consistency loss, and identity loss

---

## 🧪 Evaluation & Results

- Generated 100 Monet-style images from photos using the trained generator
- Packaged generated outputs into `images.zip` for Kaggle submission
- Visual inspection shows effective style transfer
- MiFID score computed upon submission

---

## 📁 Project Structure

. ├── notebooks/ │ └── monet_cyclegan_training.ipynb # Full training & EDA ├── images.zip # Generated images for submission ├── 

## 📸 Example Results

| Original Photo | Generated Monet |
|----------------|-----------------|
| ![](examples/photo.jpg) | ![](examples/monet.jpg) |

---

## ✅ Deliverables

- ✅ Jupyter notebook with EDA, model training, and visualization
- ✅ GitHub repo with full code and README
- ✅ Kaggle submission `images.zip` with generated samples

---

## 👨‍💻 Author

*Deepakraj E*  
*Mini-Project for Deep Learning Course*
