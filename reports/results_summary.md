EMG Signal Detective — Results Summary


1. Project Overview

This project explores surface electromyography (sEMG) signals using Python and a real-world dataset from PhysioNet.

The analysis focuses on a 2-second recording of the left tibialis anterior muscle during walking. The objective was to examine the signal's amplitude and frequency characteristics, investigate potential sources of noise, and explore the effects of applying a moving average filter.

The project combines signal visualization, numerical analysis, and basic signal processing to better understand how EMG recordings can be analyzed and interpreted.


2. Dataset and Methodology

Dataset

The analysis uses the Surface Electromyographic Signals During Walking dataset from PhysioNet.

The selected recording was S01, using the channel semg LT TIB.A, corresponding to the left tibialis anterior muscle.

The first 2 seconds of the recording were analyzed, containing 4,000 samples collected at a sampling rate of 2,000 Hz. Signal amplitudes are expressed in microvolts (μV).

Methodology

The analysis was conducted using Python, with NumPy for numerical calculations, Matplotlib for visualization, and WFDB for accessing the dataset.

The following techniques were applied:

Signal visualization: Examining the waveform over time and identifying its largest positive peak.

Amplitude analysis: Calculating Mean Absolute Value (MAV) and Root Mean Square (RMS).

Frequency analysis: Applying the Fast Fourier Transform (FFT) to examine the signal's frequency components.

Signal processing: Applying a 10-sample moving average filter (5 ms window) to smooth the waveform.

The original and processed signals were then compared using their amplitude measurements, waveforms, and frequency spectra.


3. Key Findings

Amplitude Measurements

**Original signal:**
- MAV: 2.9799 μV
- RMS: 3.8392 μV

**Smoothed signal:**
- MAV: 2.0496 μV
- RMS: 2.4841 μV

Following moving average filtering:
- MAV decreased by approximately 31.2%.
- RMS decreased by approximately 35.3%.

Frequency Analysis

The original frequency spectrum showed a prominent component around 100 Hz, alongside smaller components across the analyzed frequency range.

After applying the moving average, frequency components were attenuated across much of the spectrum. The prominent component around 100 Hz remained visible but was reduced.

Overall Observations

The moving average filter produced a smoother waveform and reduced both amplitude measurements and frequency magnitudes. These results demonstrate that signal processing can significantly alter the characteristics of an EMG recording.



## 4. Interpretation

The analysis demonstrates how different techniques can be used to examine surface EMG signals.

The decrease in MAV and RMS following moving average filtering indicates that smoothing reduced the overall amplitude of the selected signal.

The frequency comparison also showed attenuation across much of the analyzed frequency range. This suggests that the moving average acts as a low-pass filter, reducing higher-frequency components while preserving some lower-frequency content.

However, these changes do not necessarily indicate that unwanted noise was removed. Some attenuated components may contain meaningful muscle activity.

Overall, the results highlight the importance of understanding how signal processing affects both the amplitude and frequency characteristics of EMG recordings before interpreting the processed signal.



## 5. Limitations

Several limitations should be considered when interpreting the results:

- **Short recording:** The analysis focused on only 2 seconds of one muscle channel, so findings may not represent the entire recording or other subjects.
- **Pre-filtered data:** The original EMG signal was already hardware-filtered during data acquisition.
- **Filter limitations:** The moving average can reduce meaningful muscle activity along with unwanted fluctuations.
- **Window size:** The results depend on the selected 10-sample window. Different window sizes may produce different results.
- **Unconfirmed noise sources:** Potential sources of interference, such as power-line interference and movement artifacts, were considered but not individually verified.

The analysis therefore demonstrates the effects of basic signal processing but does not establish that noise was successfully removed or that the processed signal is more accurate.



## 6. Conclusion

This project provided an introduction to surface EMG signal analysis using Python, combining signal visualization, amplitude measurements, frequency analysis, and basic signal processing.

The moving average filter demonstrated how processing can reduce signal fluctuations while also altering meaningful signal characteristics.

Overall, the investigation highlighted the importance of understanding a signal before processing it and carefully interpreting the effects of any modifications.
