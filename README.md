# Employee Attrition Prediction App

This project is a Streamlit web app that predicts whether an employee is likely to leave the company based on HR-related features such as age, department, job role, salary, overtime, and job satisfaction.

## Project files
- App script: app.py
- Trained model: decision_tree_pipeline.pkl
- Dataset: WA_Fn-UseC_-HR-Employee-Attrition.csv
- Training script: jana_alaa_day_11.py
- Demo video: [projectREC.mp4](projectREC.mp4)

## Dataset used
The app uses the IBM HR Analytics Employee Attrition & Performance dataset, stored in the file:
- WA_Fn-UseC_-HR-Employee-Attrition.csv

### Dataset summary
- Rows: 1470
- Columns: 35
- Target column: Attrition
- Class distribution:
  - No: 1233
  - Yes: 237

### Notes about the data
The dataset contains employee information such as:
- Age
- BusinessTravel
- Department
- DistanceFromHome
- Education
- JobRole
- MonthlyIncome
- OverTime
- YearsAtCompany
- and other HR-related features

Before training, the preprocessing step removed some columns that were not useful for prediction, including:
- EmployeeCount
- Over18
- StandardHours

## How the app works
1. The user enters employee details in the Streamlit interface.
2. The app formats the input into a DataFrame.
3. The trained model predicts whether the employee is likely to leave.
4. The result is shown as either a likely attrition risk or a low-risk prediction.

## Demo video
You can watch the recorded demo here:
- [projectREC.mp4](projectREC.mp4)

## Requirements
The project dependencies are listed in requirements.txt.

### Install the requirements on Windows
Open PowerShell in the project folder and run:

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
```

### Main packages included
- pandas
- numpy
- scikit-learn
- joblib
- streamlit

## Run the app
From the project folder, run:

```powershell
streamlit run app.py
```

If the model file is missing, you can retrain it by running the training script:

```powershell
python jana_alaa_day_11.py
```
