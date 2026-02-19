🧠 MRI Brain Tumor Image Generation using GANs
<p align="center"> <img src="https://img.shields.io/badge/Domain-Medical%20AI-green"/> <img src="https://img.shields.io/badge/Model-GAN-blue"/> <img src="https://img.shields.io/badge/Framework-PyTorch%20%7C%20TensorFlow-orange"/> <img src="https://img.shields.io/badge/Status-Research%20Project-success"/> </p>
📌 Overview

Brain tumor MRI datasets often suffer from class imbalance, where tumor-positive scans are significantly fewer than normal scans. This imbalance negatively impacts deep learning model performance.

This project leverages Generative Adversarial Networks (GANs) to generate realistic synthetic brain tumor MRI images for dataset augmentation and improved model robustness.

The system demonstrates the practical application of generative deep learning in healthcare AI.

🖼️ Sample Results
🧾 Original MRI Scan
<div align="center"> <img src="image-01-differentes-coupes-axiales.jpg" width="450"/> </div>
🔥 GAN Generated MRI Image
<div align="center"> <img src="images.jpg" width="450"/> </div>
🏗️ Methodology

The model follows the adversarial training paradigm:

Random Noise (z)
        ↓
Generator Network
        ↓
Synthetic MRI Image
        ↓
Discriminator (Real vs Fake)
        ↓
Adversarial Optimization
🔁 Training Strategy

Generator learns to produce realistic tumor MRIs

Discriminator learns to classify real vs fake images

Both networks improve iteratively through adversarial loss

🧠 Key Features

✔ GAN-based MRI tumor image synthesis

✔ Reduces dataset imbalance

✔ Enhances training data diversity

✔ Modular training pipeline

✔ Scalable for other medical imaging domains

🛠️ Tech Stack

Programming: Python

Deep Learning: PyTorch / TensorFlow

Data Processing: NumPy, OpenCV

Visualization: Matplotlib

⚙️ Installation & Setup
1️⃣ Clone Repository
git clone https://github.com/yourusername/mri-gan-generator.git
cd mri-gan-generator
2️⃣ Install Dependencies
pip install -r requirements.txt
3️⃣ Train the Model
python train.py
4️⃣ Generate Synthetic MRI Images
python generate.py

Generated outputs will be stored in:

outputs/
📂 Project Structure
MRI-GAN/
│
├── dataset/              # MRI dataset (training images)
├── models/               # Generator & Discriminator architectures
├── train.py              # Model training script
├── generate.py           # Synthetic image generation script
├── outputs/              # Generated MRI images
├── requirements.txt      # Project dependencies
└── README.md             # Project documentation
🎯 Project Objectives

Address class imbalance in medical datasets

Improve robustness of tumor detection models

Apply GANs in healthcare AI

Demonstrate practical generative modeling skills

📈 Future Enhancements

Conditional GAN (cGAN) for tumor type control

DCGAN / StyleGAN architecture experimentation

Integration with tumor classification pipeline

Quantitative evaluation (FID Score, SSIM, PSNR)

📌 Conclusion

This project demonstrates how Generative Adversarial Networks (GANs) can enhance medical imaging datasets by generating realistic synthetic brain tumor MRIs.

It highlights the practical potential of generative AI in healthcare, improving dataset quality and enabling more robust diagnostic AI systems.
