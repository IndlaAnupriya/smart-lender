Smart Lender - Loan Eligibility Predictor
Flask web app with XGBoost model predicting loan eligibility.

Setup
python -m venv venv
.\venv\Scripts\activate
pip install -r requirements.txt
Place loan_data.csv in project root
python preprocessing.py
python train_model.py
python eda.py
python app.py
Run
python app.py → http://127.0.0.1:5000

Test
pytest tests\test_app.py -v

Deploy
ibmcloud cf push
