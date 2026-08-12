<div align="center">

# Upani Ayodya Gunathunga

**Biomedical Engineering Undergraduate · University of Moratuwa**

*Computer vision, Signal Processing, Electronics and embedded intelligence for human-centered healthcare and assistive systems*

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Upani_Gunathunga-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/upani-gunathunga-biomedicaleng)
[![Email](https://img.shields.io/badge/Email-upaniayodhya@gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:upaniayodhya@gmail.com)
[![Location](https://img.shields.io/badge/Colombo-Sri_Lanka-3C8B5A?style=for-the-badge&logo=googlemaps&logoColor=white)]()

![Profile Views](https://komarev.com/ghpvc/?username=Upani-Gunathunga&label=Profile%20views&color=blueviolet&style=flat)

</div>

---

## 👩‍🔬 About Me

Third-year **Biomedical Engineering** undergraduate (CGPA **3.84 / 4.0**, two Dean's List semesters) in the Department of Electronic and Telecommunication Engineering, University of Moratuwa.



---

## 🧭 Research Interests

<table>
<tr>
<td width="33%" valign="top">


**Computer Vision**

Vision-based assistive tech
Human–Computer Interaction
Vision for healthcare
Embedded CV · Edge AI
Applied AI for real problems

</td>
<td width="33%" valign="top">


**Machine Learning**

Deep Learning · PyTorch
Medical image segmentation
Embedded ML / TinyML
Vision models
Real-time inference

</td>
<td width="33%" valign="top">


**Autonomous Robotics**

Robot perception
LiDAR processing · SLAM
Navigation
Coverage path planning
Mobile robotics

</td>
</tr>
</table>

> The thread connecting these: **intelligent systems that perceive, decide, and act on real hardware, in real environments, for real users.**

---

## 🔬 Featured Research Projects

### 🩻 UNeXt-PyTorch-BUSI — Reproducing a MICCAI 2022 Architecture

![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?logo=pytorch&logoColor=white)
![Medical Imaging](https://img.shields.io/badge/Medical_Image_Segmentation-0A9396)
![Computer Vision](https://img.shields.io/badge/Computer_Vision-5A189A)
![Status](https://img.shields.io/badge/Ongoing-2026-yellow)

**Problem** — Ultrasound segmentation models are often too heavy for point-of-care devices. UNeXt (MICCAI 2022) proposes an MLP-based alternative to heavy convolutional decoders.

**Approach**
- Reproducing the paper from scratch in PyTorch: convolutional encoder–decoder backbone, tokenized MLP block with axial feature shifting, combined **Dice + BCE** loss
- Training and validating on the **BUSI** dataset (647 clinical breast ultrasound images, benign/malignant) with best-validation-loss checkpointing to control overfitting
- Full modular pipeline — custom `Dataset`/`DataLoader`, training loop, **IoU/F1** evaluation against paper-reported benchmarks, video-frame inference for real-time segmentation

**Why it matters** — Reading a paper closely enough to rebuild it, then verifying the numbers, is the core skill this project was chosen to develop.

---

### 🤟 SignPath — Sri Lankan Sign Language Tutor

![MediaPipe](https://img.shields.io/badge/MediaPipe-0097A7?logo=google&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?logo=opencv&logoColor=white)
![Raspberry Pi](https://img.shields.io/badge/Raspberry_Pi_5-A22846?logo=raspberrypi&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-000000?logo=flask&logoColor=white)
![HCI](https://img.shields.io/badge/HCI-6A4C93)
![Status](https://img.shields.io/badge/Ongoing-2026-yellow)

**Problem** — Most hearing parents of deaf children in Sri Lanka never learn SLSL, and no learning tool exists for the language. Cloud-based solutions fail where connectivity and cost are constraints.

**Approach**
- Real-time SLSL recognition on a **Raspberry Pi 5** using MediaPipe hand landmark detection, streamed from a mobile camera
- Fully **offline** web dashboard giving learners live feedback on their signing — no internet dependency

**Why it matters** — As much an HCI problem as a vision problem: the design question is what feedback actually helps a non-expert correct their own hand shape. Offline operation forces real decisions about latency and model footprint at the edge.

---

### 🫁 Embedded Respiratory Breath Classifier

![ESP32](https://img.shields.io/badge/ESP32--S3-E7352C?logo=espressif&logoColor=white)
![Embedded ML](https://img.shields.io/badge/Embedded_ML-FF6F00)
![Signal Processing](https://img.shields.io/badge/Signal_Processing-1B4965)
![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)

**Problem** — Respiratory monitoring hardware is expensive. Can useful breath classification run *entirely* on a low-cost microcontroller with no cloud link?

**Approach**
- **I2S** audio acquisition from an INMP441 MEMS microphone, with a state-machine breath segmentation pipeline
- On-device feature extraction: RMS, ZCR, variance, duration
- Multiclass logistic regression trained on the **Respiratory Sound Database**, deployed directly to the ESP32-S3
- LED feedback: Short → 🔴 | Normal → 🔵 | Long → 🟢

**Why it matters** — TinyML under hard memory and latency budgets: feature design driven by what the silicon can sustain, not by what scores best offline.

---

### 🤖 Smart Autonomous Floor Mopping Robot (SAFMR)

![ROS2](https://img.shields.io/badge/ROS2_Jazzy-22314E?logo=ros&logoColor=white)
![SLAM](https://img.shields.io/badge/SLAM-0B7285)
![LiDAR](https://img.shields.io/badge/RPLidar_C1-2D6A4F)
![STM32](https://img.shields.io/badge/STM32-03234B?logo=stmicroelectronics&logoColor=white)
![C++](https://img.shields.io/badge/C++-00599C?logo=cplusplus&logoColor=white)

**Problem** — Complete-coverage navigation in unmapped indoor spaces, on a low-cost hardware stack.

**Approach**
- Simulated a SLAM-based self-navigation system in **ROS2 Jazzy** with `slam_toolbox`, using **boustrophedon cellular decomposition** for full-floor coverage path planning
- Deployed on hardware: RPLidar C1 processing on a Raspberry Pi 5, fused with **MPU6050 IMU** data for real-time rotation correction during navigation
- Designed the sensor integration PCB schematic in Altium Designer

**Why it matters** — The gap between a clean simulation and a robot that drifts on a real floor is where the interesting work is. This project is the origin of my interest in robot perception and SLAM.

---

### 🩺 Early Diabetes Prediction — XGBoost ML Pipeline

![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)
![XGBoost](https://img.shields.io/badge/XGBoost-0095D5)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-F7931E?logo=scikitlearn&logoColor=white)
![Medical ML](https://img.shields.io/badge/Medical_ML-C1121F)

**Problem** — Small, noisy clinical tabular datasets (Pima Indians Diabetes Database, 768 patients) reward careful methodology far more than model complexity.

**Approach**
- Engineered 8 candidate features (log transforms, interaction terms, ratio features)
- Greedy forward selection via **5-fold cross-validated AUC** to prevent overfitting
- XGBoost with RandomizedSearchCV (40 combinations × 5-fold CV), class imbalance correction, L1/L2 regularisation
- False-positive error analysis — identified **Age** as the primary misclassification driver; designed and evaluated hard-removal vs. soft-penalisation correction pipelines

**Why it matters** — Deliberate emphasis on error analysis and validation discipline: understanding *why* a clinical model fails matters more than its headline metric.

---

### 🏥 Adaptive Smart Gravity-Based Infusion Pump Monitor

![ESP32](https://img.shields.io/badge/ESP32-E7352C?logo=espressif&logoColor=white)
![C++](https://img.shields.io/badge/C++-00599C?logo=cplusplus&logoColor=white)
![IoT](https://img.shields.io/badge/IoT-00838F)
![React](https://img.shields.io/badge/React-61DAFB?logo=react&logoColor=black)

**Problem** — Ward-level infusion monitoring is unaffordable for low-resource clinical settings. Requirements gathered directly from **Apeksha Hospital, Sri Lanka**.

**Approach**
- Low-cost IoT ward-level monitoring system with patient history integration
- Evaluated the feasibility of **IR-drop sensing** on ESP32 as the sensing front end

🏆 Semi-Finalist — HackX, University of Kelaniya
🏆 Finalist — Startup Spark 2.0, IESL (Techno 2025)
🏆 Finalist — Pitch Arena, University of Ruhuna (Rextro 2025)

---

<details>
<summary><b>🔧 Earlier hardware & systems work</b></summary>

<br>

**🌡️ Electronic Hot & Cold Compression Device**
![ATmega328P](https://img.shields.io/badge/ATmega328P-00979D)
![Altium](https://img.shields.io/badge/Altium_Designer-A5915F?logo=altiumdesigner&logoColor=white)
![SolidWorks](https://img.shields.io/badge/SolidWorks-E1251B?logo=dassaultsystemes&logoColor=white)
Low-cost closed-loop hot–cold therapy device built around a Peltier module, with logic-level MOSFET control, custom firmware, and a custom PCB.

**🎸 Analog Acoustic Guitar Tuner**
![Analog](https://img.shields.io/badge/Analog_Electronics-333333)
![Altium](https://img.shields.io/badge/Altium-A5915F?logo=altiumdesigner&logoColor=white)
PCB design and output indication circuitry for a fully analog tuner.

**🏁 IESL RoboGames 2025 — Preliminary Round**
![C](https://img.shields.io/badge/C-A8B9CC?logo=c&logoColor=black)
![Webots](https://img.shields.io/badge/Webots-1E88E5)
Autonomous maze navigation with an e-puck robot using left-wall-following and sequential colored marker detection.

**📡 Bluetooth Mobile Robot with Collision Avoidance**
![Java](https://img.shields.io/badge/Java-007396?logo=openjdk&logoColor=white)
![Embedded](https://img.shields.io/badge/Embedded_Systems-4A4A4A)
Wireless teleoperation over Bluetooth serial with a custom Java Swing control interface and embedded firmware.

</details>

---

## 🛠️ Technical Skills

### Computer Vision & Deep Learning
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?logo=pytorch&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?logo=tensorflow&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?logo=opencv&logoColor=white)
![MediaPipe](https://img.shields.io/badge/MediaPipe-0097A7?logo=google&logoColor=white)

CNNs · U-Net · YOLO · Transfer learning (MobileNetV2, ResNet) · Medical image segmentation · Custom architecture implementation · Loss design (Dice + BCE) · Hyperparameter tuning

### Machine Learning
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-F7931E?logo=scikitlearn&logoColor=white)
![XGBoost](https://img.shields.io/badge/XGBoost-0095D5)
![NumPy](https://img.shields.io/badge/NumPy-013243?logo=numpy&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?logo=pandas&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557C)

Supervised learning · Feature engineering · Cross-validation · Model evaluation · Error analysis

### Embedded Systems & Edge AI
![ESP32](https://img.shields.io/badge/ESP32-E7352C?logo=espressif&logoColor=white)
![STM32](https://img.shields.io/badge/STM32-03234B?logo=stmicroelectronics&logoColor=white)
![Raspberry Pi](https://img.shields.io/badge/Raspberry_Pi_5-A22846?logo=raspberrypi&logoColor=white)
![Arduino](https://img.shields.io/badge/ATmega328P-00979D?logo=arduino&logoColor=white)

Embedded ML · TinyML · I2S audio · Sensor data processing · Sensor fusion · Firmware development

### Robotics & Simulation
![ROS2](https://img.shields.io/badge/ROS2_Jazzy-22314E?logo=ros&logoColor=white)
![Gazebo](https://img.shields.io/badge/Gazebo-FF6600)

SLAM (`slam_toolbox`) · LiDAR processing · IMU fusion · Coverage path planning · Autonomous navigation

### Programming
![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)
![C++](https://img.shields.io/badge/C++-00599C?logo=cplusplus&logoColor=white)
![C](https://img.shields.io/badge/C-A8B9CC?logo=c&logoColor=black)
![SQL](https://img.shields.io/badge/SQL-4479A1?logo=mysql&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)

### Hardware & Design Tools
![Altium](https://img.shields.io/badge/Altium_Designer-A5915F?logo=altiumdesigner&logoColor=white)
![SolidWorks](https://img.shields.io/badge/SolidWorks-E1251B?logo=dassaultsystemes&logoColor=white)
![Fusion](https://img.shields.io/badge/Fusion-F16529?logo=autodesk&logoColor=white)

PCB schematic & layout design · Closed-loop control hardware · Prototyping

---

## 📊 GitHub Activity

<div align="center">



[![GitHub Streak](https://streak-stats.demolab.com?user=Upani-Gunathunga&theme=radical&hide_border=true)](https://git.io/streak-stats)

[![GitHub Contribution Graph](https://github-readme-activity-graph.vercel.app/graph?username=Upani-Gunathunga&theme=radical&hide_border=true)](https://github.com/Upani-Gunathunga)

</div>

---

## 🎓 Education

**B.Sc. (Hons) Biomedical Engineering** — University of Moratuwa · *March 2024 – Present*
Department of Electronic and Telecommunication Engineering
Cumulative GPA **3.84 / 4.0** — 🏅 Dean's List (Semesters 1 & 3)

**G.C.E. Advanced Level 2022 (Physical Science)** — Ranked **190th** in the country · Z-score 2.5353

---

## 📚 Certifications

**DeepLearning.AI / Coursera** — Instructor: Andrew Ng · 2026

| Course | Implemented |
|---|---|
| **Convolutional Neural Networks** | ResNet from scratch · MobileNetV2 transfer learning · YOLO real-time detection · U-Net semantic segmentation · Neural style transfer (VGG-19) |
| **Advanced Learning Algorithms** | TensorFlow neural network for multiclass digit classification · Decision trees via entropy & information gain |
| **Supervised ML: Regression & Classification** | Regularized logistic regression for quality-assurance prediction |

---

## 🏅 Achievements & Leadership

- 🥈 **Second Place** — All-Island Article Competition for Undergraduates, Green Building Council of Sri Lanka (World Environment Day 2024)
- 🎤 **Semi-Finalist** — Speech Olympiad 2025, Gavel Club, University of Moratuwa
- 📋 **Assistant Treasurer** — Gavel Club, University of Moratuwa (2026/27)
- ✏️ **Editorial Committee Lead** — Brainstorm 2026, IEEE EMBS SBC, University of Moratuwa
- 📰 **Sub-Editor** — Electronic Club, University of Moratuwa (2025/26)

> Writing and speaking are part of how I do research, not a side interest — an idea that can't be explained clearly hasn't been understood clearly.

---

## 🤝 Looking Ahead

I'm interested in research collaborations and internships in **computer vision, deep learning, embedded & edge AI, human–computer interaction, and autonomous systems** — particularly work where perception models have to run on real hardware and serve real users.

My longer-term goal is graduate study and a research career, contributing to work that makes intelligent systems genuinely useful in healthcare and accessibility.

Always glad to discuss a problem, a paper, or a project.

<div align="center">

[![Email](https://img.shields.io/badge/upaniayodhya@gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:upaniayodhya@gmail.com)
[![LinkedIn](https://img.shields.io/badge/Connect_on_LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/upani-gunathunga-biomedicaleng)

**Thanks for visiting — feel free to reach out! 👩‍💻**

</div>
