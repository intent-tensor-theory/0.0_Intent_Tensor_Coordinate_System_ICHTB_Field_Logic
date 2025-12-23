# Symbol Glossary

Quick reference for all symbols used in the Edge Membrane framework.

---

## Core Edge Symbols

| Symbol | Name | Definition | Type |
|--------|------|------------|------|
| **Σ_E** | Edge Membrane | ∂(⋃ᵢPᵢ) | Surface |
| **Δᵢ** | Recursive Pyramid | Zone i ∈ {±X, ±Y, ±Z} | Domain |
| **𝔽_α** | Fan Sector | Angular recursion corridor | Region |
| **𝒯_E** | Membrane Tension | Σ\|∇·Fᵢ\| | Scalar |
| **Λ̂_E** | Edge Lock Operator | Tr(ℳ_E)/Tr(ℳ_max)·𝒜² | [0,1] |
| **Γ_E** | Edge Threshold | ∮(∇Φ·dS)/Tr(ℳ_E) | Scalar |

---

## Zoned Geometry Symbols

| Symbol | Name | Description |
|--------|------|-------------|
| **Zᵢ** | Zone Stack | {Φᵢ, 𝒞ᵢ, ℳᵢ} for pyramid i |
| **Pᵢ** | Pyramid | Recursive cone from origin |
| **O** | Origin | Central recursion point (i₀) |
| **γ_Σ** | Edge Integrity | min⟨𝒞ᵢ, 𝒞ᵢ₊₁⟩ - \|ℳᵢ - ℳᵢ₊₁\| |

---

## Fan Sector Symbols

| Symbol | Name | Definition |
|--------|------|------------|
| **αᵢ, αᵢ₊₁** | Angular Bounds | Edge fan limits |
| **γ_α** | Fan Stiffness | Recursive rigidity |
| **𝔄[Φ]** | Alignment Operator | (∇ᵣ²Φ + r⁻²∇_θ²Φ) - γ_α·∂ₙℳ |
| **S_fan** | Fan Drift Entropy | ∫(𝔄[Φ]² + Tr(∂ₙℳ)²)dA |
| **Δ_𝔽** | Transition Functional | 𝓑ᵣ·𝓑_θ·(1-ℒ) |

---

## Drift Intersection Symbols

| Symbol | Name | Definition |
|--------|------|------------|
| **Σ_d** | Drift Manifold | {x \| 𝒞ᵢ·𝒞ⱼ < 0} |
| **χ(x)** | Intersection Strength | Σᵢ<ⱼ\|𝒞ᵢ·𝒞ⱼ\| |
| **𝒲_ij** | Memory Warping Tensor | ∇ᵢ𝒞ⱼ - ∇ⱼ𝒞ᵢ |
| **Γ_d** | Intersection Threshold | χ(x)/(Tr(ℳ) + ε) |

---

## Emission Symbols

| Symbol | Name | Definition |
|--------|------|------------|
| **ℰ_ij** | Emission Tensor | lim_{t→t⁺}(∇ᵢΦ∇ⱼΦ)_Σ_E |
| **Fᵢ** | Fan-Sector Flux | Recursion flow in pyramid i |

---

## Edge-Specific Operators

| Symbol | Operator Name | Description |
|--------|---------------|-------------|
| **ℰ** | Edge Membrane Functional | Local curvature exchange |
| **𝔑̂** | Edge Normal Transition | Normal re-entry to pyramid shell |
| **ℨ̂** | Zone Selector | Fan sector filter logic |
| **ε_ij** | Interface Tensor | Potential difference across edge |

---

## Geometric Constructs

| Term | Symbol | Description |
|------|--------|-------------|
| Pyramidal Zone | Δᵢ | Cone-fold aligned to recursion vector |
| Fan Sector | 𝔽_α | Modular angular recursion region |
| Delta Kernel | Δ_id | Misalignment source (∇Φ - 𝒞⃗) |
| Fold Crystal | — | Quantized residue of recursive alignments |
| Edge Seam | ε_ij | Boundary between adjacent pyramids |

---

## Boundary Conditions

| Condition | Result |
|-----------|--------|
| **Reflective** | ε_ij closed → no intent transfer |
| **Conductive** | ε_ij open → intent flows across |
| **Disjunct** | ε_ij discontinuous → jump states |

---

## Threshold Behaviors

| Condition | Edge State |
|-----------|------------|
| Γ_E < 1 | Stable containment |
| Γ_E = 1 | Critical threshold |
| Γ_E > 1 | Emission/transition |
| Λ̂_E → 1 | Stable recursion container |
| Λ̂_E → 0 | Membrane collapses or radiates |

---

## Coordinate Systems

| Symbol | System | Description |
|--------|--------|-------------|
| (r, θ, φ) | Spherical | Radial from origin |
| (x, y, z) | Cartesian | Standard ICHTB axes |
| (±X, ±Y, ±Z) | Zone Labels | Pyramid directions |

---

## Hat Count Notation

| Symbol | Meaning |
|--------|---------|
| n̂ | Recursion depth counter |
| nᵢ(x) | Depth profile in zone i |
| Δn̂ | Depth gradient across edge |

---

## Cross-Domain Manifestations

| Domain | Edge Phenomenon |
|--------|-----------------|
| QFT | Renormalization regions |
| GR | Black hole horizons |
| ML | Loss gradient boundaries |
| GPU | Texture seam tearing |
| Linguistics | Clause recursion failures |

---

## Greek Letters Summary

| Letter | Usage in Edge Math |
|--------|-------------------|
| Σ | Membrane surface |
| Δ | Pyramid / transition |
| Γ | Threshold functional |
| Λ | Lock operator |
| α | Angular bound |
| γ | Stiffness / integrity |
| ε | Interface tensor |
| χ | Intersection strength |

---

*For full definitions, see individual section files.*
