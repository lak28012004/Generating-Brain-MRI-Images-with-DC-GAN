🧠 Brain Tumor Detection using GANs
📌 Overview

A brain tumor is a mass of abnormal cells in the brain. Since the skull is rigid, any abnormal growth can increase intracranial pressure and potentially become life-threatening.

Brain tumors are classified as:

Primary Tumor – Originates in the brain (often benign)

Secondary Tumor (Metastatic) – Spreads to the brain from other organs such as lung or breast

🩺 Diagnosis – MRI (Magnetic Resonance Imaging)

MRI is the preferred imaging technique for brain tumor detection.

Uses magnetic fields to generate detailed brain images

Contrast dye improves clarity

More detailed than CT scans

Helps measure tumor size and spread within CNS

<div align="center"> <img src="images/mri_scan_example.jpg" width="500"/> </div>
📊 The Numbers (India Statistics)

40,000 – 50,000 new brain tumor cases annually

20% are children

Affects only 0.0035% of the total population

This creates a class imbalance problem in Machine Learning:

In 10,000 MRI scans → only ~35 positive tumor cases

Majority samples are non-tumor

⚠️ This imbalance leads to:

Biased models

Poor generalization

Reduced sensitivity

Source: Economic Times Health

🤖 Proposed Solution – Generative Modelling

To address class imbalance, we use Generative Models.

Generative models learn the underlying data distribution and generate new synthetic samples to augment limited datasets.

🔥 Generative Adversarial Networks (GANs)

GANs consist of two neural networks competing against each other:

Generator

Discriminator

<div align="center"> <img src="images/gan_architecture.png" width="600"/> </div>
⚙️ Generator

Takes random noise (z)

Generates synthetic MRI images

Attempts to mimic real tumor MRI distribution

🕵️ Discriminator

Receives real + generated samples

Outputs probability (0 → Fake, 1 → Real)

Learns to distinguish real vs synthetic images

🎯 How GANs Work

Random noise → Generator

Generator creates fake MRI image

Real MRI + Fake MRI → Discriminator

Discriminator evaluates authenticity

Generator improves through feedback

This process continues until generated images closely resemble real tumor MRI scans.

🧮 Minimax Loss Function

GANs operate under a minimax optimization:

Generator → Minimize loss

Discriminator → Maximize loss
The objective:

min_G max_D V(D, G)

Where:

G tries to fool D

D tries to correctly classify real vs fake
💡 Why GANs for Brain Tumor Detection?

✅ Solve class imbalance
✅ Generate synthetic tumor MRI data
✅ Improve model generalization
✅ Enhance diagnostic AI performance

🛠 Tech Stack

Python

TensorFlow / PyTorch

OpenCV

MRI Dataset

📌 Future Improvements

Conditional GANs

Data augmentation pipeline

Integration with CNN classifier

Deployment as web-based diagnostic tool
📎 Project Structure
Brain-Tumor-GAN/
│
├── dataset/
├── models/
├── training/
├── images/
├── notebooks/
└── README.md
📢 Conclusion

Brain tumor detection suffers from severe data imbalance.
Using GAN-based generative modeling, we can synthetically expand tumor datasets and build more robust diagnostic systems.
