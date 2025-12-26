# Mono-Channel Speech Enhancement

A project focused on extracting clean speech from noisy single-channel recordings. This is an ongoing exploration into Digital Signal Processing (DSP) fundamentals, specifically for real-time edge applications.

## Why this project?
I started this to understand how we can isolate signals in the frequency domain. While many AI models exist for this now, I wanted to implement the "Spectral Subtraction" method from scratch to learn how the Short-Time Fourier Transform (STFT) actually manipulates audio buffers.

## The Approach (Work in Progress)
The current implementation follows the standard DSP pipeline:
1. **Windowing:** Dividing the signal into 20ms overlapping frames (Hamming window) to keep the signal stationary.
2. **FFT:** Converting time-domain samples into frequency bins.
3. **Noise Estimation:** Measuring the 'noise floor' during silent periods of the audio.
4. **Subtraction:** Subtracting the noise magnitude from the total signal magnitude.
5. **Phase Reconstruction:** Combining the original phase with the new magnitude to keep the voice sounding natural.

## Current Status
- [x] Audio file loading and STFT conversion.
- [x] Basic Spectral Subtraction script.
- [ ] Optimization to reduce "Musical Noise" (artifacting).
- [ ] Real-time processing implementation.

## Tech Used
* Python (Librosa, NumPy, SciPy)
* Signal Processing Math (Fourier Analysis)
