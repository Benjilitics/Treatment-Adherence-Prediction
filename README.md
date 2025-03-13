# Treatment Adherence Prediction Project

### Project Overview
This project uses machine learning to predict patient treatment adherence based on various demographic, behavioral, clinical, and psychological factors. The analysis includes exploratory data analysis (EDA), feature engineering, model training, and evaluation to identify the most effective predictive model.

### Table of Contents
- [Prerequisites](#prerequisites)
- [Project Setup](#project-setup)
- [Project Structure](#project-structure)
- [Data Description](#data-description)
- [Analysis Workflow](#analysis-workflow)
- [Git Repository Management](#git-repository-management)
- [Troubleshooting](#troubleshooting)

### Prerequisites
* Python 3.8 or later
* Visual Studio Code
* Git

### Project Setup

#### 1. Install Required Software
* Python: Download and install from python.org. Check "Add Python to PATH" during installation.
* Visual Studio Code: Download and install from code.visualstudio.com.
* Git: Download and install from git-scm.com.

#### 2. Set Up the Project Environment
Create a project folder:
```bash
mkdir treatment_adherence_project
cd treatment_adherence_project
```

Create a virtual environment:
```bash
python -m venv venv
```

Activate the virtual environment:
```bash
# Windows
.\venv\Scripts\activate
# Mac/Linux
source venv/bin/activate
```

Install required libraries:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

### Project Structure
```
treatment_adherence_project/
├── venv/                    # Virtual environment (not tracked by Git)
├── data/                    # Data files
│   └── synthetic_treatment_adherence_data.csv
├── adherence_analysis.py    # Main analysis script
├── requirements.txt         # List of required libraries
├── .gitignore              # Git ignore file
└── README.md               # Project documentation
```

### Data Description
The dataset includes the following features:
* Demographic factors: Age, Gender, Income_Level
* Behavioral factors: Missed_Appointments, Refill_Gaps
* Clinical factors: Side_Effects_Severity, Comorbidities, Polypharmacy
* Psychological factors: Health_Literacy, Mental_Health_Status
* System-related factors: Medication_Cost, Provider_Communication, Social_Support
* Target variable: Adherence (1=Adherent, 0=Non-Adherent)

### Analysis Workflow
The `adherence_analysis.py` script performs the following steps:

#### Exploratory Data Analysis (EDA)
* Load the dataset and examine basic statistics
* Visualize the distribution of the target variable
* Analyze relationships between features

#### Feature Engineering
* Convert categorical variables to dummy variables
* Scale numeric features
* Create interaction terms (if applicable)

#### Model Training and Evaluation
* Split data into training and testing sets
* Train multiple models:
  * Logistic Regression
  * Random Forest
  * Gradient Boosting
* Evaluate models using:
  * Cross-validation
  * Accuracy
  * Classification report (precision, recall, F1-score)
  * ROC-AUC score
  * ROC curves

### Git Repository Management

#### Setting Up Git Repository
```bash
# Initialize Git repository
git init

# Create .gitignore file
echo "venv/
__pycache__/
*.pyc
*.pyo
.DS_Store" > .gitignore

# Stage and commit files
git add .
git commit -m "Initial commit: Add treatment adherence analysis script"

# Link to GitHub repository
git remote add origin https://github.com/your-username/treatment-adherence-project.git
git branch -M main
git push -u origin main
```

### Troubleshooting

#### Virtual Environment Issues
* If the virtual environment is not recognized in VS Code, ensure you've selected the correct Python interpreter
* If libraries are not found, verify that the virtual environment is activated and libraries are installed

#### Running the Analysis
* Ensure the virtual environment is activated
* Run the script: `python adherence_analysis.py`
* Review the output, including plots and model performance metrics

This project was created to demonstrate machine learning techniques for predicting patient treatment adherence.