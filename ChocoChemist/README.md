# 🍫 ChocoChemist: Predicting Chocolate Bar Ratings

ChocoChemist is a machine learning project that predicts expert chocolate ratings (from 1 to 4) using both structured product data and unstructured flavor descriptions.

The model is trained on the **Flavors of Cacao** dataset and uses:
- **Feature engineering** from cocoa %, ingredients, company, and origin
- **TF-IDF vectorization** of flavor notes
- **LightGBM** for regression modeling

---

## 📊 Final Model Performance
- The final LightGBM model, trained on a combination of engineered numeric features and TF-IDF text vectors from flavor notes, achieved a **Root Mean Squared Error (RMSE)** of **0.3507**.  
- Given that the ratings range from **1 to 4**, this low RMSE indicates that the model is capable of closely approximating expert ratings, effectively learning patterns from both structured metadata and unstructured sensory descriptions.

---

## 📌 Key Highlights
- Grouped rare companies to reduce noise
- Extracted flavor terms using TF-IDF
- Combined numeric and text features using LightGBM
- Visualized feature importance and key flavor descriptors

---

## 📦 Dataset
- Source: [Chocolate Ratings Dataset]([http://flavorsofcacao.com/chocolate_database.html](https://www.kaggle.com/datasets/joebeachcapital/chocolate-ratings))

