# 🌀 Free & Forced Vibration Experiments – REE 308  
A complete experimental investigation of the vibration behavior of a cantilever beam under free and forced excitation. Includes system modeling, measurements, Arduino data acquisition, transmissibility analysis, and comparison with theoretical predictions.

## 📌 Course  
**REE 308 – Vibrations Laboratory**  
University of Science and Technology in Zewail City  
Supervisor: **Eng. Mohamed Lotfi Eid Shaltoat**

## 👥 Team  
- Aya Abdelrahman Atya – SID: 202000247  
- **Phelopater Ramsis – SID: 202001171**  
- Alia Elhalawany – SID: 202000292  

---

## 📘 Project Overview  
This laboratory project examines how a **cantilever beam** responds to **free vibration** (initial disturbance) and **forced vibration** (base excitation using an electrodynamic shaker).  

The experiment uses:  
- A **TIRA Vib shaker**  
- Accelerometer + Arduino for data collection  
- Signal generator & amplifier  
- MATLAB for plotting and analysis  

The report focuses on:  
- Mathematical modeling of SDOF systems  
- Determining natural frequency, damping ratio, damping coefficient  
- Measuring real-time responses  
- Comparing experimental and theoretical results  
:contentReference[oaicite:0]{index=0}

---

## 🧪 Part 1 — Free Vibration Experiment

### **Experimental Setup**  
(Photos shown on **page 4**)  
The setup includes the shaker, accelerometer, Arduino, and laptop running MATLAB.  
The beam is displaced manually and released to vibrate freely.  
:contentReference[oaicite:1]{index=1}

### **Mathematical Model**  
The free vibration of a damped SDOF system is governed by:

\[
m\ddot{x} + c\dot{x} + kx = 0
\]

Solution under underdamped conditions:

\[
x(t) = e^{-\zeta\omega_n t} 
\left(C_1 \sin(\omega_d t) + C_2 \cos(\omega_d t)\right)
\]

Definitions (page 6–7):
- \( \zeta = \frac{c}{2\sqrt{km}} \)
- \( \omega_n = \sqrt{\frac{k}{m}} \)
- \( \omega_d = \omega_n\sqrt{1-\zeta^2} \)
:contentReference[oaicite:2]{index=2}

### **Beam Properties**  
From measurements on **pages 7–8**:
- Length: 29.5 cm  
- Width: 39 mm  
- Thickness: 1.5 mm  
- Density (avg steel): 7900 kg/m³  
- Equivalent mass: **0.0313 kg**  
- Stiffness: **256.36 N/m**  
:contentReference[oaicite:3]{index=3}

### **Extracted Experimental Parameters**  
Using measured peaks (page 9):
- Damping ratio: **ζ ≈ 0.0353**  
- Damped natural frequency: **ωd ≈ 55.1 Hz**  
- Natural frequency: **ωn ≈ 55.15 Hz**  
:contentReference[oaicite:4]{index=4}

### **Theoretical Values**  
Using stiffness & equivalent mass (page 11–12):
- \( \omega_n = 90.94 \, \text{Hz} \)
- \( \omega_d = 90.88 \, \text{Hz} \)
- Damping coefficient \( c = 0.199 \)
:contentReference[oaicite:5]{index=5}

### **Time Response Comparison**  
- Measured vs. theoretical graphs shown on **page 14**.  
- Experimental signal decays faster, showing higher effective damping.  
- Maximum acceleration is significantly lower experimentally.  
:contentReference[oaicite:6]{index=6}

### **Sources of Error** (page 15)
- Neglecting accelerometer mass  
- Extra vibrations from surroundings  
- Human-induced errors  
- Beam fixture imperfections  

---

## 🧪 Part 2 — Forced Vibration Experiment

### **Experimental Setup**  
Shown again on **pages 16–18**:
- Signal generator → amplifier → shaker  
- Accelerometer → Arduino → MATLAB  
- Ruler for precise dimensions  
:contentReference[oaicite:7]{index=7}

### **Mathematical Model**  
\[
m\ddot{z} + c\dot{z} + kz = m\ddot{y}
\]
Where \( z = x - y \).  

Forced-vibration steady-state solution:

\[
x(t) = Y \cdot \sqrt{ \frac{1 + (2\zeta r)^2 }{(1-r^2)^2 + (2\zeta r)^2} } \cdot \sin(\omega t - \psi)
\]

with frequency ratio \( r = \omega / \omega_n \).  
:contentReference[oaicite:8]{index=8}

### **Measured vs. Theoretical Amplitude–Frequency Curves**  
(Page 21)

- Experimental amplitudes trend agrees with theory.  
- Theoretical curve is smoother; experimental curve shows noise + irregularities.  
- Error at low frequency ≈ **0.4%**, increasing at high frequencies.  
:contentReference[oaicite:9]{index=9}

### **Sources of Error** (page 22)
- Environmental noise  
- Real system not perfectly SDOF  
- Readings fluctuating during measurement  
- No anchor sensor for reference  

---

## 📎 Conclusion  
The experiments demonstrate clear differences between **free** and **forced** vibrations in an SDOF cantilever beam.  

Key takeaways (page 23):
- Free vibration allowed extraction of damping and natural frequency.  
- Forced vibration showed amplitude sensitivity to frequency ratio & transmissibility.  
- Theoretical models predict ideal behavior, while experimental data contains practical imperfections.  
- Understanding these differences is essential for real-world vibration control and system design.  
:contentReference[oaicite:10]{index=10}

---

## 🗂️ Files in This Folder  
- **Report.pdf** — Full laboratory report (free + forced vibration)  
- **README.md** — This description  

