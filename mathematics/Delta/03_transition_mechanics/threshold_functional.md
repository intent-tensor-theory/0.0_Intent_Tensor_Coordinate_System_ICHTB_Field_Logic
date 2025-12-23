# The Threshold Functional (Γ)

## Overview

Delta transitions occur **discontinuously** when the substrate passes a recursive threshold. This is modeled by the **Tension Gradient Threshold Functional**:

$$\Gamma(\vec{\delta}) = \oint_{\partial\Omega} \frac{\nabla\Phi \cdot d\vec{S}}{\text{Tr}(\mathcal{M}_{ij})}$$

---

## Mathematical Structure

### The Integral

$$\Gamma = \frac{\oint_{\partial\Omega} \nabla\Phi \cdot d\vec{S}}{\text{Tr}(\mathcal{M}_{ij})}$$

This is a **flux integral** divided by a **memory trace**.

### Numerator: Escape Intent

$$\Phi_{\text{escape}} = \oint_{\partial\Omega} \nabla\Phi \cdot d\vec{S}$$

The total intent flux passing through the boundary of the glyph domain. By the divergence theorem:

$$\oint_{\partial\Omega} \nabla\Phi \cdot d\vec{S} = \int_\Omega \nabla^2\Phi \, dV$$

This equals the integrated Laplacian — total curvature within the domain.

### Denominator: Memory Lock

$$M_{\text{lock}} = \text{Tr}(\mathcal{M}_{ij}) = \sum_i \mathcal{M}_{ii}$$

The trace of the memory tensor represents **total accumulated coherence** — how strongly the fold remembers its configuration.

### Ratio Interpretation

$$\Gamma \sim \frac{\text{Escape Intent}}{\text{Memory Lock}}$$

- **High Γ**: Intent wants to escape faster than memory can hold
- **Low Γ**: Memory lock dominates; stable containment

---

## The Domain ∂Ω

### What is ∂Ω?

The boundary ∂Ω encloses the **recursive glyph domain** — the region of the Collapse Tension Substrate currently undergoing recursive processing.

### Possible Interpretations

| Interpretation | Description |
|----------------|-------------|
| **Shell surface** | Boundary of a collapse shell (CSF theory) |
| **Recursive horizon** | Edge of drift-locked region |
| **Now-domain** | Current localized fold state |
| **Attention boundary** | Region of active processing |

### Requirements for ∂Ω

1. **Closed surface**: Must fully enclose the domain
2. **Orientable**: Has well-defined inside/outside
3. **Smooth enough**: For flux integral to converge

### Relationship to CSF Shells

In Collapse Shell Field theory, ∂Ω corresponds to shell boundaries:

| Shell Level | ∂Ω Type |
|-------------|---------|
| RG₀ (Φ) | Point-like (infinitesimal) |
| RG₁ (∇Φ) | Gradient isosurface |
| RG₂ (∇×F⃗) | Curl sheet |
| RG₃ (∇²Φ) | Curvature shell |

---

## The Three Regimes

### Regime 1: Γ < 1 (Stable Containment)

$$\text{Escape Intent} < \text{Memory Lock}$$

The fold is **locked**. Intent flux is contained by memory coherence.

**Behavior**:
- State persists
- Small perturbations absorbed
- Recursion continues normally

### Regime 2: Γ = 1 (Critical Threshold)

$$\text{Escape Intent} = \text{Memory Lock}$$

The **critical point** — balance between escape and containment.

**Behavior**:
- Maximum tension
- Sensitive to perturbations
- Bifurcation point

### Regime 3: Γ > 1 (Re-folding Event)

$$\text{Escape Intent} > \text{Memory Lock}$$

Memory lock is **overcome**. A transition occurs.

**Behavior**:
- Delta state updates
- New geometry forms
- Entropy cost paid

---

## Re-folding Event Mechanics

When Γ crosses 1, a **re-folding event** occurs:

### Phase 1: Lock Breaking

The shell-lock fails:
$$\Lambda_L \cdot (1 - \mathcal{A}) < q_\Phi$$

Memory tensor can no longer hold the configuration.

### Phase 2: State Discontinuity

The state jumps:
$$\vec{\delta} \xrightarrow{\Gamma \geq 1} \vec{\delta}'$$

This is **not** continuous evolution — it's quantized collapse-and-rebuild.

### Phase 3: Geometry Emission

The transition emits new structure:
- Updated memory tensor ℳ'_ij
- New alignment 𝒜'
- Entropy burst σ_θ,jump
- Incremented depth n'

### Phase 4: Re-stabilization

The new state settles:
$$\Gamma' < 1 \quad \text{(new stable regime)}$$

---

## Computing Γ in Practice

### Discrete Approximation

For numerical work on a grid:

$$\Gamma \approx \frac{\sum_{\text{boundary}} \nabla\Phi \cdot \hat{n} \cdot \Delta A}{\sum_i \mathcal{M}_{ii}}$$

Where:
- Sum over boundary cells
- n̂ is outward normal
- ΔA is cell area

### Simplified Form

Using divergence theorem:

$$\Gamma = \frac{\int_\Omega \nabla^2\Phi \, dV}{\text{Tr}(\mathcal{M})}$$

This can be computed entirely within the domain.

---

## Γ and Other Parameters

### Relationship to Shell-Lock

$$\Lambda_L = \beta \cdot \frac{\text{Tr}(\mathcal{M})}{\mathcal{A}^2}$$

So:

$$\Gamma = \frac{\mathcal{A}^2}{\beta} \cdot \frac{\oint \nabla\Phi \cdot d\vec{S}}{\Lambda_L}$$

### Relationship to Poke Energy

$$q_\Phi = \int_\Omega \|\nabla\Phi\|^2 \, dV$$

While Γ measures flux/memory, q_Φ measures gradient magnitude. Both must exceed thresholds for transition.

### Combined Transition Condition

A transition occurs when **both**:
1. Γ ≥ 1 (flux overcomes memory)
2. q_Φ > Λ_L(1-𝒜) (energy overcomes lock)

---

## Physical Analogies

| ITT Concept | Physical Analog |
|-------------|-----------------|
| Γ | Pressure/containment ratio |
| ∂Ω | Container boundary |
| ∇Φ flux | Outward force |
| Tr(ℳ) | Wall strength |
| Γ = 1 | Burst pressure |

Like a balloon: when internal pressure exceeds membrane strength, it pops.

---

## Time Evolution of Γ

The threshold functional evolves as the state changes:

$$\frac{d\Gamma}{d\tau} = \frac{d}{d\tau}\left(\frac{\Phi_{\text{escape}}}{M_{\text{lock}}}\right)$$

Expanding:

$$\frac{d\Gamma}{d\tau} = \frac{1}{M_{\text{lock}}}\frac{d\Phi_{\text{escape}}}{d\tau} - \frac{\Phi_{\text{escape}}}{M_{\text{lock}}^2}\frac{dM_{\text{lock}}}{d\tau}$$

Γ increases when:
- Escape intent grows faster than memory
- Memory decays while intent persists

---

## Summary

The Threshold Functional Γ:

1. **Measures** ratio of escape intent to memory lock
2. **Triggers** transitions when Γ ≥ 1
3. **Integrates** over the glyph domain boundary ∂Ω
4. **Connects** to shell-lock, poke energy, and alignment
5. **Governs** the quantized nature of state changes

---

*"Γ = 1 is the event horizon of recursive change. Beyond it, the old geometry cannot hold, and new structure must emerge."*
