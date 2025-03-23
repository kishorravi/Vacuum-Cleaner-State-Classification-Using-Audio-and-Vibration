# 🧹 Intelligent Vacuum Cleaner State Classification using Audio and Vibration Data

This project is a **Proof of Concept (PoC)** that demonstrates how **machine learning** can be used to classify the operational state of a **vacuum cleaner** using data from **vibration sensors** and **audio recordings**. The system achieves **100% accuracy** on a well-structured benchmark dataset, validating its potential for industrial, commercial, and smart home applications.

---

## 💼 Business Case

Vacuum cleaners — both consumer-grade and industrial — operate under various conditions, including changes in speed, obstructions, and cover states. Identifying these states in real-time is critical for:

- **Smart automation**
- **User safety**
- **Predictive maintenance**
- **Operational efficiency**

This PoC shows how we can use **low-cost IoT sensors** and **ML classification** to automatically detect and respond to such states. It sets the stage for **AI-enhanced appliances** and **edge-based fault detection systems**.

---

## 🧪 Objective

> Predict the **operational state** of a vacuum cleaner using its **real-time sensor data** (vibration and audio), classifying it into one of 13 predefined states such as:
>
> - Low Speed / High Speed
> - Obstruction / No Obstruction
> - Cover Open / Closed

---

## 📊 Dataset Overview

**Source**: [Vacuum Vibration Monitoring Dataset](https://www.kaggle.com/datasets/ricardofebra/vacuum-vibration-monitoring)

| Sensor Type | Format | Details |
|-------------|--------|---------|
| Audio       | CSV    | 1 column (`mic`) - microphone time-series |
| Vibration   | CSV    | 3 columns (`acc_x`, `acc_y`, `acc_z`) - accelerometer time-series |
| Labels      | Embedded in filenames (e.g., `label_03.csv`) | Represents 1 of 13 vacuum states |

Each vacuum cleaner condition has one sample (13 total), labeled from `00` to `12`. These are mapped to real-world vacuum conditions like speed, obstruction presence, and cover state.

---

## 🧠 ML Pipeline

### 🔧 Preprocessing
- Load audio and vibration files
- Extract statistical features:
  - Mean, Std Dev, Min, Max, Median
  - Percentiles (25%, 75%), Energy, Zero-Crossing Rate

### 🧠 Model
- **Algorithm**: `RandomForestClassifier` (scikit-learn)
- **Features**: Combined audio + vibration features
- **Performance**:
  - Accuracy: **100%**
  - F1 Score: **1.00**
  - Precision/Recall: **1.00**

> ⚠️ Note: Due to limited sample size, the model is trained and evaluated on the full dataset. For production deployment, more samples per state are required for generalization.

---

## 🧰 Project Structure

