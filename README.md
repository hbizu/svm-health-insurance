# Health Insurance Cost Prediction with SVM  

This project was developed as part of an **Artificial Intelligence** course and was carried out by three students.  

## 📌 Objective  
The main goal was to develop a **predictive model** to estimate health insurance costs based on personal and demographic attributes.  

---

## 🧠 Methodology  
1. **Preprocessing**  
   - Applied **One-Hot Encoding** to transform categorical variables into numerical form.  
   - Normalized independent variables using **StandardScaler**.  
   - Removed outliers (very high costs and unrealistic BMI values).  

2. **Model Training**  
   - Used **Support Vector Regression (SVR)** with a polynomial kernel to capture non-linear relationships.  
   - Hyperparameters were optimized with **GridSearchCV**, resulting in:  
     ```
     C = 10  
     degree = 3  
     epsilon = 0.1  
     kernel = 'poly'  
     gamma = 1
     ```  

3. **Evaluation**  
   - Model performance was evaluated using the **R² metric** and accuracy.  

---

## 📊 Results  
- Final performance: **R² = 0.8002**  
- Average accuracy: **0.8137**  

### Feature impact analysis:
- **By sensitivity (impact on costs):**  
  1. Smoking status (strongest impact)  
  2. BMI (second most important factor)  
  3. Age group (third most relevant)  

- **By accuracy improvement:**  
  1. Smoking status  
  2. Age group  
  3. Marital status  

These results confirm that lifestyle and demographic factors play a crucial role in health insurance cost prediction.  

---

## 📄 Dataset  
⚠️ **Note:** The original dataset used in this project is **not included in this repository** due to academic restrictions.  

For testing purposes, you can create a CSV file with the following columns:  

- `genero`  
- `estado_civil`  
- `zona_residencia`  
- `fumador`  
- `class_etaria`  
- `imc`  
- `custo`  

Additionally, for prediction, another CSV (`just_features.csv`) must contain the same columns except `custo`.  

