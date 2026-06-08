# Physiological-Stress-Classification

Overview

This project implements a complete **end-to-end machine learning pipeline** for detecting 
psychological stress from wearable physiological signals, built on the 
**WESAD (Wearable Stress and Affect Detection)** dataset from the University of Siegen.

The human body responds to stress through the **autonomic nervous system (ANS)** — 
triggering measurable changes in heart rate, skin conductance, muscle tension, breathing, 
and skin temperature. This project captures those changes using five biosignals recorded 
from a chest-worn sensor and trains machine learning models to automatically classify 
mental states in a subject-independent manner.



    What This Project Does

1. Processes 5 physiological signals — ECG, EDA, EMG, RESP, TEMP — sampled at 700 Hz
2. Extracts 35 handcrafted features- per 60-second sliding window (time-domain, frequency-domain, and nonlinear)
3. Trains 4 classifiers — Random Forest, Gradient Boosting, SVM, Logistic Regression
4. Evaluates with LOSO-CV — Leave-One-Subject-Out cross-validation across 15 subjects for true subject-independent generalization
5. Supports two modes — plug in real WESAD `.pkl` files or run instantly with the built-in synthetic data generator
Visualizes everything — confusion matrices, feature importance, per-subject accuracy, signal waveforms, physiological radar charts
6. Saves a production-ready model — reload and run `predict_stress()` on any new window
