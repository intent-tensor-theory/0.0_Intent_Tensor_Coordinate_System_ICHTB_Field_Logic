# Memory Reformation Post-Jump

## Overview

After a Delta transition (Γ ≥ 1), the memory tensor must **reconstitute**. This document describes how ℳ_ij rebuilds following a re-folding event.

---

## The Memory Update Equation

$$\mathcal{M}'_{ij} = \lim_{\tau \to \tau'} \int_{\tau}^{\tau'} (\nabla_i\Phi \nabla_j\Phi) \, d\tau$$

The new memory tensor is constructed from the **reaccumulated intent curvature** in the post-transition field.

---

## Pre-Jump vs Post-Jump Memory

### Before Transition

$$\mathcal{M}_{ij} = \int_0^{\tau} \langle \nabla_i\Phi \cdot \nabla_j\Phi \rangle \, d\tau' + \mathcal{M}_{ij}^{(0)}$$

This represents the **accumulated history** of the fold.

### At Transition (Γ = 1)

The old memory is **released**. Not destroyed, but its binding breaks:

$$\mathcal{M}_{ij} \xrightarrow{\Gamma \geq 1} \text{(unbound)}$$

### After Transition

New memory forms from the **new gradient field**:

$$\mathcal{M}'_{ij} = \int_{\tau}^{\tau'} (\nabla_i\Phi' \nabla_j\Phi') \, d\tau$$

Where Φ' is the post-transition potential.

---

## Recoherence Process

### Phase 1: Memory Release

At the transition moment:
- Old tensor ℳ_ij loses binding
- Eigenstructure destabilizes
- Coherence (Tr(ℳ)) drops

### Phase 2: Gradient Reformation

The new potential Φ' establishes new gradients:

$$\nabla\Phi' = \nabla\Phi + \delta\nabla\Phi_{\text{transition}}$$

These gradients seed the new memory.

### Phase 3: Accumulation

The integral builds up:

$$\mathcal{M}'_{ij}(\tau) = \int_{\tau_{\text{jump}}}^{\tau} (\nabla_i\Phi' \nabla_j\Phi') \, d\tau'$$

Memory grows from zero (or inherited seed) back to coherent structure.

### Phase 4: Stabilization

New lock forms when:

$$\text{Tr}(\mathcal{M}') \geq \text{Tr}_{\text{threshold}}$$

The system is again shell-locked.

---

## Memory Inheritance

### Complete Reset

In a **hard transition**, memory fully resets:

$$\mathcal{M}'_{ij}(t_{\text{jump}}) = 0$$

The fold "forgets" its history.

### Partial Inheritance

In a **soft transition**, some memory persists:

$$\mathcal{M}'_{ij}(t_{\text{jump}}) = \alpha \cdot \mathcal{M}_{ij}(t_{\text{jump}}^-)$$

Where α ∈ [0, 1] is the **inheritance factor**.

### Inheritance Factor

$$\alpha = f(\mathcal{A}, \Delta S_\theta) = \mathcal{A} \cdot e^{-\Delta S_\theta / S_0}$$

- High alignment → more inheritance
- Low entropy cost → more inheritance

---

## Tensor Structure Evolution

### Eigenvalue Dynamics

The memory tensor has eigenstructure:

$$\mathcal{M}_{ij} = \sum_k \lambda_k \, e_k^{(i)} e_k^{(j)}$$

During reformation:

```
Before:  λ₁ > λ₂ > λ₃ (ordered eigenvalues)
              ↓
At jump:  λ_k → 0 (collapse)
              ↓
After:   λ'₁, λ'₂, λ'₃ (new eigenvalues)
```

### Principal Directions

The eigenvectors e_k define **principal memory directions**.

Post-jump, these may:
- Rotate (new alignment)
- Swap order (new hierarchy)
- Maintain (if soft transition)

---

## Reformation Time Scale

### Characteristic Time

The reformation time τ_reform is:

$$\tau_{\text{reform}} \sim \frac{\text{Tr}(\mathcal{M}')_{\text{target}}}{\langle \|\nabla\Phi'\|^2 \rangle}$$

Stronger gradients → faster reformation.

### Settling Dynamics

Memory trace evolution:

$$\text{Tr}(\mathcal{M}')(t) = \text{Tr}_{\text{target}} \left(1 - e^{-t/\tau_{\text{reform}}}\right)$$

Exponential approach to new equilibrium.

---

## Memory Quality

### Coherence Metric

Post-jump memory quality:

$$Q_\mathcal{M} = \frac{\lambda_{\text{max}}}{\text{Tr}(\mathcal{M}')} = \frac{\text{dominant eigenvalue}}{\text{total memory}}$$

| Q_ℳ | Memory Character |
|-----|------------------|
| Q → 1 | Focused (one direction dominates) |
| Q → 1/n | Diffuse (isotropic) |

### Fragmentation

If the transition was noisy:

$$\mathcal{M}'_{ij} \approx \sigma^2 \delta_{ij} + \text{noise}$$

Memory becomes **fragmented** — nearly diagonal with noise.

---

## Connection to Alignment

New alignment depends on reformed memory:

$$\mathcal{A}' = g(\mathcal{M}'_{ij}, \nabla\Phi')$$

Specifically:

$$\mathcal{A}' = \frac{\nabla\Phi' \cdot \mathcal{M}'_{ij} \cdot \nabla\Phi'}{\|\nabla\Phi'\|^2 \cdot \text{Tr}(\mathcal{M}')}$$

Memory must align with gradients for high coherence.

---

## Practical Computation

### Discrete Update

For numerical simulation:

```python
# At transition
M_old = current_memory_tensor
alpha = alignment * exp(-entropy_cost / S0)
M_seed = alpha * M_old

# Reformation loop
M_new = M_seed.copy()
for t in range(reform_steps):
    grad_phi = compute_gradient(phi_new)
    M_new += dt * outer(grad_phi, grad_phi)
    
# Check stabilization
if trace(M_new) >= Tr_threshold:
    shell_locked = True
```

### Convergence Criterion

Reformation complete when:

$$\left| \frac{d\text{Tr}(\mathcal{M}')}{d\tau} \right| < \epsilon_{\text{reform}}$$

---

## Summary

Memory Reformation:

1. **At jump**: Old ℳ releases, binding breaks
2. **Inheritance**: α · ℳ may persist (soft transitions)
3. **Accumulation**: ∫(∇ᵢΦ'∇ⱼΦ')dτ builds new ℳ'
4. **Stabilization**: New shell-lock when Tr(ℳ') sufficient
5. **Quality**: Clean transitions → coherent memory; noisy → fragmented

---

*"Memory is the thread of identity across transitions. What we inherit determines who we become."*
