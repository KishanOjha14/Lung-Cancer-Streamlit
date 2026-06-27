# Lung Cancer Detection System 🫁

[![Python Version](https://img.shields.io/badge/python-3.7%2B-blue.svg)](https://www.python.org/downloads/)
[![Streamlit](https://img.shields.io/badge/Streamlit-1.18.0-FF4B4B.svg)](https://streamlit.io/)
[![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-FF6F00.svg)](https://www.tensorflow.org/)
[![License](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)

A comprehensive Web Application built with **Streamlit** that utilizes Machine Learning and Deep Learning to predict the likelihood of Lung Cancer. The application features predictive models based on both patient tabular data and CT-Scan images.

## 🌟 Features

### 1. Comprehensive Educational Dashboard (`Introduction`)
*   **Awareness & Statistics:** Demystifies common misconceptions about lung cancer using real-world statistics from the American Cancer Society.
*   **Beyond Smoking:** Educates users on the significant impact of environmental and genetic factors (like air pollution and indoor stove usage). Backed by cited research studies from institutions like Tata Memorial Hospital and AIIMS, it emphasizes that smoking is not the sole cause of the disease.

### 2. In-Depth Dataset & Model Analysis (`About the Dataset`)
Features a multi-tab interface providing full transparency into the data and models used:
*   **Data Preview & Correlation:** Displays the raw data structure (features like 'Dust Allergy', 'Genetic Risk', 'Occupational Hazards') and visualizes a Pearson Correlation Matrix to identify attributes that most significantly impact model performance.
*   **Algorithm Performance:** Showcases the evaluation metrics and confusion matrices for the implemented supervised learning algorithms (Linear Regression, SVM, KNN, Decision Tree), noting their high accuracy on the test sets.
*   **CNN Architecture Breakdown:** Explains the inner workings of the 2D Convolutional Neural Network used for image processing. It includes model summaries, training vs. validation accuracy/loss plots, and hyperparameter details (RMSprop optimizer, binary crossentropy).

### 3. Interactive ML Prediction Engine (`Lung Cancer Prediction`)
*   **Personalized Risk Assessment:** Allows users to input 17 distinct health and lifestyle parameters (e.g., Age, Gender, Fatigue, Shortness of Breath, Swallowing Difficulty, Snoring) through an intuitive form.
*   **Real-time Classification:** Utilizes a pre-trained Machine Learning model (loaded via `pickle`) to instantly evaluate the inputs and classify the patient's risk level, providing alerts for 'High', 'Medium', or 'Low/No' risk of lung disease. Includes a handy slider to auto-fill sample data from the test set for quick demonstration.

### 4. Advanced Deep Learning Image Analysis (`CNN Based disease Prediction`)
*   **CT-Scan Upload & Processing:** Features a secure file uploader where users can submit chest CT-Scan images (`png`, `jpeg`, `jpg`).
*   **Neural Network Inference:** A custom-trained Keras/TensorFlow CNN model preprocesses the uploaded image and performs a real-time binary classification. It outputs a clear, human-readable percentage confidence score predicting whether the scan indicates a 'Normal' case or a potential 'Lung Cancer' case.

## 🛠️ Technologies & Libraries Used

*   **Programming Language:** Python
*   **Web Framework:** Streamlit (`streamlit`, `streamlit-option-menu`)
*   **Machine Learning:** Scikit-Learn (`scikit-learn`)
*   **Deep Learning:** TensorFlow & Keras (`tensorflow`)
*   **Data Manipulation:** Pandas (`pandas`), NumPy (`numpy`)
*   **Data Visualization:** Matplotlib (`matplotlib`), Seaborn (`seaborn`)
*   **Image Processing:** Pillow (`PIL`)

## 📂 Project Structure

```text
Lung-Cancer-Streamlit/
│
├── app.py                   # Main Streamlit application script
├── requirements.txt         # Project dependencies
├── models/                  # Directory containing pre-trained models
│   ├── final_model.sav      # Trained ML model for tabular data (e.g., SVM)
│   └── keras_model.h5       # Trained CNN model for CT-Scan images
├── datasets/                # Directory containing CSV datasets for training/testing
│   ├── data.csv
│   ├── train.csv
│   └── ...
├── images/                  # Static images used in the UI (graphs, banners)
└── ctscan_images/           # Sample CT-Scan images (if applicable)
```

## 🚀 Getting Started

Follow these steps to run the project locally on your machine.

### 1. Prerequisites

Ensure you have Python installed (preferably version 3.7 or higher).

### 2. Clone the Repository

```bash
git clone https://github.com/KishanOjha14/Lung-Cancer-Streamlit.git
cd Lung-Cancer-Streamlit
```

### 3. Install Dependencies

It is recommended to create a virtual environment before installing the dependencies.

```bash
# Create a virtual environment (optional but recommended)
python -m venv venv
source venv/bin/activate  # On Windows use: venv\Scripts\activate

# Install the required packages
pip install -r requirements.txt
```

### 4. Run the Application

Start the Streamlit server to run the web application.

```bash
streamlit run app.py
```

The application will automatically open in your default web browser at `http://localhost:8501`.

## 🧠 Machine Learning Algorithms

The project explores several supervised learning algorithms for tabular data classification:
*   Support Vector Machine (SVM)
*   Decision Tree Classifier
*   K-Nearest Neighbours (KNN)
*   Linear Regression

The deep learning model for image classification utilizes a **Convolutional Neural Network (CNN)** with 2D Convolution and MaxPooling layers, ending with a sigmoid activation function for binary classification (Cancer vs. Normal).

## 📸 Screenshots

*(You can add screenshots of your running application here to make your README more appealing)*

## 🤝 Contributing

Contributions, issues, and feature requests are welcome! Feel free to check the [issues page](https://github.com/KishanOjha14/Lung-Cancer-Streamlit/issues).

## 📝 License

This project is open-source and available under the [MIT License](LICENSE).
