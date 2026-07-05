# AIPredictions

Customer Churn Prediction App

This project is a Flask-based web application that predicts whether a customer is likely to churn. It uses a trained machine learning model and provides a simple form-based interface where users can enter customer details and receive a prediction along with a risk explanation.

## Project Overview

The application includes:

- A web interface built with Flask and HTML templates
- A trained machine learning model stored as model.pkl
- A preprocessing and training pipeline for churn prediction
- A prediction page that displays the result, probability, confidence, and recommendation

## Folder Structure

- app.py: Runs the Flask web application
- train_model.py: Trains and saves the prediction model
- model.pkl: Pretrained model file used by the app
- static/: Contains CSS and JavaScript files for the UI
- templates/: Contains the HTML pages for the home page and results page
- WA_Fn-UseC_-Telco-Customer-Churn.csv: Dataset used for training

## Requirements

Before running the app, make sure you have:

- Python 3.9 or newer
- pip installed
- An active internet connection if dependencies need to be installed

## Step-by-Step Setup

### 1. Open the project folder

```bash
cd /workspaces/AIPredictions/Churn-main
```

### 2. Create a virtual environment

On Linux or macOS:

```bash
python -m venv venv
source venv/bin/activate
```

On Windows PowerShell:

```powershell
python -m venv venv
.\venv\Scripts\Activate.ps1
```

### 3. Install dependencies

You can install everything using the requirements file:

```bash
pip install -r ../requirements.txt
```

If you prefer to install manually, use:

```bash
pip install flask pandas joblib scikit-learn xgboost
```

### 4. Run the application

Start the Flask server:

```bash
python app.py
```

Once the server starts, open your browser and visit:

```text
http://127.0.0.1:5000
```

The application should open automatically in your browser if your system allows it.

## How to Use the App

1. Open the home page in your browser.
2. Fill in the customer information form.
3. Click the prediction button.
4. View the result, which includes:
   - Whether the customer is likely to churn or stay
   - Churn probability
   - Confidence level
   - A recommended action for the business

## Retrain the Model (Optional)

If you want to rebuild the model from the dataset:

1. Make sure the CSV dataset is present in the project folder.
2. Run the training script:

```bash
python train_model.py
```

3. The script will train several models, compare them, and save the best model as model.pkl.
4. Start the app again with:

```bash
python app.py
```

## Troubleshooting

- If you see a module import error, install the missing package using pip.
- If port 5000 is already being used, stop the other application or change the port in app.py.
- If the app cannot find the model file, make sure model.pkl exists in the same directory as app.py.
- If the app does not start, verify that the virtual environment is activated and all dependencies are installed.

## Notes

This app is intended for demonstration and learning purposes. For production use, you should add validation, authentication, logging, and deployment configuration.
