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

Am=9.3;

Fm=298;

Fs=29800;

Ac=18.6;

Fc=2980;

t=0:1/Fs:2/Fm;

em=Am*cos(2*3.14*Fm*t);

subplot(3,1,1);

plot(t,em);

ec=Ac*cos(2*3.14*Fc*t);

subplot(3,1,2);

plot(t,ec);

eAM1=Ac*(1+(em/Ac)).*cos(2*3.14*Fc*t);

eAM2=Ac*(-1+(em/Ac)).*cos(2*3.14*Fc*t);

dsbsc=eAM1+eAM2;

subplot(3,1,3);

plot(t,dsbsc);


Output Graph
<img width="1620" height="966" alt="image" src="https://github.com/user-attachments/assets/52742de4-f2dc-4191-af47-7cbd9815f20b" />


Tablular Column
![WhatsApp Image 2026-02-25 at 8 59 23 PM](https://github.com/user-attachments/assets/7c3d42fa-3826-4193-abe1-e431b62c67bb)


Result

Thus the DSB-SC-AM Modulation and Demodulation is generated.

