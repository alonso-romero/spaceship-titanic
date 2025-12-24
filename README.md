![Repo Image](title.png)

## 📌 Project Overview

In the year 2912, the Spaceship Titanic, an interstellar passenger liner, collided with a spacetime anomaly while rounding Alpha Centauri. Although the ship remained intact, almost half of the passengers were transported to an alternate dimension.

This project aims to build a machine learning model to predict which passengers were "transported" by the anomaly using records recovered from the ship's damaged computer system.

## 🎯 Objective
The goal is to perform a binary classification to predict the Transported status (True/False) for each passenger in the test set. Success is measured by **Classification Accuracy**.

## 📊 Dataset Description
The dataset consists of personal records for ~13,000 passengers:

- `PassengerId`: A unique Id for each passenger (gggg_pp).
- `HomePlanet`: The planet the passenger departed from.
- `CryoSleep`: Whether the passenger was in suspended animation.
- `Cabin`: Cabin number where the passenger stayed (`deck`/`num`/`side`).
- `Age`: Passenger age.
- `VIP`: Whether the passenger paid for special service.
- **Luxury Amenities**: Expenditure in `RoomService`, `FoodCourt`, `ShoppingMall`, `Spa`, and `VRDeck`.
- `Transported`: The target variable (only in `train.csv`).

## 🛠️ Methodology

1. Exploratory Data Analysis (EDA): Visualizing feature distributions and correlations (e.g., the impact of `CryoSleep` on transportation rates).

2. Data Preprocessing:
- Handling missing values (Imputation).
- Feature engineering: Extracting `Deck` and `Side` from the `Cabin` feature.
- Encoding categorical variables.

3. Modeling: The primary model utilized is a **Gradient Boosting Classifier (GBC)**.
- Evaluation was conducted using standard classification metrics.

4. Results Generation: Predictions were exported to `gbc_test.csv`.

## 📂 Repository Structure

- `Spacehip-Titanic-Project.ipynb`: Main Jupyter Notebook containing EDA, preprocessing, and model training.
- `train.csv` / `test.csv`: Raw data from Kaggle.
- `Results.pdf`: Summary report of the model's performance and findings for a non-technical audience.
- `Final Project Presentation.pptx`: A slide deck detailing the project's journey and outcomes.
- `gbc_test.csv`: Final predictions using Gradient Boosting.
- `transported_passengers.csv`: Processed output of predicted transported individuals.

## ⚙️ How to Run

1. Clone the repository
```bash
git clone https://github.com/alonso-romero/spaceship-titanic.git
```

2. Install dependencies
```bash
pip install -r requirements.txt
```

3. Open `Spaceship-Titanic-Project.ipynb` in Jupyter or VS Code to view the analysis

## 🚀 Results

Detailed performance metrics can be found in `Results.pdf`.