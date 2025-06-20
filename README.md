# Student Stress Level Analysis & Prediction

A comprehensive data analysis and machine learning project to identify key factors correlated with student stress and to build a model to predict stress levels.

## Project Overview

This project explores a dataset of student attributes to uncover insights into academic stress. The analysis follows a complete data science workflow:

1.  **Exploratory Data Analysis (EDA):** To understand the data and discover initial patterns and relationships.
2.  **Data Preprocessing:** To prepare the data for machine learning models.
3.  **Predictive Modeling:** To train a Random Forest Classifier to predict student stress categories.
4.  **Model Evaluation:** To critically assess the performance and limitations of the trained model.

## 📈 Key Findings & Insights

This analysis answered our primary research question and revealed several other significant insights:

* ### 1. No Significant Impact of AI Tools on Typical Stress
    The primary research question was to determine if using AI for studying affects stress. Our analysis, particularly through boxplot comparisons, showed that the **median stress level for students who use AI and those who do not is identical (a value of 6)**. This leads to the conclusion that AI usage is not a significant factor in determining a student's *typical* stress level in this dataset.

* ### 2. The Paradox of Exam Preparation
    The most counter-intuitive and significant finding was the relationship between exam preparation and stress. Students who reported being **'Revised Fully' exhibited the highest median stress level (a value of 7)**, higher than those who were 'On Track' or even 'Falling Behind'. This suggests that factors like **performance anxiety and perfectionism** may be stronger drivers of stress than a lack of preparation itself.

* ### 3. Weak Correlation with Lifestyle Habits
    Numerical analysis via scatter plots and a correlation heatmap confirmed that there is **no significant linear relationship** between stress levels and lifestyle habits such as `average_sleep_hours` (correlation: 0.04) and `daily_screen_time` (correlation: 0.01).

* ### 4. Model Performance and Bias
    A Random Forest Classifier was trained to predict stress categories ('Low', 'Medium', 'High'). While the model achieved a certain overall accuracy, the confusion matrix revealed a **strong performance imbalance**. The model is effective at identifying the 'Medium' stress class (the majority class) but performs very poorly on the minority classes, frequently misclassifying 'Low' and 'High' stress students as 'Medium'. This indicates a strong model bias that would need to be addressed in future iterations.

## 🛠️ Technical Setup

To run this analysis on your local machine, please follow these steps:

1.  **Clone the Repository**
    ```bash
    git clone [https://github.com/tu-usuario/tu-repositorio.git](https://github.com/tu-usuario/tu-repositorio.git)
    cd tu-repositorio
    ```
    2.  **Create a Virtual Environment**
    It is highly recommended to use a virtual environment to manage dependencies.
    ```bash
    python -m venv .venv
    # Activate the environment (Windows)
    .venv\Scripts\activate
    # Activate the environment (macOS/Linux)
    source .venv/bin/activate
    ```

3.  **Install Dependencies**
    This project's dependencies are listed in the `requirements.txt` file. Install them with pip:
    ```bash
    pip install -r requirements.txt
    ```

4.  **Run the Notebook**
    Once the setup is complete, you can open and run the `EDA and Stress Prediction Model.ipynb` file in a Jupyter environment like VS Code or Jupyter Lab.

## 📊 Dataset

The dataset used in this analysis is the **"Global High School Student Lifestyle & Wellness"** dataset, sourced from Kaggle. The data is contained in the `student life.csv` file.

## 💻 Tools and Libraries

* **Python 3.12**
* **Pandas** for data manipulation and analysis.
* **Seaborn & Matplotlib** for data visualization.
* **Scikit-learn** for machine learning (data splitting, modeling, and evaluation).
* **Jupyter Notebook** as the development environment.
