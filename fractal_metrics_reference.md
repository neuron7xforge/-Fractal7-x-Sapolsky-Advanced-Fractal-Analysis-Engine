## 1. Fractal Dimension (Box-Counting)

D = lim (ε → 0) [ log(N(ε)) / log(1/ε) ]

## 2. Hurst Exponent (Rescaled Range Analysis)

E(R/S)_t = c · t^H  
log(E(R/S)_t) = log c + H · log t

## 3. Detrended Fluctuation Analysis (DFA)

Y(k) = ∑_{i=1}^{k} [ x(i) - ⟨x⟩ ]  
F(n) = sqrt( (1/N) ∑_{k=1}^{N} [ Y(k) - Y_n(k) ]² )  
F(n) ∼ n^α

## 4. Power-Law Scaling

S(f) ∝ f^(-β)  
β = 2H - 1

## 5. Wavelet Transform Modulus Maxima (WTMM)

W_ψ(a, b) = (1/√a) ∫ x(t) · ψ((t - b)/a) dt

## 6. Multifractal Formalism

μ_i(q) = p_i^q / ∑_j p_j^q  
Z(q, a) = ∑ p_i^q ∼ a^τ(q)  
τ(q) = qH(q) - 1  
f(α) = αq - τ(q)  
α = dτ(q)/dq

## 7. Interpretation Thresholds

H = 0.5 → random  
H > 0.5 → persistent  
H < 0.5 → anti-persistent  
D ∈ (1, 2)  
β ≈ 1 → 1/f noise  
width f(α) → degree of multifractality
