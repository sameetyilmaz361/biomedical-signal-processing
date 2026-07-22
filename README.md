# biomedical-signal-processing
FFT-based signal filtering — synthetic signals and real ECG data (MIT-BIH)
# Biomedical Signal Processing

Frequency-domain signal processing examples in Python — FFT-based spectral analysis and powerline noise (60 Hz) filtering, explored on synthetic signals and then applied to a real ECG recording from the MIT-BIH Arrhythmia Database (via PhysioNet/Kaggle).

The approach is the same throughout: transform the signal into the frequency domain (FFT), identify and remove the target noise frequency, then transform back (inverse FFT) to get the cleaned signal. The same technique applies directly to EMG and EEG signals as well.

## Files

- `frequency_spectrum.py` — spectral analysis on a synthetic signal
- `signal_filtering.py` — noise filtering on a synthetic signal
- `ecg_signal_filtering.py` — the same filtering technique applied to real ECG data (`100_SIG_II.npy`, MIT-BIH record 100, Lead II, 360 Hz sampling rate)

## Tech stack

Python, NumPy, SciPy (`scipy.fftpack`), Matplotlib

## Usage

```bash
pip install numpy scipy matplotlib
python frequency_spectrum.py
python signal_filtering.py
python ecg_signal_filtering.py
```

The ECG script requires `100_SIG_II.npy` to be in the same folder — [download from Kaggle](https://www.kaggle.com/datasets/nelsonsharma/ecg-lead-2-dataset-physionet-open-access).
