RGCC-X⁺
Risk-Gated Contractive Control with Latent State Estimation
A Control-Theoretic Framework for Provably Bounded Hallucination Suppression in Large Language Models
Author: Alim ul Haq Khan
Independent Researcher – Cognitive Systems & Emotional AI
Founder, Aura-X Ω
UK Patent Application No. 2518804.6
📚 Version History
This repository contains the V1 implementation. Extended versions are available as open-access preprints:
Version
Title
DOI
Published
V1
RGCC-X⁺: Contractive Control for Hallucination Suppression (this repository)
Submitted to Springer Nature
2025
V2
RGCC-X⁺ V2: Recursive Geometric Contraction Control — A Lyapunov-Inspired Dynamic Stability Framework with Empirical Validation
�
Feb 25, 2026
Load image
V3
RGCC-X⁺ V3: Universal Cross-Model Adaptive Orchestration for Hallucination Mitigation with Bayesian Cost Calibration
�
Feb 26, 2026
Load image
What's new in each version
V2 adds:
Extended Kalman Filter (EKF) for nonlinear state tracking
Logistic regression-derived risk weights (ROC-AUC = 0.847)
Cost-Aware Adaptive Routing layer (Theorem 6) — average overhead 1.28×
Self-correction recovery module (Theorem 5)
Full empirical validation: 312-question benchmark, human annotation κ = 0.74
V3 adds:
Cross-model universality across 3 LLM families (Claude-3, GPT-4-class, Gemini-class)
Bayesian λ auto-calibration — converges to 1.19× average cost in ~120 turns
Conversation Graph stability detector for coordinated adversarial sequences
Extended benchmark: N = 624, 8 stress categories, three-way ANOVA
🌐 Live Demo
🔗 Interactive Web Simulation:
https://alimulhaqkhan-prog.github.io/rgcc-x-plus-control-framework/
📘 Overview
RGCC-X⁺ is a control-theoretic middleware framework that models hallucination in large language models (LLMs) as a stochastic dynamical state and applies:
Contractive feedback control
Kalman latent state estimation
Risk-gated adaptive contraction
Lyapunov stability certification
Information-theoretic lower bounds
The framework provides formal guarantees of bounded hallucination dynamics under stated assumptions, rather than relying purely on empirical mitigation.
🧠 Core Mathematical Model
Hallucination state evolution:
e_{t+1} = (1 - eta) * e_t + epsilon + xi_t
where:
eta ∈ (0,1] → contraction strength
epsilon → entropy-imposed irreducible floor
xi_t → stochastic disturbance
Steady state:
e* = epsilon / eta
Epistemic Reliability Equation:
e* = c * H(Y|X) / eta
📐 Theoretical Guarantees (V1 — 5 Theorems)
Uniform Ultimate Boundedness
Drift Suppression
Switching Stability
Adversarial Damping
Entropy-Imposed Lower Bound
V2 extends to 6 theorems; V3 to 9 theorems. See preprints above.
🔬 Synthetic Validation (V1)
Monte Carlo simulation — 300 steps, 50 seeds:
Condition
Steady-State
Variance @ t=300
Uncontrolled
No convergence
0.120
Static (eta=0.4)
0.050
0.00063
Adaptive RGCC-X⁺
0.038
0.00048
All results match theoretical predictions within < 5% error.
📊 Preliminary Empirical Evidence — TruthfulQA Subset (V1)
Method
Hallucination Rate
Latency
Baseline
28%
1.0×
Static contraction
21%
1.8×
Adaptive RGCC-X⁺
16%
1.4×
For full empirical validation (N=312, human-annotated), see V2 preprint.
🏗 Architecture
Pipeline stages:
Generation
Risk Computation
Kalman State Estimation
Adaptive Contraction
Escalation (if needed)
Stabilized Output
📂 Repository Structure
rgcc-x-plus-control-framework/
│
├── index.html          # Web simulation demo
├── /experiments        # Synthetic experiments
├── /rgcc               # Core control logic (planned)
└── README.md
🚀 Running the Simulation
Web Demo — open the live demo above or run locally:
Open index.html in your browser
Python (if added later):
pip install -r requirements.txt
python experiments/synthetic_validation.py
📖 Manuscript
V1 — Full manuscript submitted to Discover Artificial Intelligence (Springer Nature)
V2 Preprint: https://doi.org/10.5281/zenodo.18770256
V3 Preprint: https://doi.org/10.5281/zenodo.18780684
📜 Citation
V1:
@article{khan2025rgcc,
  title     = {RGCC-X+: Risk-Gated Contractive Control with Latent State Estimation},
  author    = {Khan, Alim ul Haq},
  year      = {2025}
}
V2:
@misc{khan2026rgccv2,
  title     = {RGCC-X+ V2: Recursive Geometric Contraction Control for Large Language Model Hallucination Mitigation},
  author    = {Khan, Alim ul Haq},
  year      = {2026},
  doi       = {10.5281/zenodo.18770256},
  url       = {https://doi.org/10.5281/zenodo.18770256}
}
V3:
@misc{khan2026rgccv3,
  title     = {RGCC-X+ V3: Universal Cross-Model Adaptive Orchestration for Hallucination Mitigation},
  author    = {Khan, Alim ul Haq},
  year      = {2026},
  doi       = {10.5281/zenodo.18780684},
  url       = {https://doi.org/10.5281/zenodo.18780684}
}
⚠ Limitations (V1)
Controls stochastic error, not systematic bias
Linear-Gaussian assumption
Scalar state abstraction
Preliminary empirical scope (addressed in V2 and V3)
🧭 Research Direction
RGCC-X⁺ contributes toward Epistemic Stability Engineering —
the design of provably bounded cognitive systems.
📄 License
© 2026 Alim ul Haq Khan. UK Patent Application No. 2518804.6.
V1 code: open for academic use.
V2/V3 frameworks: see individual preprint licenses.
📬 Contact
alimulhaqkhan@gmail.com
Timergara, Lower Dir, Khyber Pakhtunkhwa, Pakistan
ORCID: 0009-0001-4708-0365