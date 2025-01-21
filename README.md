# Heart Disease Prediction Using Bayesian Networks

This project implements a Bayesian Network model to predict the likelihood of heart disease based on various health and lifestyle factors. The model is created and trained using the `pgmpy` library and utilizes the `VariableElimination` inference algorithm for predictions.

---

## Prerequisites

To run this project, ensure you have the following installed:

- Python (>= 3.7)
- pandas
- pgmpy

Install the required Python libraries using:

```bash
pip install pandas pgmpy
```

---

## Dataset

The dataset used is `heart (1).csv`, which should be placed in the same directory as the script. The dataset contains the following columns:

- `age` (Categorical): Age group (e.g., SuperSenior-Citizen, SeniorCitizen, MiddleAged, Youth, Teen)
- `Gender` (Categorical): Male or Female
- `Family` (Binary): Family history of heart disease (Yes/No)
- `diet` (Categorical): Quality of diet (High, Medium)
- `Lifestyle` (Categorical): Activity level (Athlete, Active, Moderate, Sedentary)
- `cholestrol` (Categorical): Cholesterol levels (High, BorderLine, Normal)
- `heartdisease` (Binary): Presence of heart disease (Yes/No)

---

## Script Overview

The script performs the following steps:

1. **Data Loading**: Reads the CSV file into a pandas DataFrame.
2. **Model Definition**: Defines the Bayesian Network structure.
3. **Model Training**: Fits the model using Maximum Likelihood Estimation.
4. **Inference**: Allows the user to input values for various factors and predicts the likelihood of heart disease.

---

## Running the Script

1. Clone the repository and navigate to the script directory:

```bash
git clone https://github.com/your-repo/heart-disease-prediction.git
cd heart-disease-prediction
```

2. Place the `heart (1).csv` dataset in the same directory.

3. Run the script:

```bash
python heart_disease_prediction.py
```

4. Follow the prompts to enter values for the following variables:

   - **Age**:
     - SuperSenior-Citizen: `0`
     - SeniorCitizen: `1`
     - MiddleAged: `2`
     - Youth: `3`
     - Teen: `4`

   - **Gender**:
     - Male: `0`
     - Female: `1`

   - **Family History**:
     - Yes: `1`
     - No: `0`

   - **Diet**:
     - High: `0`
     - Medium: `1`

   - **Lifestyle**:
     - Athlete: `0`
     - Active: `1`
     - Moderate: `2`
     - Sedentary: `3`

   - **Cholesterol**:
     - High: `0`
     - BorderLine: `1`
     - Normal: `2`

5. View the prediction results for heart disease.

---

## Example Output

```text
For Age enter SuperSenior - Citizen:0, SeniorCitizen:1, MiddleAged:2, Youth:3, Teen:4
For Gender enter - Male:0, Female:1
For Family History enter - Yes:1, No:0
For Diet enter - High:0, Medium:1
For LifeStyle enter - Athlete:0, Active:1, Moderate:2, Sedentary:3
For Cholesterol enter - High:0, BorderLine:1, Normal:2

Enter Age: 2
Enter Gender: 0
Enter Family History: 1
Enter Diet: 0
Enter Lifestyle: 3
Enter Cholesterol: 0
+----------------+-------------------+
| heartdisease  |   phi(heartdisease) |
+----------------+-------------------+
| heartdisease_0 |           0.3567 |
| heartdisease_1 |           0.6433 |
+----------------+-------------------+
```

---

## Notes

- Ensure that the dataset is correctly formatted and matches the column names used in the script.
- The model structure assumes certain dependencies between variables. These can be modified based on domain knowledge.

---

