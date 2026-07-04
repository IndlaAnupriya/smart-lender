Smart Lender - Loan Eligibility Predictor

A Flask-based machine learning web application that predicts whether a loan applicant is eligible using the XGBoost algorithm.

Technologies Used
Python
Flask
XGBoost
Pandas
NumPy
Scikit-learn
HTML/CSS
IBM Cloud (Deployment)
Step 1: Create Virtual Environment
python -m venv venv

This creates a virtual environment named venv.

Why?

Keeps project libraries separate.
Avoids version conflicts.
Step 2: Activate Virtual Environment

Windows

.\venv\Scripts\activate

Mac/Linux

source venv/bin/activate

After activation you'll see

(venv)

before your terminal prompt.

Step 3: Install Dependencies
pip install -r requirements.txt

This installs all required libraries.

Usually includes

Flask
xgboost
numpy
pandas
scikit-learn
matplotlib
seaborn
joblib
pytest
Step 4: Add Dataset

Place

loan_data.csv

inside the project folder.

Example

Smart-Lender/
│
├── loan_data.csv
├── preprocessing.py
├── train_model.py
├── app.py
Step 5: Data Preprocessing

Run

python preprocessing.py

This script usually

Removes missing values
Encodes categorical variables
Splits data
Saves processed dataset
Step 6: Train the Model

Run

python train_model.py

This

Loads processed data
Trains an XGBoost classifier
Evaluates accuracy
Saves the trained model

Usually creates

model.pkl

or

xgboost_model.pkl
Step 7: Perform EDA (Exploratory Data Analysis)

Run

python eda.py

This generates:

Graphs
Correlation matrix
Histograms
Missing-value analysis
Feature importance
Step 8: Start Flask Application

Run

python app.py

Output

Running on http://127.0.0.1:5000

Open your browser and visit:

http://127.0.0.1:5000

You can then:

Enter applicant details
Click Predict
View whether the loan is likely to be approved
Step 9: Run Tests

Execute

pytest tests\test_app.py -v

This runs automated tests for your Flask application.

The -v option provides detailed test output.

Step 10: Deploy to IBM Cloud

Run

ibmcloud cf push

This command:

Uploads your application
Creates a Cloud Foundry app
Makes it accessible online

Before deploying, ensure you have:

Installed the IBM Cloud CLI
Logged in using ibmcloud login
Selected the correct Cloud Foundry organization and space
Included a valid manifest.yml (if required)
Typical Project Structure
Smart-Lender/
│
├── app.py
├── train_model.py
├── preprocessing.py
├── eda.py
├── requirements.txt
├── loan_data.csv
├── model.pkl
├── templates/
│   └── index.html
├── static/
│   ├── style.css
│   └── images/
├── tests/
│   └── test_app.py
└── README.md
Project Workflow
loan_data.csv
        │
        ▼
preprocessing.py
        │
        ▼
Processed Dataset
        │
        ▼
train_model.py
        │
        ▼
XGBoost Model (model.pkl)
        │
        ▼
Flask App (app.py)
        │
        ▼
User Inputs Applicant Details
        │
        ▼
Prediction:
Eligible / Not Eligible
