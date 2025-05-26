# Aim
To generte Frequency modulated wave for given specification
# Tools Required
Python or MATLAB
# Procedure
1. Initialize the amplitude and frequency of carrier wave
2. Initialize the amplitude and frequency of Message signal
3. Initialize the frequency deviation delta.
4. Initialize the time duration
5. Plot the FM wave

# Code
```
import numpy as np
import matplotlib.pyplot as plt

A_c = 1
f_c = 100
f_m = 10
delta_f = 50
T = 1
fs = 1000

t = np.linspace(0, T, int(fs * T), endpoint=False)

m_t = np.sin(2 * np.pi * f_m * t)

s_t = A_c * np.cos(2 * np.pi * f_c * t + delta_f * m_t)

plt.figure(figsize=(10, 6))

plt.subplot(2, 1, 1)
plt.plot(t, m_t)
plt.title("Message Signal (m(t))")
plt.xlabel("Time [s]")
plt.ylabel("Amplitude")

plt.subplot(2, 1, 2)
plt.plot(t, s_t)
plt.title("FM Modulated Signal (s(t))")
plt.xlabel("Time [s]")
plt.ylabel("Amplitude")

plt.tight_layout()
plt.show()
```
# Waveform
![image](https://github.com/user-attachments/assets/f3078548-9eb5-420b-b6c8-121425284031)

# Result
Sucessfully generated Frequency modulated wave for given specification
