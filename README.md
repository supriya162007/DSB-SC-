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

Program
```
ac = 16.0;
Am = 8.0;
fc = 4600;
fm = 460;
fs = 200000;

t = 0:1/fs:2/fm;
wc = 2*3.14*fc;
wm = 2*3.14*fm;

e1 = Am * sin(wm * t);
subplot(3,1,1);
plot(t, e1);
title("Modulating Signal");
xgrid;
e2 = ac * sin(wc * t);
subplot(3,1,2);
plot(t, e2);
title("Carrier Signal");
xgrid;

e3 = (Am/2 .* cos(wc*t - wm*t)) - (Am/2 .* cos(wc*t + wm*t));
subplot(3,1,3);
plot(t, e3);
title("Double Side Band Suppressed Carrier (DSB-SC)");
xgrid;
```

Output Graph
![WhatsApp Image 2025-11-11 at 10 41 26_80667bfe](https://github.com/user-attachments/assets/c73f2507-9844-4bf9-a1e4-70202c32712f)

Tablular Column
![WhatsApp Image 2025-11-24 at 11 02 48_059871aa](https://github.com/user-attachments/assets/94934233-70be-4a1c-b519-e40858ae0a82)


Result

Thus the DSB-SC-AM Modulation and Demodulation is generated.

