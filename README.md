# Car Marketplace Analysis
# Project Goal
The primary objective of this project, **Car Marketplace Analysis**, was to conduct a multidimensional analysis of the secondary car market in Poland and build an interpretable machine learning model to automatically estimate vehicle prices and detect market opportunities.
Unlike standard statistical reports, this project covers the full data science lifecycle. It allows stakeholders to:
*   **Understand Market Structure:** Explore how prices, depreciation, and features vary across brands and regions using advanced interactive visualizations.
*   **Identify Key Price Determinants:** Statistically verify which technical parameters and equipment pieces genuinely drive a vehicle's value.
*   **Detect Market Opportunities:** Use a Machine Learning (Random Forest) model to calculate the "Fair Price" of a car and automatically flag undervalued offers ("Super Deals") or overpriced listings.
*   **Explain AI Decisions:** Utilize Explainable AI (XAI) to understand exactly why the model priced a specific car the way it did, feature by feature.
# 💻 Technologies & Tools
*   **R & R Markdown** – Main statistical programming language and reporting framework used to build reproducible research.
*   **Tidyverse & dplyr** – For robust data wrangling, cleaning, and preprocessing.
*   **ggplot2 & Plotly** – For generating static and interactive data visualizations (Treemaps, Waffle charts).
*   **Leaflet & sf** – For spatial data analysis and interactive regional price mapping across Polish voivodeships.
*   **Ranger** – Fast implementation of the Random Forest algorithm used for predictive price modeling.
*   **DALEX** – Used for Descriptive Machine Learning Explanations (Variable Importance, Partial Dependence Profiles, and Break-Down plots).
*   **naniar & VIM** – For missing data visualization and advanced hot-deck imputation.
# 📊 Key Features & Architecture
**Module 1: Data Preprocessing & Validation**
*   **The Insight:** Automatically handles missing data and applies strict rule-based validation (e.g., verifying realistic mileage and price ranges).
*   **Business Value:** Cleans the raw data from scraped listings, ensuring that the predictive models are trained on reliable, high-quality information without anomalies.
**Module 2: Market Exploratory & Spatial Analysis**
*   **The Insight:** Employs interactive hierarchy maps, spatial cartograms (Leaflet), and depreciation curves to show market dominance, regional price differences, and how fast specific brands lose value.
*   **Business Value:** Provides an intuitive overview for quick decision-making, helping buyers understand which brands retain value (like Porsche) and where cars are statistically cheaper.
**Module 3: The ML Opportunity Scanner (Random Forest)**
*   **The Insight:** A predictive model acting as an automated evaluator. It compares the actual listing price with the model-calculated "Fair Value", grouping them into segments (e.g., "Super Deal", "Market Price", "Overpriced").
*   **Business Value:** Allows users to filter thousands of listings to find genuinely undervalued cars, completely ignoring emotional or biased pricing from sellers.
**Module 4: Explainable AI (DALEX)**
*   **The Insight:** Generates Waterfall (Break-Down) plots for individual vehicle listings.
*   **Business Value:** Delivers a transparent verdict on pricing. It breaks down the price of a chosen car to show exactly how much value is added or subtracted by its mileage, engine power, or specific transmission type.
# 📂 Project Structure
The repository is organized as follows:
*   `Car_Marketplace_Analysis.Rmd` - The core R Markdown file containing all the data processing logic, exploratory analysis, and ML model definitions.
*   `Car_Marketplace_Analysis.html` - The pre-rendered, interactive HTML report containing all visualizations, code outputs, and findings.
*   `Car_sale_ads.csv.zip` - The compressed dataset containing the used car sales offers (March–May 2021).
*   `x.css` - Custom stylesheet used for formatting the HTML output report.
*   `README.md` - Project documentation (This file).
# 🚀 How to Run
The project has already been processed and rendered into a convenient, interactive HTML format.
1.  Clone this repository to your local machine or download the files.
2.  Open the `Car_Marketplace_Analysis.html` file in any modern web browser to view the interactive report, plots, and insights.
*(Optional)* If you wish to re-run the code or modify the models:
1.  Ensure you have **R** and **RStudio** installed.
2.  Install the necessary dependencies by running the following in your R console:
    ```R
    install.packages(c("tidyverse", "ggplot2", "plotly", "leaflet", "ranger", "DALEX", "naniar", "validate", "giscoR"))
    ```
3.  Ensure the `Car_sale_ads.csv.zip` file is located in the same directory as the [.Rmd](cci:7://file:///c:/Users/PC/Downloads/Projekt.Rmd:0:0-0:0) file.
4.  Open `Car_Marketplace_Analysis.Rmd` in RStudio and click the **"Knit"** button to regenerate the report.
# 👤 Authors
**Piotr Pszenny, Polina Glamozdova, Julia Kolerska**
*Data Science Project*
