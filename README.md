# Predictive Maintenance of Turbofan Engines

This repository contains the project work for the Data Science and Machine Learning internship at **Uniconverge Technologies Pvt Ltd (UCT)**, facilitated by Upskill Campus done during the period July - August 2025.

## 📝 Introduction

The goal of this project is to predict the Remaining Useful Life (RUL) of turbofan engines using a simulated time-series dataset provided by NASA. The project involves a complete machine learning workflow, including data exploration, feature engineering, preprocessing, and the development and comparison of two predictive models: a Random Forest Regressor and a Long Short-Term Memory (LSTM) network.

---

## 📊 Dataset

The project uses the **NASA C-MAPSS (Commercial Modular Aero-Propulsion System Simulation)** dataset. This dataset is divided into four subsets, each with increasing complexity:

| Dataset | Training Engines | Test Engines | Operating Conditions | Fault Modes |
| :--- | :--- | :--- | :--- | :--- |
| **FD001** | 100 | 100 | 1 | 1 |
| **FD002** | 260 | 259 | 6 | 1 |
| **FD003** | 100 | 100 | 1 | 2 |
| **FD004** | 248 | 249 | 6 | 2 |

Each engine's data includes time-series measurements from 21 sensors and 3 operational settings.

---

## 📂 Project Structure

The repository is organized as follows:
```
└── UNICONVERGE/
├── 📂 data/
│   ├── 📂 FD001/
│   ├── 📂 FD002/
│   ├── 📂 FD003/
│   └── 📂 FD004/
├── 📂 notebooks/
│   ├── 📄 Turbofan_Analysis_FD001_(Base_Case).ipynb
│   ├── 📄 Turbofan_Analysis_FD002_(Multi-Condition).ipynb
│   ├── 📄 Turbofan_Analysis_FD003_(Multi-Fault).ipynb
│   └── 📄 Turbofan_Analysis_FD004_(Complex_Case).ipynb
├── 📂 reports/
│   ├── 📄 Agamya_Week-01.docx
│   └── ... (Weekly and Final Reports)
├── 📂 venv/
├── 📄 .gitignore
├── 📄 README.md
└── 📄 requirements.txt
```
* **data/**: Contains the four NASA C-MAPSS datasets, each in its own subfolder.
* **notebooks/**: Contains the Jupyter Notebooks for the analysis of each dataset. Each notebook includes the full workflow from EDA to model evaluation.
* **reports/**: Contains all weekly and final project reports.

---

## Methodology

The project follows a structured approach for each dataset:
1.  **Exploratory Data Analysis (EDA):** Visualizing sensor trends and calculating standard deviations to identify useless features.
2.  **Feature Engineering:** Calculating the Remaining Useful Life (RUL) for the training data.
3.  **Preprocessing:** Normalizing features using a Min-Max Scaler and reshaping the data into sequences for the LSTM model.
4.  **Modeling:**
    * Training a **Random Forest Regressor** as a baseline model.
    * Implementing and tuning a **Long Short-Term Memory (LSTM)** network to handle the time-series nature of the data.
5.  **Evaluation:** Comparing the models based on their Root Mean Squared Error (RMSE) on the test set.

---

## 📈 Results Summary

The performance of the two models was compared across all four datasets. The LSTM model showed a significant advantage on the more complex `FD003` dataset, which features multiple fault modes.

| Dataset | Random Forest (RMSE) | LSTM (RMSE) |
| :--- | :--- | :--- |
| **FD001** | 34.60 | 80.64 |
| **FD002** | 34.58 | 37.55 |
| **FD003** | 50.42 | **14.39** |
| **FD004** | 42.92 | 40.65 |

---

## How to Run?

1.  Clone this repository to your local machine.
2.  Set up a Python virtual environment and install the required libraries using the `requirements.txt` file:
    ```bash
    pip install -r requirements.txt
    ```
3.  Open the Jupyter Notebooks in the `notebooks/` directory and run the cells in order.

---

## Author

* **Agamya David**