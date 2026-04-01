# DSBSC

EX NO: 2    DSB-SC-AM MODULATOR AND DEMODULATOR

---

## AIM:
To write a program to perform DSBSC modulation and demodulation using SCILAB and study its spectral characteristics.

---

## EQUIPMENTS REQUIRED
- Computer with i3 Processor  
- SCI LAB  

---

Note: Keep all the switch faults in off position

---

## ALGORITHM:

1. Define Parameters:
   - Fs: Sampling frequency  
   - T: Duration of the signal  
   - Fc: Carrier frequency  
   - Fm: Frequency of the message signal  
   - Amplitude: Maximum amplitude of the message signal  

2. Generate Signals:
   - Message Signal: Sinusoidal signal  
   - Carrier Signal: High-frequency sinusoidal signal  

3. DSBSC Modulation:
   - Multiply message signal with carrier signal  

4. DSBSC Demodulation:
   - Multiply modulated signal with carrier  
   - Apply low-pass filter to recover message  

5. Visualization:
   Plot all signals  

---

## PROCEDURE
- Refer Algorithms and write code  
- Open SCILAB in System  
- Type code in New Editor  
- Save the file  
- Execute the code  
- If any error, correct and execute again  
- Verify waveform  

---

## MODEL WAVEFORM
<img width="703" height="679" src="https://github.com/user-attachments/assets/e7c7c7f8-ccf2-41ac-b1f3-325989941a6f" />

---

## PROGRAM
```scilab
clc;
clear;
close;

// Parameters
ac = 181;          // Carrier amplitude
Am = 18.1;         // Message amplitude
fc = 6460;         // Carrier frequency
fm = 646;          // Message frequency
fs = 45000;        // Sampling frequency

// Time axis
t = 0:1/fs:2/fm;

// Angular frequencies
wc = 2*%pi*fc;
wm = 2*%pi*fm;

// 1. Message Signal
m = Am * sin(wm*t);

// 2. Carrier Signal
c = ac * sin(wc*t);

// 3. DSB-SC Signal
dsb_sc = m .* sin(wc*t);

// 4. Conventional AM Signal
am = (ac + m) .* sin(wc*t);

// Plotting
subplot(4,1,1);
plot(t, m);
xtitle("Message Signal");
xgrid();

subplot(4,1,2);
plot(t, c);
xtitle("Carrier Signal");
xgrid();

subplot(4,1,3);
plot(t, dsb_sc);
xtitle("DSB-SC Signal");
xgrid();

subplot(4,1,4);
plot(t, am);
xtitle("Conventional AM Signal");
xgrid();
```

---

## OUTPUT GRAPH
<img width="1919" height="1199" src="https://github.com/user-attachments/assets/1c2b6406-e0d9-42c5-81b5-afcb519763bf" />

---

## TABULAR COLUMN
<img width="1280" height="975" src="https://github.com/user-attachments/assets/1ee17d2d-fd2a-4d32-b948-fb2115859b14" />

---

## RESULT
Thus the DSB-SC-AM Modulation and Demodulation is generated.
