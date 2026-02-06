## Nyquist theorem
Is the theorem that is states that a signal can be fully reconstructed if it is sampled with at least twice the highest frequency component. The idea is that sampling with at least twice the speed allows for two point to be sampled in on period of the signal. This frequency is known as the Nyquist frequency ($\frac{F_{s}}{2}$). Which makes the signal somewhat reproducible from those two points. As you increase the sampling rate to be more than twice the highest frequency component the accuracy of the reconstruction of the signal becomes better.


## aliasing
To understand aliasing we first have to be able to understand [[Fan Folding]]
## Anti-aliasing filter
Aliasing is when frequencies that are more than the Nyquist frequency  are being sampled. This is typically an undesirable effect so a anti-aliasing filter is used before entering the ADC to remove these frequencies so they don't get sampled. This is typically achieved with a low pass filter.

https://www.analog.com/en/resources/technical-articles/guide-to-antialiasing-filter-basics.html