# DSBSC


EX NO: 2	DSB-SC-AM MODULATOR AND DEMODULATOR

AIM:

To write a program to perform DSBSC modulation and demodulation using SCI LAB and study its spectral characteristics

EQUIPMENTS REQUIRED

•	Computer with i3 Processor
•	SCI LAB

Note: Keep all the switch faults in off position

Algorithm:

1.	Define Parameters:
•	Fs: Sampling frequency.
•	T: Duration of the signal.
•	Fc: Carrier frequency.
•	Fm: Frequency of the message signal.
•	Amplitude: Maximum amplitude of the message signal.
2.	Generate Signals:
•	Message Signal: A sinusoidal signal that will be modulated.
•	Carrier Signal: A high-frequency sinusoidal signal used for modulation.
3.	DSBSC Modulation:
•	Modulated Signal: Multiply the message signal by the carrier signal to produce the DSBSC signal.
4.	DSBSC Demodulation:
•	Multiplication: Multiply the modulated signal by the carrier signal to get the product of the message signal with itself (i.e., the original message signal plus high-frequency components).
•	Low-pass Filtering: Apply a Butterworth low-pass filter to remove the high- frequency components and recover the original message signal.
5.	Visualization:
Plot the message signal, carrier signal, DSBSC modulated signal, and the recovered signal after demodulation.
PROCEDURE

•	Refer Algorithms and write code for the experiment.
•	Open SCILAB in System
•	Type your code in New Editor
•	Save the file
 
•	Execute the code
•	If any Error, correct it in code and execute again
•	Verify the generated waveform using Tabulation and Model Waveform

Model Waveform

<img width="703" height="679" alt="image" src="https://github.com/user-attachments/assets/e7c7c7f8-ccf2-41ac-b1f3-325989941a6f" />

Program```clc;
clear;
close;

// Parameters
ac = 181;          // Carrier amplitude
Am = 18.1;        // Message amplitude
fc = 6460;       // Carrier frequency
fm = 646;        // Message frequency
fs = 45000;      // Sampling frequency

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
Output Graph
<img width="1919" height="1199" alt="Screenshot 2026-03-22 151421" src="https://github.com/user-attachments/assets/1c2b6406-e0d9-42c5-81b5-afcb519763bf" />


Tablular Column


Result

Thus the DSB-SC-AM Modulation and Demodulation is generated.

