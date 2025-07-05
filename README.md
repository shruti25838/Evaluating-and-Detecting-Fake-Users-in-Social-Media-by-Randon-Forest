# Fake Account Detection using Random Forest and GAN-based Augmentation

This project aims to classify social media accounts as **real or fake** using machine learning techniques, specifically focusing on **Random Forest classification** and **data augmentation with GANs (Generative Adversarial Networks)**. By analyzing user-level features such as follower count, profile bio length, and media activity, the model learns to identify patterns associated with fake accounts.

---

## Objective

With the increasing presence of bots and fake accounts on social platforms, it's critical to develop automated tools that can flag suspicious behavior. This project tackles that problem using a two-stage approach:
1. Train a robust Random Forest classifier on labeled real/fake account data.
2. Enhance the dataset using GAN-generated synthetic samples to improve generalization.

---

## Project Workflow

### Step 1 – Data Import and Conversion
- Loaded two separate JSON files: `realAccountData.json` and `fakeAccountData.json`
- Converted them into structured CSV format for preprocessing

### Step 2 – Merging the Datasets
- Combined both datasets into one unified DataFrame
- Added a binary label `isFake` to distinguish between real (0) and fake (1) accounts

### Step 3 – Correlation Analysis
- Performed correlation analysis across all numerical and binary features
- Helped identify which variables most strongly influence the fake/real classification

### Step 4 – Data Visualization
- Used visual tools like:
  - Heatmaps for correlation
  - Histograms and boxplots for feature distribution
  - Scatter plots for pairwise analysis

### Step 5 – Train/Test Split
- Split the combined dataset into training and test subsets (typically 80:20)
- Ensured class balance and randomized sampling for unbiased evaluation

### Step 6 – Data Augmentation with GANs
- Developed and trained a GAN model to generate additional realistic account data
- Augmented both real and fake classes to address data imbalance and enrich patterns
- Merged synthetic data with original to create a more comprehensive training set

### Step 7 – Random Forest Classification
- Implemented the Random Forest algorithm using `scikit-learn`
- Process:
  - Installed and imported necessary packages
  - Trained the model on the augmented dataset
  - Made predictions on the test set

### Step 8 – Model Evaluation
- Assessed model performance using:
  - **Confusion Matrix** – To identify false positives/negatives
  - **Classification Report** – Including precision, recall, and F1-score
  - **Overall Accuracy** – To gauge prediction effectiveness

---

## Features Used

The dataset includes key features such as:

- `userFollowerCount`
- `userFollowingCount`
- `userBiographyLength`
- `userMediaCount`
- `userHasProfilPic` (binary)
- `userIsPrivate` (binary)
- `usernameDigitCount`
- `usernameLength`

---

## Conclusion

This pipeline demonstrates that combining traditional machine learning (Random Forest) with synthetic data generation (GANs) can result in a powerful system for detecting fake accounts on social media platforms. The model performs well in classification tasks and offers room for further improvement with ensemble methods or deep learning classifiers.

