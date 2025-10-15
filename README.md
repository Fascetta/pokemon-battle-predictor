# Pokémon Battle Winner Prediction 🏆

This repository contains the code and methodology for the **Pokémon Battles Prediction** Kaggle competition, part of the **Fundamentals of Data Science** course at Sapienza University of Rome (I Semester 2025-2026).

The goal of this project is to train a machine learning model that can accurately predict the winner of a Pokémon battle using only the data from the first 30 turns.


## The Challenge 🧠

The problem is a **binary classification task** where the model must predict the `player_won` feature. The main challenge lies not in the classification itself, but in feature engineering. The data is provided in `.jsonl` format, where each line is a complex JSON object containing nested information about a single battle.

Our mission is to parse this complex data, create powerful features, and build a model that generalizes well to unseen test data.

## Methodology 🔬

Our approach to this problem is structured around three key areas:

#### 1. Feature Engineering & Selection
The raw data is grouped into two main types:
* **Static Features:** Pre-battle information, such as the stats and types for all 6 Pokémon on a player's team.
* **Dynamic Features:** Live battle information that changes turn-by-turn, including HP percentages and status changes over 30 turns

We will engineer features that quantify type matchups, momentum shifts, and overall team strength.

#### 2. Model Experimentation
We will explore a variety of models, starting with a simple baseline (e.g., Logistic Regression) and iterating towards more complex and powerful algorithms like Gradient Boosting. The process will involve careful tuning of hyperparameters to optimize performance.

#### 3. Robust Validation
To avoid the "Optimism" trap of evaluating on training data, we will rely on a strong local validation strategy.
* Our primary guide for model selection and tuning will be **k-fold Cross-Validation**.
* The public leaderboard will only be used as a final sanity check, not as a validation set, to prevent overfitting to its small data slice.

## Getting Started 🚀

To reproduce our results, follow these steps:

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/](https://github.com/)[Your-Username]/pokemon-battle-predictor.git
    cd pokemon-battle-predictor
    ```

2.  **Set up a virtual environment:**
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
    ```

3.  **Install dependencies:**
    ```bash
    pip install -r requirements.txt
    ```

4.  **Add Data:**
    Download the `train.jsonl` and `test.jsonl` files from the Kaggle competition page and place them in a `data/` directory in the root of the project.

5.  **Run the analysis:**
    Open and run the Jupyter Notebook to see the data processing, training, and prediction pipeline.
    ```bash
    jupyter notebook "Main Notebook.ipynb"
    ```

## Competition Details

* **Competition Starts:** Monday, October 13
* **Competition Ends:** Friday, November 14
* **Evaluation Metric:** Accuracy

---

> [cite_start]TA: Leonardo Rocci (`rocci.1922496@studenti.uniroma1.it`) [cite: 13, 17]
