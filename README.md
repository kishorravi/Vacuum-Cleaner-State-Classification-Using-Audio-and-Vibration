# 🧹 Vacuum Cleaner State Classification Using Audio and Vibration

This project is a **Proof of Concept (PoC)** that uses **audio and vibration sensor data** to classify the operational states of a **vacuum cleaner** using a machine learning model.

> ✅ **Model Accuracy**: 100% (on full dataset)

---

## 📌 Business Case

Vacuum cleaners (especially in industrial or robotic settings) can benefit from **real-time operational monitoring**. This PoC demonstrates how **affordable sensor data** (audio + vibration) and **machine learning** can be combined to:

- Detect obstructions or anomalies
- Monitor motor speed and behavior
- Identify open/closed cover states
- Enable predictive maintenance and reduce downtime

> ⚙️ This approach helps make vacuum cleaners **smarter, safer, and more efficient**.

---

## 🧠 Project Summary

- **Dataset**: [Vacuum Vibration Monitoring](https://www.kaggle.com/datasets/ricardofebra/vacuum-vibration-monitoring)
- **Sensors**:
  - Microphone (Audio: `mic`)
  - Accelerometer (`acc_x`, `acc_y`, `acc_z`)
- **Model**: `RandomForestClassifier` from scikit-learn
- **Features**: Statistical summaries from audio and vibration signals
- **States**: 13 labeled vacuum operating conditions

---

## 📁 Folder Structure

