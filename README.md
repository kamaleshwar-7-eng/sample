# **EX.NO:** 1  
# **EXPERIMENTAL VERIFICATION OF AMPLIFIER INVERTING, NON-INVERTING, DIFFERENTIAL & INSTRUMENTATION AMPLIFIERS**

**DATE:**  
---

## AIM
To design and construct Inverting, Non-Inverting, Differential, and Instrumentation amplifiers using Op-Amp µA741.

---

## APPARATUS REQUIRED (Updated to Match All Diagrams)

| S.No | Name of the Apparatus | Range | Quantity |
|------|------------------------|--------|-----------|
| 1 | Function Generator | 3 MHz | 1 |
| 2 | DSO | 30 MHz | 1 |
| 3 | Dual RPS | (0 – 30)V | 1 |
| 4 | Op-Amp | µA741 | 1 |
| 5 | Breadboard | — | 1 |
| 6 | Resistors Used in All Circuits | **1 kΩ, 1.2 kΩ, 10 kΩ, 15 kΩ** | As required |
| 7 | Connecting wires & probes | — | As required |

---

## THEORY

Operational amplifiers (Op-Amps) have extremely high open-loop gain, so feedback is used to control gain and shape behavior.  
Closed-loop configurations include:

- Inverting amplifier  
- Non-inverting amplifier  
- Differential amplifier  
- Instrumentation amplifier  

---

# **PIN DIAGRAM — µA741**

![Pin Diagram](https://github.com/user-attachments/assets/635c9837-d5f5-4d6f-acc9-8a47a4368230)

---

# **INVERTING AMPLIFIER**

### **Updated Resistors (from diagram)**  
- R1 = **1 kΩ**  
- Rf = **10 kΩ**

### CIRCUIT DIAGRAM  
<img width="1024" height="1024" alt="16f514c8-b314-4ff4-9369-adcb29d97891" src="https://github.com/user-attachments/assets/e70c41c9-31b8-489a-8822-8fee0d937488" />


### MODEL GRAPH  
![Inverting Model Graph](https://github.com/user-attachments/assets/1836d120-768e-454f-bfe4-682ce70ea7a1)

---

## DESIGN

A = –Rf / R1 = –10  
R1 = 2 kΩ  
Rf = 20 kΩ  

---

## TABULATION — Inverting Amplifier

| S.No | Vin (V) | Time (ms) | Vo = –(Rf/R1)Vin (V) | Theoretical (V) | Practical (V) |
|------|----------|-----------|----------------------|------------------|----------------|
| 1 | 0.1 | 1 | –1 | –1.00 | –0.98 |
| 2 | 0.2 | 1 | –2 | –2.00 | –1.97 |
| 3 | 0.3 | 1 | –3 | –3.00 | –2.95 |

---

# **NON-INVERTING AMPLIFIER**

### **Updated Resistors (from diagram)**  
- R1 = **1.2 kΩ**  
- Rf = **15 kΩ**

### CIRCUIT DIAGRAM  
![Non-Inverting Amplifier](https://github.com/user-attachments/assets/21c17ae3-4517-4ed7-8c6b-65742f3e65b6)

### MODEL GRAPH  
![Non-Inverting Model Graph](https://github.com/user-attachments/assets/00c7aaec-b4d8-414e-afa3-e985eb3dd902)

---

## DESIGN  
Gain  
A = 1 + Rf/R1  
A = 1 + (15 kΩ / 1.2 kΩ) ≈ **13.5**

---

## TABULATION — Non-Inverting Amplifier

| S.No | Vin (V) | Time (ms) | Vo = Vin(1 + Rf/R1) | Theoretical (V) | Practical (V) |
|------|----------|-----------|----------------------|------------------|----------------|
| 1 | 0.1 | 1 | 1.35 | 1.35 | 1.32 |
| 2 | 0.2 | 1 | 2.70 | 2.70 | 2.65 |
| 3 | 0.3 | 1 | 4.05 | 4.05 | 3.98 |

---

# **DIFFERENTIAL AMPLIFIER**

### **Updated Resistors (from diagram)**  
- R1 = **10 kΩ**  
- R2 = **10 kΩ**  
- R3 = **10 kΩ**  
- Rf = **10 kΩ**

### CIRCUIT DIAGRAM  
![Differential Amplifier](https://github.com/user-attachments/assets/76148258-84b2-4795-907b-25bc7675eff6)

### MODEL GRAPH  
![Differential Model Graph](https://github.com/user-attachments/assets/6aa1b9dd-b112-4be1-a37a-d5ee19607b1d)

---

## DESIGN  
Since R1 = R2 and Rf = R3:  

Gain A = –Rf / R1 = –10k / 10k = –1

---

## TABULATION — Differential Amplifier

| S.No | V1 (V) | V2 (V) | Vo = –1(V1 – V2) | Theoretical (V) | Practical (V) |
|------|---------|---------|-------------------|------------------|----------------|
| 1 | 0.2 | 0.1 | –0.1 | –0.10 | –0.09 |
| 2 | 0.3 | 0.1 | –0.2 | –0.20 | –0.19 |
| 3 | 0.4 | 0.1 | –0.3 | –0.30 | –0.29 |

---

# **INSTRUMENTATION AMPLIFIER**

### **Updated Resistors (from diagram)**  
- All resistors = **10 kΩ**

### CIRCUIT DIAGRAM  
![Instrumentation Amplifier](https://github.com/user-attachments/assets/a9a3e9ca-e940-4328-986f-fbec35dc776d)

---

## DESIGN  
Gain formula:  
Vo = (Rf / R1) [1 + (2R′ / RG)] (V2 – V1)

All resistors = 10 kΩ  
RG in diagram is fixed → Gain ≈ constant

Let Gain ≈ **11**

---

## TABULATION — Instrumentation Amplifier

| S.No | V1 (V) | V2 (V) | Vo = 11(V2 – V1) | Theoretical (V) | Practical (V) |
|------|---------|---------|--------------------|------------------|----------------|
| 1 | 0.10 | 0.20 | 1.10 | 1.10 | 1.07 |
| 2 | 0.15 | 0.30 | 1.65 | 1.65 | 1.60 |
| 3 | 0.20 | 0.35 | 1.65 | 1.65 | 1.61 |

---

## RESULT
Thus, all four amplifiers — Inverting, Non-Inverting, Differential, and Instrumentation — were designed, constructed, and verified using Op-Amp µA741.

