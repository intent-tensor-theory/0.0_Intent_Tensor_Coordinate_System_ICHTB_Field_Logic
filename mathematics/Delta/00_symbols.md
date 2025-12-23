# Symbol Glossary

Quick reference for all symbols used in the Delta framework.

---

## Core Delta Symbols

| Symbol | Name | Definition | Type |
|--------|------|------------|------|
| **Δ_id** | Identity Kernel | ∇Φ - 𝒞⃗ | Scalar/Vector |
| **δ⃗** | State Vector | {𝒜, σ_θ, ℳ_ij, n} | Tuple |
| **𝔗̂** | Transition Operator | δ⃗ₙ₊₁ = 𝔗̂(q_Φ)·δ⃗ₙ | Operator |
| **Γ** | Threshold Functional | ∮(∇Φ·dS⃗)/Tr(ℳ) | Scalar |

---

## State Vector Components

| Symbol | Name | Description | Range |
|--------|------|-------------|-------|
| **𝒜** | Alignment Scalar | Recursive coherence | [0, 1] |
| **σ_θ** | Entropy Rate | Unbinding/production rate | ≥ 0 |
| **ℳ_ij** | Memory Tensor | State coherence matrix | Symmetric |
| **n** | Recursion Depth | Stack depth / hat count | ℕ |

---

## Transition Parameters

| Symbol | Name | Definition | Units |
|--------|------|------------|-------|
| **q_Φ** | Poke Energy | ∫_Ω ‖∇Φ‖² d³x | [Joules] |
| **Λ_L** | Shell-Lock Threshold | β·Tr(ℳ)/𝒜² | [Joules] |
| **β** | Stiffness Constant | Substrate rigidity | Empirical |

---

## Entropy Dynamics

| Symbol | Name | Description |
|--------|------|-------------|
| **ΔS_θ** | Entropy Cost | ∫(𝒟(1-ℒ))dτ |
| **𝒟** | Drift Magnitude | Misalignment velocity |
| **ℒ** | Shell-Lock Strength | Resistance to transition |

---

## Domain & Boundary

| Symbol | Name | Description |
|--------|------|-------------|
| **Ω** | Glyph Domain | Recursive fold region |
| **∂Ω** | Domain Boundary | Shell-surface of fold |
| **dS⃗** | Surface Element | Oriented area element |

---

## Post-Jump Dynamics

| Symbol | Name | Definition |
|--------|------|------------|
| **ℳ'_ij** | Updated Memory | lim∫(∇ᵢΦ∇ⱼΦ)dτ |
| **k** | Decay Constant | Drift settling rate |
| **τ, τ'** | Time Markers | Pre/post transition |

---

## Threshold Regimes

| Condition | Name | Result |
|-----------|------|--------|
| Γ < 1 | Stable | Containment holds |
| Γ = 1 | Critical | Threshold reached |
| Γ > 1 | Transition | Re-folding event |

---

## Dimensional Stack Reference

| Dimension | Primary Object |
|-----------|----------------|
| 0D | Φ (scalar potential) |
| 1D | ∇Φ (gradient) |
| 1.5D | Δ_id (identity kernel) |
| 2D | ∇×F⃗ (curl/memory) |
| 2.5D | δ⃗ (state vector) |
| 3D | ∇²Φ (curvature) |
| 3.5D | ρ_q (charge emission) |

---

## Greek Letters Summary

| Letter | Usage in Delta |
|--------|----------------|
| Δ | Identity kernel / change |
| δ | State vector |
| Γ | Threshold functional |
| Λ | Shell-lock threshold |
| σ | Entropy rate |
| τ | Recursive time |
| Φ | Intent potential |
| β | Stiffness constant |

---

## Operator Summary

| Operator | Action |
|----------|--------|
| ∇ | Gradient |
| ∇² | Laplacian |
| ∮ | Closed surface integral |
| Tr() | Matrix trace |
| ‖·‖_F | Frobenius norm |
| exp() | Exponential |

---

*For full definitions, see individual section files.*
