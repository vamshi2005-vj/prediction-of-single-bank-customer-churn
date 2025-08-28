![Python](https://img.shields.io/badge/python-3.10-blue)
![License](https://img.shields.io/badge/license-MIT-green)

# Multi-Customer Bank Churn Prediction

## PROJECT OVERVIEW:
This Flask web application predicts whether multiple bank customers are at risk of leaving the bank (churn) based on their personal and financial information.  
Supports **single-customer** predictions via a form and **multi-customer predictions** via CSV upload.  
**Features**
- User authentication with **admin** and **employee** login.
- Password hashing for security.
- OTP-based password reset sent to registered emails.
- Bulk predictions via CSV upload.
- Saves at-risk customers automatically in an Excel file (`at_risk_customers.xlsx`).
- Built with Flask, scikit-learn, pandas, joblib, and SQLite.

## Project Structure
- `app.py`                     → Main Flask application
- `churn_predict_model.pkl`     → Pre-trained churn prediction model
- `Churn_Modelling.csv`         → Sample dataset for preprocessing
- `churn_app.db`                → SQLite database
- `requirements.txt`            → Python dependencies
- `at_risk_customers.xlsx`      → Excel file for at-risk customers
- `uploads/`                    → Uploaded CSV files (bulk predictions)
- `templates/`                  → HTML templates
  - `login.html`               → Login & OTP template
  - `index.html`               → Prediction form template
- `static/`                     → CSS, JS, images (if any)
  - `css/`
  - `js/`
  - `images/`
- `logs/`                       → Optional logs folder
  - `app.log`
- `README.md`                   → Project documentation
- `.gitignore`                  → Files/folders to ignore in Git
- `LICENSE`                     → MIT License

**Note:** Large data and model files (`Churn_Modelling.csv`, `churn_predict_model.pkl`) are **not included** in the repo. Place them locally to run the app.

## Setup Instructions

**1. Clone the repository**
```bash
git clone https://github.com/vamshi2005-vj/multi-customer-churn.git
cd multi-customer-churn

2. Create and activate a virtual environment
python -m venv .venv
# Windows
.\\.venv\\Scripts\\activate
# macOS/Linux
source .venv/bin/activate

3. Install dependencies
pip install -r requirements.txt

4. Place necessary files in the project folder
churn_predict_model.pkl
Churn_Modelling.csv

5. Run the Flask app
bash
Copy code
python app.py

6. Open the app in a browser
http://127.0.0.1:5000/

Usage:
Login as Admin or Employee.

If the password is incorrect, an OTP will be sent automatically to the registered email.
For single-customer prediction, fill in the form.
For multi-customer prediction, upload a CSV file with the required columns:
CustomerId, CreditScore, Geography, Gender, Age, Tenure,
Balance, NumOfProducts, HasCrCard, IsActiveMember, EstimatedSalary
Geography: 1 = Germany, 2 = Spain, 3 = France
Gender: 0 = Female, 1 = Male
Download at-risk customers as at_risk_customers.xlsx.

Dependencies:
Flask
Flask-Mail
pandas
scikit-learn
joblib
openpyxl
werkzeug
sqlite3 (built-in)

All dependencies are listed in requirements.txt.

License
MIT License

Author
Vamshi Jakkali
