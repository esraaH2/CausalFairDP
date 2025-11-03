# 🧠 CausalFairDP: Fair and Privacy-Preserving Synthetic Data Generation with Causal Structure Preservation using Diffusion Models

CausalFairDP is an advanced **Diffusion-based generative framework** that produces **fair**, **privacy-preserving**, and **causally consistent** synthetic tabular data.  
It integrates **Differential Privacy (DP)**, **Fairness-aware optimization**, and **Causal Structure Preservation**, providing a responsible solution for **ethical AI and data sharing**.

---

## 🚀 Overview

Real-world datasets often contain **bias** (e.g., gender, race) and can leak **sensitive information**.  
CausalFairDP mitigates these risks through a **multi-stage development pipeline** that progressively adds fairness, privacy, and causal consistency to diffusion-based generative models.

---

## 🧩 Architecture

CausalFairDP is based on an enhanced **U-Net Diffusion architecture** with:
- **Input dimension:** 14  
- **Hidden dimension:** 512  
- **Layers:** 6  
- **Diffusion steps:** 2000  
- **Scheduler:** Cosine Annealing  
- **Privacy:** Differential Privacy (ε=1.0, δ=1e-5)  
- **Fairness weight:** 1.5  
- **Frameworks:** PyTorch + Opacus + NumPy + Pandas  

---

## ⚙️ Key Features

| Feature | Description |
|----------|-------------|
| 🧠 **Diffusion Model** | Generates high-quality tabular data from Gaussian noise. |
| ⚖️ **Fairness Optimization** | Reduces bias across sensitive attributes (`sex`, `race`). |
| 🔐 **Differential Privacy** | Guarantees user-level privacy via noise injection (Opacus). |
| 🔗 **Causal Structure Preservation** | Maintains causal edges and dependencies between features. |
| 📊 **Evaluation Framework** | Measures KS, Wasserstein, SPD, and correlation metrics. |

---

## 🧪 Model Comparison

CausalFairDP evolved through **four progressive models**, each improving fairness, privacy, and causal consistency.

| Model | Description | Fairness | Privacy | Causality | Avg KS ↓ | SPD (Sex) ↓ | SPD (Race) ↓ | File |
|--------|-------------|-----------|----------|------------|-----------|---------------|---------------|------|
| **1️⃣ Vanilla Diffusion** | Basic diffusion model without fairness or privacy. | ❌ No | ❌ No | ❌ No | 0.301 | 0.200 | 0.200 | `vanilla_diffusion_full.pth` |
| **2️⃣ FairGAN Diffusion** | Adds fairness-aware loss to reduce bias. | ✅ Yes | ❌ No | ❌ No | 0.295 | 0.120 | 0.118 | `fairgan_diffusion_full.pth` |
| **3️⃣ DP Diffusion** | Incorporates Differential Privacy (ε=1.0). | ⚠️ Partial | ✅ Yes | ❌ No | 0.288 | 0.110 | 0.105 | `dp_diffusion_full.pth` |
| **4️⃣ CausalFairDP (Enhanced)** | Final integrated model combining fairness + privacy + causality. | ✅ Yes | ✅ Yes | ✅ Yes | **0.2113** | **0.0768** | **0.0000** | `causalfairdp_enhanced_full.pth` |

---


@article{CausalFairDP2025,
  title     = {CausalFairDP: Fair and Privacy-Preserving Synthetic Data Generation with Causal Structure Preservation using Diffusion Models},
  author    = {Esraa Halboup},
  year      = {2025},
  note      = {GitHub Repository: https://github.com/esraaH2/CausalFairDP}
}

