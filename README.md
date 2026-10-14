# 🎓 Student Marks Prediction System

An end-to-end machine learning project that predicts a student's **math score** from demographic details and their reading and writing scores. It includes a modular training pipeline and a Flask web app for live predictions.

## Features
- Data ingestion, transformation and model training as separate components
- Trains and compares multiple regression models with hyperparameter tuning
- Automatically picks the best model by R² score
- Flask web app with a form for instant predictions
- Custom logging and exception handling

## Dataset
Students Performance dataset (`notebook/data/stud.csv`) with these columns:

| Feature | Description |
|---|---|
| gender | Student gender |
| race_ethnicity | Group A–E |
| parental_level_of_education | Parent's education level |
| lunch | Standard / free-reduced |
| test_preparation_course | Completed / none |
| reading_score | Reading score |
| writing_score | Writing score |
| **math_score** | **Target to predict** |

## Models Compared
Linear Regression, Decision Tree, Random Forest, Gradient Boosting, AdaBoost, KNN, XGBoost, CatBoost.

## Project Structure
```
├── app.py                  # Flask application
├── setup.py
├── requirements.txt
├── notebook/               # EDA and model training notebooks + dataset
├── src/
│   ├── components/         # data_ingestion, data_transformation, model_trainer
│   ├── pipeline/           # predict_pipeline
│   ├── utils.py
│   ├── logger.py
│   └── exception.py
├── templates/              # HTML pages
└── artifacts/              # Saved model, preprocessor and data splits
```

## Getting Started

**1. Clone the repository**
```bash
git clone https://github.com/Kaif-077/Student-Marks-Prediction.git
cd <Student-Marks-Prediction>
```

**2. Create a virtual environment and install dependencies**
```bash
python -m venv venv
venv\Scripts\activate        # Windows
source venv/bin/activate     # Mac/Linux
pip install -r requirements.txt
```

**3. Train the model** (optional, trained artifacts are already included)
```bash
python -m src.components.data_ingestion
```

**4. Run the web app**
```bash
python app.py
```
Open `http://127.0.0.1:5000` and go to `/predictdata` to make predictions.

## Tech Stack
Python, Pandas, NumPy, Scikit-learn, XGBoost, CatBoost, Flask, Matplotlib, Seaborn

## Future Improvements
- Add model evaluation metrics to the app
- Dockerize and deploy to the cloud
- Add input validation

## Author
**MOHAMED KAIF** – [GitHub](https://github.com/Kaif-077)