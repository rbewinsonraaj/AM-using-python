# AM-using-python
## Aim
To implement and analyze amplitude modulation (AM) using Python's NumPy and Matplotlib libraries.

## Apparatus Required
Software: Python with NumPy and Matplotlib libraries
Hardware: Personal Computer

## Theory
Amplitude Modulation (AM) is a technique used in electronic communication, primarily for transmitting information via a radio carrier wave. The general form of an FM signal is:
## Algorithm
1. Initialize Parameters: Set the values for carrier frequency, message frequency, sampling frequency, and frequency deviation.
2. Generate Time Axis: Create a time vector for the signal duration.
3. Generate Message Signal: Define the message signal as a cosine wave.
4. Compute the Integral of the Message Signal: Calculate the integral of the message signal over time.
5. Generate AM Signal: Apply the AM modulation formula to obtain the modulated signal.
6. Plot the Signals: Use Matplotlib to plot the message signal, carrier signal, and modulated signal.

## program
```
import numpy as np
import matplotlib.pyplot as plt

Am=7.5
fm=677
Ac=15.0
fc=6770
fs=67700
t=np.arange(0,2/fm,1/fs)
m=Am*np.cos(2*np.pi*fm*t)
plt.subplot(3,1,1)
plt.plot(t,m)
c=Ac*np.cos(2*np.pi*fc*t)
plt.subplot(3,1,2)
plt.plot(t,c)
s=(Ac+m)*np.cos(2*np.pi*fc*t)
plt.subplot(3,1,3)
plt.plot(t,s)
plt.show()
```
## output waveform
<img width="807" height="603" alt="image" src="https://github.com/user-attachments/assets/3326ec29-18c9-4f2a-b9a3-aa85bbf11d03" />


## Tabular Column
![WhatsApp Image 2025-11-28 at 22 02 39_61db680c](https://github.com/user-attachments/assets/f5e0b34c-f8d7-4534-937a-364c5197bc60)


## Result
The message signal, carrier signal, and amplitude modulated (AM) signal will be displayed in separate plots. The modulated signal will show amplitude variations corresponding to the amplitude of the message signal.
