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

Program
```
import numpy as np
import matplotlib.pyplot as plt
Am = 6.3
fm = 504
Ac = 12.6
fc = 5040
fs = 504000
t = np.arange(0, 3/fm, 1/fs)
m = Am * np.cos(2 * np.pi * fm * t)
plt.subplot(3, 1, 1)
plt.plot(t, m)
c = Ac * np.cos(2 * np.pi * fc * t)
plt.subplot(3, 1, 2)
plt.plot(t, c)
efm = Ac * np.cos((2 * np.pi * fc * t) + 5.1 * np.sin(2 * np.pi * fm * t))
plt.subplot(3, 1, 3)
plt.plot(t, efm)
plt.tight_layout()
plt.show()
```

Output Waveform
<img width="943" height="701" alt="image" src="https://github.com/user-attachments/assets/d9b3e2f9-caab-4e53-8447-927b5fd77e3a" />


Tabular Column

![WhatsApp Image 2025-11-28 at 9 04 32 PM](https://github.com/user-attachments/assets/a73f62fa-2f29-405f-b241-c7e846d86f55)


Calculation
<img width="704" height="1280" alt="image" src="https://github.com/user-attachments/assets/b04eedc2-1235-47a2-a3e5-b2138b7bf940" />




Result


The message signal, carrier signal, and frequency modulated (FM) signal will be displayed in separate plots. The modulated signal will show frequency variations corresponding to the amplitude of the message signal.
