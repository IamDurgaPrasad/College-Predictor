# College Predictor 

A web application that predicts college and branch preferences for JEE Advanced rank holders, backed by data-driven trends and analytics.

---

##  Table of Contents

1. [Overview](#overview)  
2. [Features](#features)  
3. [Architecture & Tech Stack](#architecture--tech-stack)  
4. [How It Works](#how-it-works)  
5. [Setup & Installation](#setup--installation)  
6. [Usage](#usage)  
7. [Project Structure](#project-structure)  
8. [Future Improvements](#future-improvements)  
9. [Contributions & License](#contributions--license)  

---

## Overview

This project provides a predictive tool for students with JEE Advanced ranks to estimate their chances of admission into various institutes and branches. It factors in historical counseling data, institute trends, and branch-wise seat distributions to generate informed predictions.

---

## Features

- Predict probable branch & institute choices based on rank.  
- Insights on branch-wise and institute-wise trends to guide decision-making.  
- Data scraping and preprocessing of official JoSAA counseling records.  
- Clean, interactive frontend with visualizations for easier interpretation.

---

## Architecture & Tech Stack

| Layer / Component        | Technology / Libraries                      |
|--------------------------|---------------------------------------------|
| Backend                  | Python, Django                              |
| Data Acquisition         | BeautifulSoup, Requests                      |
| Data Cleaning & Preproc  | Pandas, NumPy                               |
| Database                 | SQLite (for local dev/testing)              |
| Frontend & Visualization | HTML, CSS, JavaScript, Chart.js             |
| Deployment / Local Setup | Django’s built-in server                    |

---

## How It Works

1. **Data Collection & Cleaning**  
   - Scrapes JoSAA counseling data tables using BeautifulSoup.  
   - Standardizes institute and branch labels, handles missing values, and structures the data using Pandas.

2. **Trend Extraction & Modeling**  
   - Aggregates historical data to derive the relationship between ranks, branches, and institutes.  
   - Uses statistical/rank-based models to estimate probable admissions and generate predictions.

3. **Prediction & Recommendation**  
   - Given a user’s JEE Advanced rank, queries processed data to suggest likely branches and institutes.  
   - Visualizes trends: seat allotments, admission thresholds, and comparative analytics.

4. **User Interface**  
   - Frontend displays input form, predictions list, and trend charts dynamically.  
   - Chart.js is used for rendering branch/institute-wise visual insights.

---

## Setup & Installation

```bash
# Clone the repo
git clone https://github.com/IamDurgaPrasad/College-Predictor.git
cd College-Predictor

# (Optional) Create and activate a virtual environment
python3 -m venv venv
source venv/bin/activate   # Unix/Mac
venv\Scripts\activate      # Windows

# Install dependencies
pip install -r requirements.txt

# Run migrations and populate initial data (if applicable)
python manage.py migrate

# Run the development server
python manage.py runserver

# Open browser at:
http://localhost:8000/

##  Usage

- Enter a **JEE Advanced rank** in the input field.  
- Click **"Get Predictions"** to view recommended institutes and branches.  
- Explore **visual charts** showing historical trends and comparative analytics.

```


##  Project Structure

College-Predictor/
├── MainApp/ # Django application folder
├── JoSAA/ # Data scraping / preprocessing modules
├── webscrapping_scripts_and_files/
├── static/ # Static assets (CSS, JS, images)
├── templates/ # HTML templates
├── manage.py
└── requirements.txt

## Future Improvements

Expand to support other exams (e.g. JEE Main, state exams).

Integrate machine learning algorithms for better predictive accuracy.

Add user authentication + personalized recommendation history.

Store data in a scalable DB (PostgreSQL, etc.), host the app online.

Add confidence scores or ranges instead of single predictions.
