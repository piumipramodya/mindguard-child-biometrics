# MindGuard: Child-Aware Adaptive Method for Social Media Addiction Reduction

[![Platform](https://img.shields.io/badge/Platform-Android%20API%2026%2B-green.svg)]()
[![Methodology](https://img.shields.io/badge/Method-Edge%20AI%20%7C%20Sensor%20Fusion-blue.svg)]()
[![Domain](https://img.shields.io/badge/Domain-Digital%20Wellbeing-orange.svg)]()

> **Final Year Research Dissertation | NSBM Green University**  
> *Author:* N.W.P.P.P. Nanayakkara  
> *Principal Supervisor:* Eng. Prabhath Buddhika  

---

## 📌 Executive Summary

Traditional digital wellbeing applications rely on static timers or easily circumvented PINs that fail on shared family devices. **MindGuard** is a novel, on-device Edge AI framework combining **Touch Biometrics**, **Inertial Sensor Fusion**, and **Just-In-Time Adaptive Interventions (JITAI)** to passively verify individual child profiles (ages 3–12) and mitigate compulsive social media overuse.

---

## 🏛️ System Architecture

The architecture operates entirely on-device to preserve privacy and minimize latency, using a two-stage hierarchical model:

```mermaid
graph TD
    A[Touch & Motion Stream] --> B[Feature Extraction Layer<br/>16 Features: Touch + Accel + Gyro]
    B --> C[Stage 1: Random Forest Classifier<br/>Age Demographics Detection]
    
    C -->|Adult Detected| D[Adult Profile<br/>System Dormant]
    C -->|Child Detected| E[Stage 2: Child Identity Verification<br/>6D Weighted Euclidean Distance]
    
    E -->|Identity Confirmed| F[Decoupled Kinematic JITAI Engine<br/>Personalized Z-Score Tracking]
    E -->|Identity Unverified| G[Access Denied / Re-Authentication]
    
    F --> H[Adaptive Intervention Engine<br/>5-Strike Counter & 15s Integrity Timer]
    H --> I[Distraction-Free Break Mode<br/>Cognitive Micro-Games & Gamified Avatars]
