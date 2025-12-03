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
<img width="676" height="514" alt="image" src="https://github.com/user-attachments/assets/18809402-3e13-47ff-99d3-7887b7895675" />


Tabular Column

![WhatsApp Image 2025-11-29 at 08 24 28_19479784](https://github.com/user-attachments/assets/ca370fdb-2c1a-4505-80a8-02f1f76eae80)


Calculation

![WhatsApp Image 2025-11-29 at 08 42 15_7cb6ea13](https://github.com/user-attachments/assets/27710524-dbe5-4970-ad13-0c56947e9739)



Result

The message signal, carrier signal, and frequency modulated (FM) signal will be displayed in separate plots. The modulated signal will show frequency variations corresponding to the amplitude of the message signal.


The message signal, carrier signal, and frequency modulated (FM) signal will be displayed in separate plots. The modulated signal will show frequency variations corresponding to the amplitude of the message signal.
