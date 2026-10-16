### Sample
- 193 languages with a New Testament; 54 families; market data for 68 (SCCS core: 39), child-value data for 30, high-god data for 120.

### Trade-off (replication of Koplenig et al.)
- h_char vs L_char: ρ_none = -0.79, ρ_both = -0.67 (p = 2.49e-26), n = 192
- h_word vs L_word: ρ_none = -0.83, ρ_both = -0.79 (p = 7.6e-43), n = 192
- h_bpe vs L_char: ρ_none = -0.80, ρ_both = -0.69 (p = 3.78e-28), n = 192

### Q1: complexity (h) and efficiency (L) vs markets and morality
- market_sccs → h_char: β_FMA = -0.04 (p = 0.672, q = 0.78); ρ_both = +0.36 (p = 0.026); n = 39
- market_sccs → h_word: β_FMA = +0.40 (p = 0.028, q = 0.14); ρ_both = +0.20 (p = 0.213); n = 39
- market_sccs → h_bpe: β_FMA = +0.02 (p = 0.826, q = 0.88); ρ_both = +0.35 (p = 0.028); n = 39
- market_sccs → L_char: β_FMA = -0.12 (p = 0.271, q = 0.39); ρ_both = -0.06 (p = 0.729); n = 39
- market_sccs → L_word: β_FMA = -0.35 (p = 0.051, q = 0.15); ρ_both = -0.31 (p = 0.051); n = 39
- market_sccs → K_char: β_FMA = -0.20 (p = 0.253, q = 0.38); ρ_both = -0.19 (p = 0.257); n = 39
- market_any → h_char: β_FMA = -0.00 (p = 0.944, q = 0.94); ρ_both = -0.06 (p = 0.630); n = 68
- market_any → h_word: β_FMA = +0.25 (p = 0.035, q = 0.15); ρ_both = +0.24 (p = 0.049); n = 68
- market_any → h_bpe: β_FMA = +0.02 (p = 0.649, q = 0.78); ρ_both = +0.03 (p = 0.840); n = 68
- market_any → L_char: β_FMA = -0.09 (p = 0.393, q = 0.54); ρ_both = -0.15 (p = 0.224); n = 68
- market_any → L_word: β_FMA = -0.18 (p = 0.134, q = 0.27); ρ_both = -0.26 (p = 0.033); n = 68
- market_any → K_char: β_FMA = -0.17 (p = 0.236, q = 0.38); ρ_both = -0.14 (p = 0.258); n = 68
- moral_values → h_char: β_FMA = +0.04 (p = 0.471, q = 0.61); ρ_both = +0.26 (p = 0.162); n = 30
- moral_values → h_word: β_FMA = -0.26 (p = 0.170, q = 0.31); ρ_both = -0.24 (p = 0.198); n = 30
- moral_values → h_bpe: β_FMA = +0.11 (p = 0.192, q = 0.33); ρ_both = +0.31 (p = 0.100); n = 30
- moral_values → L_char: β_FMA = +0.15 (p = 0.254, q = 0.38); ρ_both = -0.01 (p = 0.966); n = 30
- moral_values → L_word: β_FMA = +0.33 (p = 0.064, q = 0.18); ρ_both = +0.32 (p = 0.087); n = 30
- moral_values → K_char: β_FMA = +0.10 (p = 0.664, q = 0.78); ρ_both = +0.27 (p = 0.145); n = 30
- universalism_proxy → h_char: β_FMA = -0.05 (p = 0.430, q = 0.57); ρ_both = +0.21 (p = 0.308); n = 26
- universalism_proxy → h_word: β_FMA = -0.46 (p = 0.004, q = 0.03); ρ_both = -0.47 (p = 0.015); n = 26 **(q<.05)**
- universalism_proxy → h_bpe: β_FMA = +0.01 (p = 0.904, q = 0.93); ρ_both = +0.19 (p = 0.357); n = 26
- universalism_proxy → L_char: β_FMA = +0.20 (p = 0.001, q = 0.01); ρ_both = +0.27 (p = 0.180); n = 26 **(q<.05)**
- universalism_proxy → L_word: β_FMA = +0.52 (p = 0.001, q = 0.01); ρ_both = +0.56 (p = 0.003); n = 26 **(q<.05)**
- universalism_proxy → K_char: β_FMA = +0.05 (p = 0.150, q = 0.28); ρ_both = +0.49 (p = 0.011); n = 26
- obedience → h_char: β_FMA = +0.02 (p = 0.833, q = 0.88); ρ_both = +0.34 (p = 0.046); n = 34
- obedience → h_word: β_FMA = +0.27 (p = 0.077, q = 0.19); ρ_both = +0.23 (p = 0.200); n = 34
- obedience → h_bpe: β_FMA = +0.11 (p = 0.125, q = 0.26); ρ_both = +0.35 (p = 0.039); n = 34
- obedience → L_char: β_FMA = -0.25 (p = 0.043, q = 0.15); ρ_both = -0.29 (p = 0.100); n = 34
- obedience → L_word: β_FMA = -0.30 (p = 0.085, q = 0.19); ρ_both = -0.41 (p = 0.015); n = 34
- obedience → K_char: β_FMA = -0.38 (p = 0.023, q = 0.14); ρ_both = -0.43 (p = 0.011); n = 34
- moralizing_god → h_char: β_FMA = -0.09 (p = 0.081, q = 0.19); ρ_both = -0.11 (p = 0.239); n = 119
- moralizing_god → h_word: β_FMA = +0.48 (p = 0.000, q = 0.00); ρ_both = +0.46 (p = 0.000); n = 119 **(q<.05)**
- moralizing_god → h_bpe: β_FMA = -0.13 (p = 0.043, q = 0.15); ρ_both = -0.22 (p = 0.019); n = 119
- moralizing_god → L_char: β_FMA = -0.03 (p = 0.712, q = 0.80); ρ_both = -0.03 (p = 0.756); n = 119
- moralizing_god → L_word: β_FMA = -0.44 (p = 0.000, q = 0.00); ρ_both = -0.37 (p = 0.000); n = 119 **(q<.05)**
- moralizing_god → K_char: β_FMA = -0.20 (p = 0.046, q = 0.15); ρ_both = -0.20 (p = 0.026); n = 119

### Q2: moral vs matched non-moral verses (positive Δh = moral phrases more complex; positive ΔL = more characters)
- emfd_high: mean Δh = +0.0093 (multilevel p = 0.566, 59% of languages > 0); mean ΔL = +0.0739 (p = 0.00231); corr(Δh, ΔL) = -0.83
- emotions: mean Δh = -0.0110 (multilevel p = 0.0138, 40% of languages > 0); mean ΔL = +0.0896 (p = 1.66e-10); corr(Δh, ΔL) = -0.78
- moral_any: mean Δh = +0.0007 (multilevel p = 0.821, 51% of languages > 0); mean ΔL = +0.0773 (p = 3.74e-13); corr(Δh, ΔL) = -0.82
- particularism: mean Δh = -0.0026 (multilevel p = 0.693, 45% of languages > 0); mean ΔL = +0.0180 (p = 0.0147); corr(Δh, ΔL) = -0.51
- prosocial: mean Δh = +0.0490 (multilevel p = 0.000178, 96% of languages > 0); mean ΔL = +0.0357 (p = 0.112); corr(Δh, ΔL) = -0.47
- trust: mean Δh = -0.0204 (multilevel p = 0.000151, 17% of languages > 0); mean ΔL = +0.0369 (p = 5.25e-05); corr(Δh, ΔL) = -0.67
- universalism: mean Δh = +0.0188 (multilevel p = 0.102, 80% of languages > 0); mean ΔL = +0.0501 (p = 1.48e-05); corr(Δh, ΔL) = -0.65

### Q2: relation of Δh / ΔL to markets and morality (all moral verses)
- market_sccs → dh: β_FMA = +0.32 (p = 0.023, q = 0.12); ρ_both = +0.22 (p = 0.172); n = 39
- market_sccs → dL: β_FMA = -0.11 (p = 0.461, q = 0.72); ρ_both = +0.02 (p = 0.890); n = 39
- market_any → dh: β_FMA = +0.29 (p = 0.006, q = 0.05); ρ_both = +0.30 (p = 0.013); n = 68
- market_any → dL: β_FMA = -0.14 (p = 0.239, q = 0.48); ρ_both = -0.12 (p = 0.339); n = 68
- moral_values → dh: β_FMA = -0.26 (p = 0.053, q = 0.17); ρ_both = -0.29 (p = 0.116); n = 30
- moral_values → dL: β_FMA = +0.05 (p = 0.672, q = 0.87); ρ_both = +0.04 (p = 0.845); n = 30
- universalism_proxy → dh: β_FMA = -0.41 (p = 0.000, q = 0.00); ρ_both = -0.56 (p = 0.003); n = 26 **(q<.05)**
- universalism_proxy → dL: β_FMA = +0.12 (p = 0.348, q = 0.61); ρ_both = +0.07 (p = 0.731); n = 26
- obedience → dh: β_FMA = +0.27 (p = 0.231, q = 0.48); ρ_both = +0.31 (p = 0.078); n = 34
- obedience → dL: β_FMA = -0.09 (p = 0.509, q = 0.74); ρ_both = -0.09 (p = 0.613); n = 34
- moralizing_god → dh: β_FMA = +0.14 (p = 0.054, q = 0.17); ρ_both = +0.20 (p = 0.029); n = 119
- moralizing_god → dL: β_FMA = -0.00 (p = 0.973, q = 0.99); ρ_both = -0.04 (p = 0.693); n = 119