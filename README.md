# Student Performance Prediction - ML Project

## Description
This project implements a machine learning pipeline to predict student performance based on various demographic and academic factors. It includes a complete lifecycle from data ingestion to model training and deployment via a Flask web application.

The application allows users to input student details and receive a predicted score (likely Math Score, given the other inputs).

## Features
The model trains on and accepts the following input features for prediction:
* **Gender**
* **Race/Ethnicity**
* **Parental Level of Education**
* **Lunch Type**
* **Test Preparation Course**
* **Reading Score**
* **Writing Score**

## Tech Stack
* **Language:** Python
* **Web Framework:** Flask
* **Machine Learning:** Scikit-learn, XGBoost, CatBoost, AdaBoost
* **Data Processing:** Pandas, NumPy

## Installation

1.  **Clone the repository** to your local machine.

2.  **Install the dependencies**:
    This project uses a `r.txt` file for requirements.
    ```bash
    pip install -r r.txt
    ```
    *(Note: Ensure you are in the root directory where `r.txt` is located)*

## Usage

1.  **Start the Flask Application**:
    ```bash
    python app.py
    ```
    This will launch the server on `http://0.0.0.0:5000/`.

2.  **Access the Web Interface**:
    Open your web browser and go to `http://localhost:5000` (or the local IP provided in the terminal).

3.  **Predict**:
    Navigate to the prediction page, fill in the student details, and submit the form to see the predicted performance score.

## Model Training pipeline
The project evaluates several regression models to determine the best fit for the data. The models included in the training pipeline are:
* Random Forest Regressor
* Decision Tree Regressor
* Gradient Boosting Regressor
* Linear Regression
* XGBRegressor
* CatBoosting Regressor
* AdaBoost Regressor

The training script automatically selects the model with the highest R2 score.

## Project Structure
* `app.py`: The Flask application entry point.
* `src/`: Contains the core logic for the ML project.
    * `components/`: Modules for data ingestion, transformation, and model training.
    * `pipeline/`: Pipelines for training and prediction.
* `templates/`: HTML templates for the web interface.
* `artifacts/`: Stores generated files like the trained model (`model.pkl`) and preprocessor.

