# 🎩 Appendix C — Hat Calculus (ĥ-Calculus)

> *Formal Derivations for Recursive Permission Cells*

---

## C.1 Introduction to Hat Notation

The **hat calculus** (ĥ-calculus) provides a rigorous framework for manipulating permission cells within the ICHTB shell grid. A "hat" is not a spatial unit but a **recursive permission evaluation point**.

### Historical Note:

The caret symbol (^) in ĥ evokes:
- **Estimation** (statistical ĥ = estimator)
- **Unit vectors** (direction without magnitude)
- **Operators** (quantum ĥ = observable)

In the ICHTB, ĥ combines all three: it estimates permission, has no intrinsic size, and operates on field states.

---

## C.2 Fundamental Definitions

### Definition C.2.1: Hat Cell

A **hat** is a permission evaluation cell indexed by:
- **r** : Shell depth (radial index from i₀)
- **n** : Angular position within shell
- **Δᵢ** : Parent fan

**Full notation:**

$$\hat{h}_n^{(r)}(\Delta_i)$$

### Definition C.2.2: Hat Function

The **hat function** maps field states to binary permission:

$$\hat{h}: \mathcal{F} \times \mathbb{N} \times \mathbb{N} \times \{1..6\} \to \{0, 1\}$$

Where 𝓕 is the space of all field states.

### Definition C.2.3: Hat Value

The **value** of a hat at position (r, n, Δᵢ) given field Φ:

$$\hat{h}_n^{(r)}(\Delta_i)[\Phi] = \begin{cases} 1 & \text{if } P_i(\Phi, r, n) = \text{true} \\ 0 & \text{otherwise} \end{cases}$$

Where Pᵢ is the permission function for fan Δᵢ.

---

## C.3 Hat Algebra

### C.3.1 Binary Operations

**Hat Union (Addition):**

$$\hat{h}_a + \hat{h}_b = \max(\hat{h}_a, \hat{h}_b)$$

Permission if **either** hat permits.

**Hat Intersection (Multiplication):**

$$\hat{h}_a \cdot \hat{h}_b = \min(\hat{h}_a, \hat{h}_b) = \hat{h}_a \wedge \hat{h}_b$$

Permission if **both** hats permit.

**Hat Negation:**

$$\neg \hat{h}_n = 1 - \hat{h}_n$$

Permission inverted.

### C.3.2 Algebraic Properties

| Property | Statement | Proof |
|----------|-----------|-------|
| Idempotent | ĥ + ĥ = ĥ | max(x,x) = x |
| Idempotent | ĥ · ĥ = ĥ | min(x,x) = x |
| Commutative | ĥ_a + ĥ_b = ĥ_b + ĥ_a | max symmetric |
| Commutative | ĥ_a · ĥ_b = ĥ_b · ĥ_a | min symmetric |
| Associative | (ĥ_a + ĥ_b) + ĥ_c = ĥ_a + (ĥ_b + ĥ_c) | max associative |
| Distributive | ĥ_a · (ĥ_b + ĥ_c) = (ĥ_a · ĥ_b) + (ĥ_a · ĥ_c) | Boolean algebra |
| De Morgan | ¬(ĥ_a + ĥ_b) = (¬ĥ_a) · (¬ĥ_b) | Standard |
| Involution | ¬(¬ĥ) = ĥ | 1-(1-x) = x |

### C.3.3 Hat Lattice

The set of all hats forms a **Boolean lattice** under (+, ·, ¬):

```
           1 (universal permit)
          /|\
         / | \
        /  |  \
      ĥ_a  ĥ_b  ĥ_c  ...
        \  |  /
         \ | /
          \|/
           0 (universal deny)
```

---

## C.4 Differential Hat Calculus

### C.4.1 Radial Derivative

The **radial derivative** of a hat across shells:

$$\frac{\partial \hat{h}_n}{\partial r} = \lim_{\delta \to 0} \frac{\hat{h}_n^{(r+\delta)} - \hat{h}_n^{(r)}}{\delta}$$

**Discretized form:**

$$\Delta_r \hat{h}_n = \hat{h}_n^{(r+1)} - \hat{h}_n^{(r)} \in \{-1, 0, 1\}$$

| Δ_r ĥ | Interpretation |
|-------|----------------|
| +1 | Permission gained (enable) |
| 0 | Permission unchanged |
| −1 | Permission lost (disable) |

### C.4.2 Angular Derivative

The **angular derivative** around a shell:

$$\frac{\partial \hat{h}^{(r)}}{\partial n} = \hat{h}_{n+1}^{(r)} - \hat{h}_n^{(r)}$$

### C.4.3 Gradient of Hat Field

For continuous approximation, the **hat gradient**:

$$\nabla_{\hat{h}} = \left( \frac{\partial \hat{h}}{\partial r}, \frac{1}{r}\frac{\partial \hat{h}}{\partial \theta} \right)$$

In polar coordinates within the fan.

### C.4.4 Laplacian of Hat Field

The **hat Laplacian** (permission curvature):

$$\nabla^2_{\hat{h}} = \frac{\partial^2 \hat{h}}{\partial r^2} + \frac{1}{r}\frac{\partial \hat{h}}{\partial r} + \frac{1}{r^2}\frac{\partial^2 \hat{h}}{\partial \theta^2}$$

**Interpretation:**
- ∇²ĥ > 0: Permission is locally minimal (enabling region)
- ∇²ĥ < 0: Permission is locally maximal (blocking region)

---

## C.5 Integral Hat Calculus

### C.5.1 Radial Integration

**Cumulative permission** from i₀ to shell R:

$$H_n^{[0,R]} = \int_0^R \hat{h}_n^{(r)} \, dr$$

**Discrete form:**

$$H_n^{[0,R]} = \sum_{r=1}^{R} \hat{h}_n^{(r)}$$

### C.5.2 Angular Integration

**Shell total** permission at depth r:

$$H^{(r)} = \oint \hat{h}^{(r)}(\theta) \, d\theta = \sum_{n=1}^{N_r} \hat{h}_n^{(r)}$$

### C.5.3 Volume Integration

**Fan total** permission:

$$H_{\Delta_i} = \int_0^{R_{\max}} \oint \hat{h}^{(r)}(\theta, \Delta_i) \, d\theta \, dr$$

### Theorem C.5.1: Permission Conservation

**Statement:** In a closed system, total permission is conserved:

$$\frac{d}{dt} \sum_{\text{all hats}} \hat{h} = 0$$

Permission shifts between hats but does not create or destroy.

---

## C.6 Line-Graft Formalism

### Definition C.6.1: Line-Graft

A **line-graft** is the radial column of hats at fixed angular index:

$$L_k = \left\{ \hat{h}_k^{(r)} \mid r \in [1, R_{\max}] \right\}$$

### C.6.2 Graft Coherence

**Coherence** measures phase alignment along a graft:

$$C(L_k) = 1 - \frac{1}{R-1} \sum_{r=1}^{R-1} \left| \arg(\hat{h}_k^{(r+1)}) - \arg(\hat{h}_k^{(r)}) \right|$$

| C(L_k) | State |
|--------|-------|
| C ≈ 1 | Fully coherent |
| C ≈ 0.5 | Partially coherent |
| C ≈ 0 | Incoherent (fractured) |

### C.6.3 Graft Transmission

**Transmission coefficient** of graft L_k:

$$T(L_k) = \prod_{r=1}^{R} \hat{h}_k^{(r)}$$

If any hat in the graft is 0, the entire graft blocks transmission.

### Theorem C.6.1: Graft Factorization

**Statement:** Shell permission factors through grafts:

$$\text{Shell forms} \Leftrightarrow \exists k: T(L_k) = 1$$

At least one complete graft must be open.

---

## C.7 Shell Harmonic Analysis

### C.7.1 Fourier Decomposition

Hat distributions on a shell can be decomposed into harmonics:

$$\hat{h}^{(r)}(\theta) = \sum_{m=0}^{\infty} \left[ A_m^{(r)} \cos(m\theta) + B_m^{(r)} \sin(m\theta) \right]$$

### C.7.2 Mode Coefficients

**Cosine coefficients:**

$$A_m^{(r)} = \frac{1}{\pi} \int_0^{2\pi} \hat{h}^{(r)}(\theta) \cos(m\theta) \, d\theta$$

**Sine coefficients:**

$$B_m^{(r)} = \frac{1}{\pi} \int_0^{2\pi} \hat{h}^{(r)}(\theta) \sin(m\theta) \, d\theta$$

### C.7.3 Mode Interpretation

| Mode m | Name | Pattern |
|--------|------|---------|
| 0 | Monopole | Uniform |
| 1 | Dipole | Two-lobed |
| 2 | Quadrupole | Four-lobed |
| 3 | Hexapole | Six-lobed |
| n | 2n-pole | 2n lobes |

### C.7.4 Power Spectrum

**Modal power** at shell r:

$$P_m^{(r)} = (A_m^{(r)})^2 + (B_m^{(r)})^2$$

**Total power:**

$$P_{\text{total}}^{(r)} = \sum_{m=0}^{\infty} P_m^{(r)}$$

---

## C.8 Inter-Shell Coupling

### C.8.1 Coupling Tensor

The **inter-shell coupling tensor** between shells r and r+1:

$$K_{mn}^{(r,r+1)} = \hat{h}_m^{(r)} \cdot \hat{h}_n^{(r+1)}$$

### C.8.2 Coupling Matrix

The full coupling matrix:

$$\mathbf{K}^{(r,r+1)} = \begin{pmatrix} K_{11} & K_{12} & \cdots \\ K_{21} & K_{22} & \cdots \\ \vdots & \vdots & \ddots \end{pmatrix}$$

### C.8.3 Shell Tension

**Tension** between adjacent shells:

$$T^{(r,r+1)} = \sum_n \left| \hat{h}_n^{(r)} - \hat{h}_n^{(r+1)} \right|^2$$

| Tension | Interpretation |
|---------|----------------|
| T → 0 | Shells in phase |
| T moderate | Weak coupling |
| T → N | Shells decoupled |

### Theorem C.8.1: Boundary Formation

**Statement:** An observable boundary forms where:

$$T^{(r,r+1)} > T_{\text{crit}}$$

The tension exceeds a critical threshold.

---

## C.9 Cascade Dynamics

### C.9.1 Cascade Rule

When a hat permits, neighbors become more likely to permit:

$$P(\hat{h}_{n+1} = 1 \mid \hat{h}_n = 1) > P(\hat{h}_{n+1} = 1)$$

### C.9.2 Cascade Equation

**Discrete cascade evolution:**

$$\hat{h}_n(t+1) = \sigma\left( \sum_{j \in N(n)} w_j \hat{h}_j(t) - \theta \right)$$

Where:
- N(n) = neighbors of n
- w_j = coupling weights
- θ = activation threshold
- σ = step function

### C.9.3 Cascade Modes

| Mode | Pattern | Condition |
|------|---------|-----------|
| Quiescent | No spread | Σw < θ |
| Linear | Constant spread | Σw ≈ θ |
| Exponential | Accelerating | Σw > θ |
| Saturated | Full coverage | All ĥ = 1 |

---

## C.10 Computational Implementation

### Algorithm C.10.1: Hat Evaluation

```python
def evaluate_hat(field_state, fan_index, shell_r, hat_n):
    """
    Evaluate permission for a single hat.
    
    Parameters:
        field_state: Current Φ configuration
        fan_index: Which fan Δᵢ (1-6)
        shell_r: Shell depth from i₀
        hat_n: Angular position in shell
        
    Returns:
        0 or 1 (permission denied or granted)
    """
    # Extract local field values at (r, n, Δᵢ)
    local_phi = field_state.at(fan_index, shell_r, hat_n)
    
    # Evaluate fan-specific permission
    if fan_index == 1:  # Δ₁: Gradient
        return 1 if norm(grad(local_phi)) > THETA_MIN else 0
    elif fan_index == 2:  # Δ₂: Curl
        return 1 if curl_stable(local_phi) else 0
    elif fan_index == 3:  # Δ₃: +∇²Φ
        return 1 if laplacian(local_phi) > 0 else 0
    elif fan_index == 4:  # Δ₄: -∇²Φ
        return 1 if laplacian(local_phi) < 0 else 0
    elif fan_index == 5:  # Δ₅: ∂Φ/∂t
        return 1 if time_aligned(local_phi) else 0
    elif fan_index == 6:  # Δ₆: Φ = i₀
        return 1 if approaches_anchor(local_phi) else 0
```

### Algorithm C.10.2: Shell Integration

```python
def shell_permission(field_state, fan_index, shell_r):
    """
    Compute total permission for a shell.
    """
    N = num_hats_in_shell(shell_r)
    total = sum(
        evaluate_hat(field_state, fan_index, shell_r, n)
        for n in range(N)
    )
    return total / N  # Normalized permission density
```

---

## C.11 Summary: ĥ-Calculus Reference

| Operation | Symbol | Definition |
|-----------|--------|------------|
| Hat value | ĥₙ^(r) | Permission at (r, n) |
| Union | ĥ_a + ĥ_b | max(ĥ_a, ĥ_b) |
| Intersection | ĥ_a · ĥ_b | min(ĥ_a, ĥ_b) |
| Negation | ¬ĥ | 1 − ĥ |
| Radial derivative | ∂ĥ/∂r | ĥ^(r+1) − ĥ^(r) |
| Angular derivative | ∂ĥ/∂n | ĥₙ₊₁ − ĥₙ |
| Line-graft | Lₖ | {ĥₖ^(r) : all r} |
| Coherence | C(L) | Phase alignment metric |
| Tension | T^(r,r+1) | Inter-shell difference |

---

## References

- [Section 4: Shell Grid Geometry](../docs/04_shell_grid.md)
- [Collapse Operators (Appendix A)](./collapse_operators.md)
- [Glyph Algebra (Appendix F)](./glyph_algebra.md)
