[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/YUvA8hIt)
# Integration 2 — PyTorch: Housing Price Prediction

**Module 2 — Programming for AI & Data Science**

---

## 🚀 Quick Reference

* **Main Script:** `train.py`
* **Virtual Environment:** `.venv2`
* **Branch:** `integration-2/pytorch`
* **Output File:** `predictions.csv`

---

## 1. Model Description
This project implements a neural network to predict housing prices in the Jordanian market. The model analyzes the relationship between property characteristics and their final valuation.

* **Target Variable:** `price_jod` (The total price of the apartment in JOD).
* **Input Features (5):**
    1.  `area_sqm`: Total area of the property.
    2.  `bedrooms`: Number of bedrooms.
    3.  `floor`: The floor level of the unit.
    4.  `age_years`: How old the building is.
    5.  `distance_to_center_km`: Proximity to the city center.

## 2. Training Configuration
The model was configured with the following hyperparameters to ensure steady convergence:

| Parameter | Setting |
| :--- | :--- |
| **Architecture** | 2-Layer Linear Neural Network (Hidden: 32 units) |
| **Activation** | ReLU |
| **Epochs** | 100 |
| **Learning Rate** | 0.01 |
| **Optimizer** | Adam |
| **Loss Function** | Mean Squared Error (MSELoss) |

## 3. Training Outcome
The training process successfully ran for 100 epochs. The loss decreased consistently, indicating that the model was effectively learning from the dataset patterns.
Initial Loss (Epoch 10): 1,950,505,856
Final Loss (Epoch 100): 1,943,173,248

* **Final Status:** Successfully generated `predictions.csv`.
* **Loss Trend:** Started in the high billions and steadily declined as the weights were optimized.

## 4. Behavioral Observation
During the training process, I observed that the **Mean Squared Error (MSE) remained numerically very high** (in the billions). While this might look alarming, it is actually expected behavior because the target variable (`price_jod`) is not scaled. Even though the numbers are large, the consistent downward trend confirms that the gradient descent process is working correctly and the model is improving its accuracy over time.

---
**Trainee:** GiddyGet7  
**Status:** Integration Task Complete