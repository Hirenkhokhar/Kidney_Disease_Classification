
# Kidney Disease Classification

## Dataset
- **Dataset Link**: [Kidney Disease Dataset](https://drive.google.com/file/d/1wmWnb1EPs3sN9Cy1KM28mOuTs1BkbjN2/view?usp=sharing)
- **Normal Images**: 240
- **Tumor Images**: 225
- **Image Size**: 224x224 pixels
- **Train-Test Split**: 80% training, 20% testing

## Problem Statement
This project builds a kidney tumor detection system using a CNN based on VGG16 for binary classification: "Normal" (no tumor) and "Tumor" (tumor present).

## Model Architecture
- **Base Model**: VGG16 (pre-trained on ImageNet)
- **Custom Layers**: Flatten, Dense (256 neurons, ReLU), Dropout (0.5), Output (Sigmoid)

## Training Details
- **Loss**: Binary Cross-Entropy
- **Optimizer**: Adam (lr=0.001)
- **Batch Size**: 16
- **Epochs**: 25 (early stopping based on validation accuracy)

## Tools & Technologies
- **Frameworks**: TensorFlow, Keras
- **Libraries**: NumPy, Matplotlib, OpenCV
- **Hardware**: GPU

## Challenges
- **Class Imbalance**: Addressed with class weights
- **Overfitting**: Mitigated with dropout and early stopping
- **Limited Data**: Overcame with transfer learning

## Results
- **Accuracy**: 96%
- **Precision**: 95%
- **Recall**: 97%
- **F1-Score**: 96%

## How to Run

### STEPS:
1. **Clone the repository**:
   https://github.com/Hirenkhokhar/Kidney_Disease_Classification.git
   
2. **Create a conda environment**: `.env`
   
3. **Install the requirements**: `requirements.txt`

4. **Run the app**: `main.py`

### MLflow Setup:
- Run `mlflow ui` to start the UI.
- For DAGSHub:  

### DVC Setup:
1. `dvc init`
2. `dvc repro`
3. `dvc dag`

## About MLflow & DVC

### MLflow
- Production-grade
- Experiment tracking
- Model logging and tagging

### DVC
- Lightweight for POC
- Experiment tracking
- Orchestration (Creating Pipelines)
