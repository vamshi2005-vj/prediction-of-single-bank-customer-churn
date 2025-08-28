![Python](https://img.shields.io/badge/python-3.10-blue)
![License](https://img.shields.io/badge/license-MIT-green)

*Bank Customer Churn Prediction (Single Customer)*
**PROJECT OVERVIEW:**
This Flask web application predicts whether a single bank customer is at risk of leaving the bank (churn) based on their personal and financial information.  
Features:
Predict churn for one customer at a time.
Automatically saves at-risk customers in an Excel file (`risk\_customers.xlsx`).
Built withFlask,scikit-learn,panda and joblib.

**Project Structure**
├─ app.py # Main Flask app
├─ requirements.txt # Python dependencies
├─ templates/ # HTML templates (index.html)
├─ static/ # CSS, JS, images (if any)
├─ .gitignore # Files/folders to ignore
├─ README.md # Project documentation

Note:Large data and model files (`Churn\_Modelling.csv`, `churn\_predict\_model.pkl`) are not included in the repo. Place them locally to run the app.

**Setup Instructions**

1.Clone the repository
```bash
git clone https://github.com/vamshi2005-vj/prediction-of-single-bank-customer-churn.git
cd prediction-of-single-bank-customer-churn

2.Create and activate a virtual environment
python -m venv .venv

Windows
.\\.venv\\Scripts\\Activate
macOS/Linux
source .venv/bin/activate

3.Install dependencies
pip install -r requirements.txt

4.Place necessary files in the project folder.
churn\_predict\_model.pkl
Churn\_Modelling.csv

5.Run the Flask app
python app.py

6.Open the app in a browser
http://127.0.0.1:5000/

**Usage:**
Fill in the customer details in the form.
Click Predict to see if the customer is at risk.
If the customer is at risk, their details are saved in risk\_customers.xlsx.

**Dependencies:**
Flask
pandas
scikit-learn
joblib
openpyxl

All dependencies are listed in requirements.txt.
Author
Vamshi Jakkali





