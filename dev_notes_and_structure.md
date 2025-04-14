```markdown
# Fractal7 x Sapolsky — Technical Overview

This document outlines the structure, methods, configuration, and requirements of the Fractal7 x Sapolsky system. It is intended for advanced users familiar with fractal analysis, signal processing, or quantitative systems.

---

## Project Structure

```
fractal_analysis/
│
├── core/
│   ├── box_counting.py              # Fractal dimension (box-counting)
│   ├── hurst_exponent.py           # Hurst exponent estimation
│   ├── dfa.py                      # Detrended fluctuation analysis
│   ├── power_law_scaling.py        # Power spectrum analysis
│   ├── wtmm.py                     # Wavelet transform modulus maxima
│   └── multifractal_spectrum.py    # Singularity spectrum f(α)
│
├── main.py                         # Unified pipeline
└── __init__.py
```

---

## Implemented Methods

1. **Box-Counting Algorithm**
   - Log–log fit of occupied boxes vs scale → fractal dimension \( D \)

2. **Hurst Exponent (R/S Analysis)**
   - Log–log fit of rescaled range over window size → \( H \)

3. **Detrended Fluctuation Analysis (DFA)**
   - Root-mean-square fluctuation of integrated detrended signal → α ≈ H

4. **Power-Law Scaling**
   - FFT-based log–log slope of power spectral density → β

5. **WTMM**
   - Continuous wavelet transform with modulus maxima detection → local scaling

6. **Multifractal Spectrum**
   - Computation of \( τ(q), α(q), f(α) \) via partition functions

7. **Regime Classification**
   - Threshold logic based on H, D, β, f(α) width

---

## Configuration (`settings.yaml`)

```yaml
wavelet: mexh
scales: [1, 2, 4, 8, 16, 32, 64]
hurst_range: [2, 100]
dfa_scales: [10, 20, 30, 40, 50]
```

---

## Requirements (`requirements.txt`)

```txt
numpy
scipy
pywavelets
matplotlib
pandas
```

Optional:
```txt
cupy
torch
```

---

## About the Author

Independent developer and researcher. Self-taught. Focused on the intersection of neural patterns, signal complexity, and algorithmic modeling. The system was created to test whether cognitive-like structures and dynamics can be formalized and executed through code without institutional support.

```
