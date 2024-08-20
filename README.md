# Data-Science-competition

# Malaria Detection from Blood Smear Images

## Overview
Malaria is a life-threatening disease caused by parasites that are transmitted to people through the bites of infected female Anopheles mosquitoes. The diagnosis typically involves examining blood smears under a microscope to identify parasitized red blood cells. However, this manual process is time-consuming and requires significant expertise.

This project aims to develop an automatic detection system using machine learning models to classify blood smear images as either "Parasitized" or "Uninfected." The project uses two machine learning approaches: Logistic Regression and Linear SVM, with features extracted using Histogram of Oriented Gradients (HOG).

## Features
- **Automatic Malaria Detection**: Classifies blood smear images into parasitized or uninfected categories.
- **Two Machine Learning Models**: Logistic Regression and Linear SVM for classification.
- **HOG Feature Extraction**: Images are processed using HOG features for robust classification.
- **Streamlit Web Application**: An interactive web app that allows users to upload blood smear images and get predictions.

## Setup and Installation

### Prerequisites
- Python 3.x
- Pip (Python package manager)

### Installation

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/yourusername/malaria-detection.git
   cd malaria-detection


Create a Virtual Environment (optional but recommended):

bash
Copy code
python3 -m venv venv
source venv/bin/activate   # On Windows, use `venv\Scripts\activate`
Install the Required Packages:

bash
Copy code
pip install -r requirements.txt
Download the Dataset:

Ensure that you have the cell_images folder in the project directory containing the blood smear images.
Train the Models:

If you haven't already trained the models, you can do so by running the training script.
bash
Copy code
python train.py
This will generate logistic_model_hog.pkl and svc_model_hog.pkl files.
Running the Application
Run the Streamlit App:

bash
Copy code
streamlit run app.py
Upload Images:

Use the web interface to upload blood smear images.
The application will classify the images as either "Parasitized" or "Uninfected" based on the trained models.
Model Details
Logistic Regression and SVM
The models are trained on HOG features extracted from blood smear images.
Images are resized to 128x64 pixels for consistent feature extraction.
The training dataset is split into 80% training and 20% validation.
HOG Feature Extraction
Image Size: 128x64 pixels
Orientations: 9
Pixels per Cell: 8x8
Cells per Block: 2x2
File Structure
bash
Copy code
├── app.py                  # Main Streamlit app script
├── train.py                # Script to train models
├── README.md               # This file
├── requirements.txt        # Python dependencies
├── cell_images/            # Directory containing blood smear images
├── logistic_model_hog.pkl  # Trained Logistic Regression model
├── svc_model_hog.pkl       # Trained SVM model
└── ...                     # Additional files and scripts
Future Work
Improve the model accuracy by experimenting with different feature extraction techniques and classifiers.
Expand the dataset with more images to improve the model's generalization ability.
Deploy the app on a cloud platform like Heroku or AWS for public use.
