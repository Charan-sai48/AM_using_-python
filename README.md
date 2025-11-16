# AM_using_python
## Aim

To implement and analyze amplitude modulation (AM) using Python's NumPy and Matplotlib libraries.

## Apparatus Required

Software: Python with NumPy and Matplotlib libraries<BR>
Hardware: Personal Computer
## Theory

Modulation can be defined as the process by which the characteristics of carrier wave are varied in accordance with the modulating wave (signal). Modulation is performed in a transmitter by a circuit called a modulator. Need for modulation is as follows: • Avoid mixing of signals • Reduction in antenna height • long distance communication • Multiplexing • Improve the quality of reception • Ease of radiation. Amplitude Modulation is the process of changing the amplitude of a relatively high frequency carrier signal in proportion with the instantaneous value of the modulating signal. The output waveform contains all the frequencies that make up the AM signal and is used to transport the information through the system. Therefore the shape of the modulated wave is called the AM envelope. With no modulating signal the output waveform is simply the carrier signal. Coefficient of modulation is a term used to describe the amount of amplitude change present in an AM waveform. There are three degrees of modulation available based on value of modulation index.

Under modulation : m<1, Em < Ec Critical modulation: m-1, Em = Ec Over modulation: m>1, Em > Ec Note: Keep all the switch faults in off position

## Algorithm

Initialize Parameters: Set the values for carrier frequency, message frequency, sampling frequency, and frequency deviation.

Generate Time Axis: Create a time vector for the signal duration.

Generate Message Signal: Define the message signal as a cosine wave.

Compute the Integral of the Message Signal: Calculate the integral of the message signal over time.

Generate AM Signal: Apply the AM modulation formula to obtain the modulated signal.

Plot the Signals: Use Matplotlib to plot the message signal, carrier signal, and modulated signal.

## Program 
```
mport numpy as np
import matplotlib.pyplot as plt

Am = 5.6
Ac = 11.2
Fm = 487
Fc = 4870
Fs = 48700

t = np.arange(0, 2/Fm, 1/Fs)

m = Am * np.cos(2 * np.pi * Fm * t)

c = Ac * np.cos(2 * np.pi * Fc * t)

s = (Ac + m) * np.cos(2 * np.pi * Fc * t)

plt.figure(figsize=(12, 8))

plt.subplot(3, 1, 1)
plt.plot(t, m)
plt.subplot(3, 1, 2)
plt.plot(t, c)
plt.subplot(3, 1, 3)
plt.plot(t, s)
plt.tight_layout()
plt.show()
```

## Output

<img width="1265" height="838" alt="image" src="https://github.com/user-attachments/assets/a6f27f9b-4c8b-40d2-837d-7bf39a5f39eb" />

## Tabular Column

## Calculation

## Result
