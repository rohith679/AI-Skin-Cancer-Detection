DermaDetect AI: A Quantum-Inspired Skin Lesion Advisor

![alt text](https-to-your-project-demo.gif)
<!-- It is HIGHLY recommended to record a short GIF of your app working and place it here. -->

An advanced deep learning web application for the classification of skin lesions, focusing on accuracy, robustness, and fairness. This project introduces Q-ConvNeXt, a novel, quantum-inspired classical architecture that demonstrates superior generalization and reliability compared to a state-of-the-art baseline.

📋 Table of Contents

About The Project

Key Features

Built With

Getting Started

Prerequisites

Installation & Setup

Model Architecture

Dataset

Results

Roadmap

License

Contact

📖 About The Project

While standard deep learning models have achieved high accuracy in classifying skin cancer, they often fail in real-world scenarios due to a lack of robustness and fairness. These models can be brittle, easily fooled by confounding visual artifacts (like rulers or ink marks in an image), and often underperform on diverse populations.

This project tackles these challenges head-on by introducing the Quantum-Inspired Tensor Module (QITM), a new deep learning layer that runs on classical GPUs but uses the mathematics of quantum tensor networks to create a more holistic and resilient understanding of image features.

The result is a complete full-stack application featuring:

A Python/Flask backend that serves a state-of-the-art, robust AI model.

A responsive React frontend that provides a seamless user experience for uploading images and interpreting the complex results in a safe, clear, and actionable way.

This work aims to be a blueprint for building next-generation medical AI that is not just accurate, but genuinely trustworthy.

✨ Key Features

High-Accuracy Classification: Differentiates between 4 key classes: Melanoma, Nevus, Seborrheic Keratosis, and Healthy Skin with state-of-the-art performance.

Proven Robustness: Rigorously tested against a corrupted dataset with visual artifacts to prove its resilience to "shortcut learning."

Explainable AI (XAI): Generates a heatmap (Grad-CAM) to visualize exactly where the AI is focusing, providing transparency into its decision-making process.

Safe OOD Rejection: Intelligently identifies and rejects irrelevant (Out-of-Distribution) images by analyzing its own prediction confidence.

Hair Removal Preprocessing: Automatically and digitally "shaves" images using the DullRazor algorithm to remove confounding hair structures before analysis.

Interactive Chatbot: An offline, rule-based assistant to answer common questions about the AI's findings.

Risk Assessment Quiz: A guided questionnaire to help users understand general skin cancer risk factors.

Fully Responsive UI: A seamless experience on both desktop and mobile devices.

🛠️ Built With

This project is a full-stack application built with modern technologies.

Backend:

Python

Flask

PyTorch

timm (PyTorch Image Models)

OpenCV

scikit-learn

Frontend:

React

Vite

Axios

CSS3

🚀 Getting Started

To get a local copy up and running, follow these simple steps.

Prerequisites

Make sure you have the following installed:

Git

Python (version 3.9+) & pip

Node.js & npm

Installation & Setup

Clone the repository:

git clone https://github.com/your_username/your_project_repository.git
cd your_project_repository

Setup the Backend:

cd backend

# Create a virtual environment (recommended)
python -m venv venv
source venv/bin/activate  # On Windows, use `venv\Scripts\activate`

# Install Python packages
pip install -r requirements.txt

# IMPORTANT: Place your trained model file in the `models` directory
# The file should be named `q_convnext_best.pth`

# Run the Flask server
python app.py

The backend will now be running on http://127.0.0.1:5000.

Setup the Frontend:
Open a new terminal.

cd frontend

# Install NPM packages
npm install

# Run the development server
npm run dev

The frontend will now be running on http://localhost:5173 (or another port). Open this URL in your browser.

🧠 Model Architecture

The core of this project is a scientific comparison between two models:

Baseline ConvNeXt: A standard, state-of-the-art convnext_base model. It represents the current gold standard.

Q-ConvNeXt (Ours): Our novel architecture. It uses the same ConvNeXt backbone but replaces the standard feature pooling with our custom Quantum-Inspired Tensor Module (QITM). This module fuses features from all four stages of the backbone, allowing it to learn a more robust and holistic representation of the lesion.

Both models are trained and evaluated on the same data to provide a direct, fair comparison of their performance, generalization, and robustness.

📊 Dataset

This project was trained and validated using a combination of four distinct, publicly available datasets, each with a specific purpose:

Main Training & Test Set (ISIC Archive): A large-scale dataset of over 12 GB used to train the core visual understanding of the models.

Fairness Benchmark Set (PAD-UFES-20): Used to perform a critical analysis of model performance across different skin tones, highlighting the real-world challenge of data bias.

Adversarial Texture Set: A curated set of non-skin images with skin-like colors (e.g., rust, wood) used to test the model's robustness against "shortcut learning."

Out-of-Distribution Set (COCO): A set of random, irrelevant images (cats, dogs, cars) used to test the model's ability to safely reject inputs it was not trained on.

📈 Results

Our experiments yielded a clear and powerful story. The Q-ConvNeXt model demonstrated superior performance and reliability.

Metric	Baseline ConvNeXt	Q-ConvNeXt (Ours)
Test Accuracy	92.66%	93.23%
Melanoma Recall	95.15%	95.72%
Overfitting Gap	5.38%	4.43%
Robustness Drop	-2.4%	-0.2%

The key finding is that Q-ConvNeXt not only achieves higher accuracy and better cancer detection (Recall) but also generalizes better (smaller overfitting gap) and is more robust to confounding artifacts.

🗺️ Roadmap

This project serves as a strong foundation. Future work could explore:

Multi-Modal Input: Integrate patient metadata (age, location) to create a "Project v4" model for even higher reliability.

Uncertainty Quantification: Implement Monte Carlo Dropout to provide a "confidence score" for each prediction.

Self-Supervised Pre-training: Use the large ISIC dataset to pre-train the model on skin textures before fine-tuning on specific lesion types.

📄 License

Distributed under the MIT License. See LICENSE for more information.

📧 Contact

Your Name - @your_twitter - your.email@example.com

Project Link: https://github.com/your_username/your_project_repository
