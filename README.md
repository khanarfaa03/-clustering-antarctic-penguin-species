# Clustering Antarctic Penguin Species

## Overview
This project performs unsupervised machine learning and statistical analysis on the Antarctic Penguin dataset. Using **K-Means Clustering**, the goal is to segment penguin populations based on physical measurements (culmen length, culmen depth, flipper length, and body mass) and validate significant morphological differences across clusters using **Hypothesis Testing (ANOVA)**.

---

## Dataset
The dataset (`penguins.csv`) contains physical measurements and categorical data collected from three penguin species (*Adélie*, *Chinstrap*, and *Gentoo*) across islands in the Palmer Archipelago, Antarctica:
- `species`: Penguin species
- `island`: Island location (Biscoe, Dream, Torgersen)
- `culmen_length_mm`: Length of the dorsal ridge of the beak
- `culmen_depth_mm`: Depth of the beak
- `flipper_length_mm`: Length of the flipper
- `body_mass_g`: Body mass in grams
- `sex`: Gender of the penguin

---

## Workflow
1. **Preprocessing & Encoding:** Clean missing values, encode categorical variables using one-hot encoding (`pd.get_dummies`), and standardize numerical features (`StandardScaler`).
2. **Optimal Cluster Selection:** Use the **Elbow Method** (Inertia vs. $K$) to identify the optimal number of clusters ($K=4$).
3. **Model Fitting:** Train the `KMeans` algorithm and map cluster labels back to the original dataset.
4. **Hypothesis Testing:** Perform One-Way Analysis of Variance (**ANOVA**) to test whether mean physical attributes significantly differ across identified clusters.

---

## Key Results
- **Optimal Clusters:** $K = 4$ clusters best separate penguins by morphological traits and sex differentiation.
- **Hypothesis Testing (ANOVA):** Statistically significant differences ($p < 0.05$) exist across cluster means for `culmen_length_mm`, `culmen_depth_mm`, and `flipper_length_mm`, confirming that K-Means effectively captured distinct biological phenotypes.

---

## Quick Start
```bash
# Clone repository
git clone [https://github.com/your-username/clustering-antarctic-penguin-species.git](https://github.com/your-username/clustering-antarctic-penguin-species.git)
cd clustering-antarctic-penguin-species

# Install dependencies
pip install pandas numpy matplotlib seaborn scikit-learn scipy

# Run script
python main.py
# -clustering-antarctic-penguin-species
Unsupervised K-Means clustering and hypothesis testing on the Palmer Archipelago Antarctic Penguin dataset to identify structural species groupings and validate morphological variance across clusters.
