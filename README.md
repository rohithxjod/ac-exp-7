# FM-using-Python

Aim


To implement and analyze frequency modulation (FM) using Python's NumPy and Matplotlib libraries. 

Apparatus Required

1.	Software: Python with NumPy and Matplotlib libraries
2.	Hardware: Personal Computer
  
Theory

Frequency Modulation (FM) is a method of transmitting information over a carrier wave by varying its frequency in accordance with the amplitude of the input signal (message signal). The frequency of the carrier wave is varied according to the instantaneous amplitude of the message signal. The general form of an FM signal is:



Algorithm


1.	Initialize Parameters: Set the values for carrier frequency, message frequency, sampling frequency, and frequency deviation.
2.	Generate Time Axis: Create a time vector for the signal duration.
3.	Generate Message Signal: Define the message signal as a cosine wave.
4.	Compute the Integral of the Message Signal: Calculate the integral of the message signal over time.
5.	Generate FM Signal: Apply the FM modulation formula to obtain the modulated signal.
6.	Plot the Signals: Use Matplotlib to plot the message signal, carrier signal, and modulated signal.

## **Program**
```
import numpy as np    
import matplotlib.pyplot as plt    
Am=5.5    
fm=477   
Ac=11    
fc=4770   
fs=47700    
b=3.99    
t=np.arange(0,2/fm,1/fs)    
m = np.cos(2 * np.pi * fm * t)    
c=np.cos(2*np.pi*fc*t)    
s = np.cos(2 * np.pi * fc * t + b * np.cos(2 * np.pi * fm * t))    

plt.subplot(3,1,1)     
plt.plot(t, m)     

plt.subplot(3,1,2)    
plt.plot(t,c)     

plt.subplot(3,1,3)      
plt.plot(t,s)

```   

Output Waveform    
<img width="702" height="513" alt="Screenshot 2025-12-03 144036" src="https://github.com/user-attachments/assets/bbde8c85-b7ef-4cd3-a74c-224ff759f88d" />



Tabular Column

![WhatsApp Image 2025-12-03 at 14 39 00_e4a28d00](https://github.com/user-attachments/assets/8b56d313-b232-49fb-b751-cde80d971164)



Calculation

![WhatsApp Image 2025-12-03 at 14 39 11_e0c86325](https://github.com/user-attachments/assets/a4044fcb-62f2-4da6-85d6-feb01fb38843)



Result

The message signal, carrier signal, and frequency modulated (FM) signal will be displayed in separate plots. The modulated signal will show frequency variations corresponding to the amplitude of the message signal.


The message signal, carrier signal, and frequency modulated (FM) signal will be displayed in separate plots. The modulated signal will show frequency variations corresponding to the amplitude of the message signal.
