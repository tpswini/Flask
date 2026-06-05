# Flask Machine Learning Prediction App

A Flask web application that demonstrates the deployment of Machine Learning models for real-time predictions. The project includes:

- Loan Approval Prediction
- Iris Flower Classification

# Features

### Loan Approval Prediction
Predicts whether a loan application is likely to be approved based on applicant information such as:

- Gender
- Marital Status
- Dependents
- Education
- Employment Status
- Credit History
- Property Area
- Applicant Income
- Co-applicant Income
- Loan Amount
- Loan Term

### Iris Flower Classification
Classifies an iris flower into one of three species:

- Setosa
- Versicolor
- Virginica

based on flower measurements.

---

## Project Structure


Flask-main/
│
├── app.py                    # Main Flask application
├── iris_model.py             # Iris classification model training
├── model.pkl                 # Pre-trained loan prediction model
├── train.csv                 # Loan training dataset
├── test.csv                  # Loan test dataset
├── Loan Prediction.ipynb     # Model development notebook
├── Procfile                  # Deployment configuration
│
├── templates/
│   ├── index.html
│   ├── prediction.html
│   └── irisprediction.html
│
├── static/
│   ├── machine.jpg
│   ├── machine.jpeg
│   ├── machine1.jpg
│   └── *.ico
│
└── README.md

## Technologies Used

- Python
- Flask
- NumPy
- Pandas
- Scikit-Learn
- HTML/CSS
- Pycharm IDE

## Installation

### 1. Clone the repository
 bash
git clone <repository-url>
cd Flask-main


### 2. Create a virtual environment

python -m venv venv

Activate it:

Windows:
venv\Scripts\activate

Linux/Mac:
source venv/bin/activate


### 3. Install dependencies


pip install flask numpy pandas scikit-learn


Or create a "requirements.txt" file and run:


pip install -r requirements.txt



## Running the Application

Start the Flask server:

python app.py


The application will run at:


http://127.0.0.1:5000


---

## Loan Prediction Workflow

The application:

1. Collects applicant information through a web form.
2. Performs feature encoding.
3. Applies logarithmic transformations to numerical values.
4. Loads the trained model ("model.pkl").
5. Predicts loan approval status.
6. Displays the result to the user.

---

## Iris Classification Workflow

The application:

1. Accepts flower measurements.
2. Trains a Decision Tree classifier using the Iris dataset.
3. Predicts the flower species.
4. Displays the classification result.

---

## Machine Learning Models

### Loan Prediction Model

The loan prediction model is stored as:

text
model.pkl


and is loaded during application startup.

### Iris Classification Model

The Iris classifier uses:

python
DecisionTreeClassifier()


from Scikit-Learn.



## Future Improvements

- Store trained Iris model instead of retraining on every request
- Add model evaluation metrics
- Improve UI design
- Add form validation
- Create REST API endpoints
- Add Docker support
- Deploy on Render, Railway, or Heroku


## Author

Developed using Flask and Scikit-Learn for Machine Learning model deployment demonstrations.

## License

This project is intended for educational and learning purposes.
