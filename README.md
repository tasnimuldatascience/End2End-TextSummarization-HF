# Text Summarizer Using Hugging Face

## Overview
This project is an **End-to-End NLP Pipeline** for text summarization using **Hugging Face Transformers**. The implementation follows **MLOps best practices**, including configuration management, modularized components, and API integration for deployment.

## **Project Workflow**
The project is structured into multiple stages to ensure smooth training, evaluation, and deployment of the summarization model.

### **1. Configuration Management**
- **`config.yaml`**: Stores paths, dataset configurations, and model settings.
- **`params.yaml`**: Contains hyperparameters for training and evaluation.

### **2. Config Entity & Configuration Manager**
- **Config Entity**: Defines structured configuration classes for various stages.
- **Configuration Manager**: Loads YAML files and provides configuration objects to other components.

### **3. Pipeline Components**
The project is divided into distinct modular components:
- **Data Ingestion**: Downloads and prepares the dataset.
- **Data Transformation**: Tokenizes and preprocesses the dataset for model training.
- **Model Trainer**: Fine-tunes a transformer-based summarization model (e.g., Pegasus, BART).

### **4. Pipeline Integration**
- **Training Pipeline**: Integrates all components and runs end-to-end model training.
- **Prediction Pipeline**: Loads the trained model and generates text summaries on new inputs.

### **5. Deployment & API Integration**
- **Frontend APIs**: Provides an interface for users to interact with the summarization model.
- **Training APIs**: Allows retraining/updating of the model via API endpoints.
- **Batch Prediction APIs**: Enables bulk text summarization requests.

## **Technologies Used**
- **Hugging Face Transformers** for NLP model implementation
- **PyTorch** for deep learning
- **DVC (Data Version Control)** for dataset tracking
- **FastAPI/Flask** for API development
- **Docker & CI/CD** for deployment automation

## **How to Run the Project**
### **Setup the Environment**
```bash
pip install -r requirements.txt
