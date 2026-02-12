Used Car Market Analysis & Price Prediction Engine
(Wstaw tu jakiś reprezentatywny wykres, np. macierz korelacji lub wykres deprecjacji)

🎯 Project Goal
The primary objective of this project was to perform a multi-dimensional analysis of the secondary automotive market in Poland. Using real-world data (scraped between March–May 2021), the study aims to decode the mechanisms governing vehicle valuation.

Beyond standard exploratory analysis, this project implements a Machine Learning model (Random Forest) to:

Quantify Determinants: Identify which technical parameters and equipment features drive market value.

Predict Prices: Build an interpretable model for automatic vehicle valuation.

Detect Anomalies: Identify undervalued assets ("market opportunities") by analyzing prediction residuals.

💻 Tech Stack & Methodology
Language:

Libraries: tidyverse (dplyr, ggplot2), randomForest, caret, lmtest.

Statistical Methods: Student's t-test, Shapiro-Wilk, Factor Analysis.

Machine Learning:  / Random Forest Ensemble.

📊 Key Research Findings
1. Depreciation Dynamics (Premium vs. Budget)
Hypothesis: Does value loss occur uniformly across the market?

Finding: No. The analysis revealed significant heterogeneity. Premium brands, despite higher initial costs, experience steeper absolute depreciation in early years. However, they exhibit better "value retention" in later years compared to budget cars, indicating a non-linear relationship between age and brand prestige.

2. Impact of Equipment on Valuation
Method: Validated using ANOVA and t-tests.

Finding: Luxury features (e.g., leather upholstery, advanced ADAS systems) provide a statistically significant price premium. Interestingly, this premium varies by segment—it is much higher for SUVs and Premium cars than for City cars, confirming that the market values configuration contextually.

3. Price Determinants
Key Drivers: Engine Power (positive correlation) and Age/Mileage (negative correlation).

Non-Linearity: The negative impact of mileage on price diminishes as the vehicle ages. This was confirmed by interaction analysis in the Random Forest model.

🤖 Machine Learning Model (Random Forest)
To address the market's complexity and information asymmetry, I moved beyond linear regression to a Random Forest model.

Model Performance & Anomaly Detection
Why Random Forest? Linear models failed to capture the complex, non-linear interactions between brand prestige, age, and equipment.

Market Opportunity Detection: By analyzing the residuals (difference between Actual Price and Predicted Price), I identified market anomalies.

Offers where Predicted Price >> Actual Price were flagged as potential "bargains" or undervalued assets.

The model achieved highest accuracy in the mid-range price segment, with increased variance in the ultra-luxury segment (outliers).

📂 Project Structure

The repository contains the full analysis workflow:
├── data/                       # Dataset (cleaned and raw)
├── images/                     # Visualizations exported from R
├── script/                     # R Scripts for Cleaning, EDA, and Modeling
├── Used_Car_Analysis.pdf       # Full Report (R Markdown Output)
└── README.md                   # Documentation

Gemini said
To jest znakomity materiał. Ten spis treści i wnioski pokazują, że to nie był prosty projekt "narysuj wykres", ale pełnoprawne badanie Data Science.

Masz tu wszystko, co kochają banki:

Data Cleaning (walidacja, braki danych).

Statystyka (ANOVA, testy t-Studenta, korelacje).

Machine Learning (Las Losowy - Random Forest).

Wnioski biznesowe (krzywe deprecjacji, segmentacja Premium vs Standard).

Oto kompletny kod README.md przygotowany specjalnie pod ten wsad. Przetłumaczyłem to na profesjonalny angielski, używając terminologii z zakresu Valuation & Risk Modeling.

Skopiuj to do pliku README.md w repozytorium Econometric_Analysis_R.

Used Car Market Analysis & Price Prediction Engine
(Wstaw tu jakiś reprezentatywny wykres, np. macierz korelacji lub wykres deprecjacji)

🎯 Project Goal
The primary objective of this project was to perform a multi-dimensional analysis of the secondary automotive market in Poland. Using real-world data (scraped between March–May 2021), the study aims to decode the mechanisms governing vehicle valuation.

Beyond standard exploratory analysis, this project implements a Machine Learning model (Random Forest) to:

Quantify Determinants: Identify which technical parameters and equipment features drive market value.

Predict Prices: Build an interpretable model for automatic vehicle valuation.

Detect Anomalies: Identify undervalued assets ("market opportunities") by analyzing prediction residuals.

💻 Tech Stack & Methodology
Language:

Libraries: tidyverse (dplyr, ggplot2), randomForest, caret, lmtest.

Statistical Methods: ANOVA, Student's t-test, Shapiro-Wilk, Breusch-Pagan, Factor Analysis.

Machine Learning: Regression Trees / Random Forest Ensemble.

📊 Key Research Findings
1. Depreciation Dynamics (Premium vs. Budget)
Hypothesis: Does value loss occur uniformly across the market?

Finding: No. The analysis revealed significant heterogeneity. Premium brands, despite higher initial costs, experience steeper absolute depreciation in early years. However, they exhibit better "value retention" in later years compared to budget cars, indicating a non-linear relationship between age and brand prestige.

2. Impact of Equipment on Valuation
Method: Validated using ANOVA and t-tests.

Finding: Luxury features (e.g., leather upholstery, advanced ADAS systems) provide a statistically significant price premium. Interestingly, this premium varies by segment—it is much higher for SUVs and Premium cars than for City cars, confirming that the market values configuration contextually.

3. Price Determinants
Key Drivers: Engine Power (positive correlation) and Age/Mileage (negative correlation).

Non-Linearity: The negative impact of mileage on price diminishes as the vehicle ages. This was confirmed by interaction analysis in the Random Forest model.

🤖 Machine Learning Model (Random Forest)
To address the market's complexity and information asymmetry, I moved beyond linear regression to a Random Forest model.

Model Performance & Anomaly Detection
Why Random Forest? Linear models failed to capture the complex, non-linear interactions between brand prestige, age, and equipment.

Market Opportunity Detection: By analyzing the residuals (difference between Actual Price and Predicted Price), I identified market anomalies.

Offers where Predicted Price >> Actual Price were flagged as potential "bargains" or undervalued assets.

The model achieved highest accuracy in the mid-range price segment, with increased variance in the ultra-luxury segment (outliers).

📂 Project Structure
The repository contains the full analysis workflow:

Plaintext
├── data/                       # Dataset (cleaned and raw)
├── images/                     # Visualizations exported from R
├── script/                     # R Scripts for Cleaning, EDA, and Modeling
├── Used_Car_Analysis.pdf       # Full Report (R Markdown Output)
└── README.md                   # Documentation
🚀 How to Run
Clone the repository.

Open the .Rmd (R Markdown) file in RStudio.

Ensure all packages listed in setup chunk are installed.

Run the chunks sequentially to reproduce the Data Cleaning -> EDA -> Modeling pipeline.

👤 Author
Piotr Pszenny
Aspiring Risk & Data Analyst | Gdańsk Tech
