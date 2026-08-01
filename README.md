# UrbanStay Hotel Booking Cancellation Prediction

<img width="300" height="200" alt="image" src="https://github.com/user-attachments/assets/f2cdf2f3-8eb1-498f-ba84-12e8a933b723" />


A comprehensive machine learning project aimed at predicting hotel booking cancellations to improve the economic efficiency of the UrbanStay hotel chain. The project involves extracting data directly from a PostgreSQL database, performing exploratory data analysis, and building a binary classification model to identify high-risk bookings.

## Project Description
Booking cancellations lead to significant revenue loss for hotels. To mitigate this, hotels can introduce a deposit system, but applying it to all customers might decrease overall booking volume. The goal of this project is to develop a machine learning model that predicts whether a specific customer will cancel their booking. 

By accurately identifying potential cancellations, the hotel can selectively request deposits only from high-risk customers, thereby minimizing financial losses without alienating reliable guests. The project also includes a calculation of the model's economic impact to ensure that its implementation is financially viable for the business.

## Goals and Objectives
- Establish a connection to the PostgreSQL database and extract historical booking and review data using `SQLAlchemy`.
- Perform Exploratory Data Analysis (EDA) to understand the factors influencing cancellations.
- Preprocess data, handle missing values, and engineer new features (including NLP features from customer reviews using TF-IDF).
- Train and evaluate multiple classification models (Logistic Regression, Decision Tree, Random Forest).
- Optimize hyperparameters to maximize the chosen business metric.
- Calculate the economic efficiency of the model to prove its profitability for the hotel chain.

## Tech Stack
- Python
- Pandas, NumPy
- SQLAlchemy, psycopg2 (Database connection and SQL queries)
- Scikit-learn (Modeling, TF-IDF Vectorizer, Pipelines, Cross-validation)
- Matplotlib, Seaborn, Phik (Data visualization and correlation analysis)

## Setup and Configuration
This project connects to an external PostgreSQL database. For security reasons, the database credentials are not hardcoded in the notebook. 

To run the notebook, you need to provide your own database credentials using environment variables. 

1. Copy the `.env.example` file to `.env`:
   ```bash
   cp .env.example .env
   ```
2. Fill in your actual database credentials in the `.env` file.
3. Load the environment variables before running Jupyter:
   ```bash
   export $(cat .env | xargs) && jupyter notebook
   ```

## Project Structure
- `hotel_booking_cancellation.ipynb` — The main Jupyter Notebook containing the full pipeline from SQL data extraction to model training and economic evaluation.
- `.env.example` — Template for database credentials.
- `requirements.txt` — List of required Python packages.

## Results
The project successfully developed a classification model capable of predicting booking cancellations. The economic evaluation demonstrated that implementing this model to selectively target high-risk bookings for deposits yields a positive financial impact, significantly reducing the revenue lost to last-minute cancellations.
