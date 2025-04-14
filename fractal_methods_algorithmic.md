```
## 1. Box-Counting Algorithm

1. Define a set of scales ε = [ε₁, ε₂, ..., εₙ]  
2. For each ε:
   a. Divide the space into boxes of size ε  
   b. Count the number N(ε) of non-empty boxes  
3. Compute log(N(ε)) vs log(1/ε)  
4. Apply linear regression → slope = D

## 2. Hurst Exponent Estimation (R/S)

1. Split time series into non-overlapping windows  
2. For each window:
   a. Calculate mean ⟨x⟩ and cumulative deviation Y(k)  
   b. Calculate range R and standard deviation S  
   c. Compute R/S  
3. Average R/S over all windows of same size  
4. Fit log(R/S) vs log(window size) → slope = H

## 3. Detrended Fluctuation Analysis (DFA)

1. Integrate the time series: Y(k) = ∑ [x(i) - ⟨x⟩]  
2. Divide Y(k) into windows of size n  
3. In each window:
   a. Fit polynomial trend  
   b. Subtract trend to get residual  
   c. Compute RMS fluctuation  
4. Compute mean F(n) over all segments  
5. Fit log(F(n)) vs log(n) → slope = α

## 4. Power Spectral Density (Fourier Method)

1. Apply FFT to time series → X(f)  
2. Compute power spectrum: S(f) = |X(f)|²  
3. Plot log S(f) vs log f  
4. Fit linear region → slope = -β

## 5. WTMM (Wavelet Transform Modulus Maxima)

1. Choose wavelet ψ and scale set a  
2. For each scale:
   a. Compute continuous wavelet transform W_ψ(a, b)  
   b. Take modulus |W_ψ(a, b)|  
   c. Detect local maxima over b  
3. Plot log(maxima) vs log(scale)  
4. Fit → slope = singularity exponent

## 6. Multifractal Spectrum Estimation

1. Partition signal into segments of size a  
2. Compute measure p_i in each segment  
3. For range of q:
   a. Compute Z(q, a) = ∑ p_i^q  
   b. Estimate τ(q) = log Z(q, a) / log a  
4. Compute α = dτ/dq  
5. Compute f(α) = qα - τ(q)

## 7. Regime Classification

1. Calculate H, D, β, and f(α)  
2. Use thresholds:
   - H ≈ 0.5 → random  
   - H > 0.5 → persistent trend  
   - H < 0.5 → reversion  
   - β ≈ 1 → criticality  
   - Wide f(α) → multifractality  
3. Label signal state accordingly
```
