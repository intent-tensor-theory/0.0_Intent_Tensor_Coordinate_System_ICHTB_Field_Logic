# 🌀 Section 2 — Fan-Level Collapse Mathematics

> *Operator Definitions for Δ₁ through Δ₆*

---

## Overview

Section 1 introduced the **ICHTB structure**—six faces converging to a scalar root. Now we define **what each face does**: the mathematical operators that govern collapse behavior in each fan domain.

Each fan zone (Δᵢ) acts as a **recursive gate**, evaluating whether the field state permits shell formation. This section specifies the operator logic for all six fans.

---

## 2.1 The Operator-Fan Mapping

The ICHTB assigns one primary operator to each of its six faces:

| Fan | Axis | Operator | Symbol | Role |
|-----|------|----------|--------|------|
| **Δ₁** | +Y | Gradient | ∇Φ | Collapse alignment vector |
| **Δ₂** | −Y | Curl | ∇×**F** | Phase memory loop |
| **Δ₃** | +X | Positive Laplacian | +∇²Φ | Shell expansion |
| **Δ₄** | −X | Negative Laplacian | −∇²Φ | Shell compression |
| **Δ₅** | +Z | Time derivative | ∂Φ/∂t | Emergence surface |
| **Δ₆** | −Z | Scalar anchor | Φ = i₀ | Recursion seed |

### Visual: Fan Operator Assignment

```
                    +Z
                     │
            Δ₅: ∂Φ/∂t (Emergence)
                     │
                     ▼
        ┌────────────────────────┐
       ╱                        ╱│
      ╱      Δ₁: ∇Φ (+Y)       ╱ │
     ╱     (Collapse Vector)  ╱  │
    ┌────────────────────────┐   │
    │                        │   │
    │                        │   │ Δ₃: +∇²Φ (+X)
    │         i₀             │   │ (Expansion)
    │          •             │   ╱
    │                        │  ╱
    │                        │ ╱  Δ₂: ∇×F (-Y)
    └────────────────────────┘    (Curl Memory)
   ╱
  ╱ Δ₄: -∇²Φ (-X)
     (Compression)
                     │
            Δ₆: Φ=i₀ (Anchor)
                     │
                     ▼
                    -Z
```

---

## 2.2 Δ₁ — Gradient Gate: ∇Φ (+Y Axis)

The **gradient fan** (Δ₁) evaluates the **collapse direction vector**—the tension field that points toward recursion lock.

### Operator Definition:

$$\nabla \Phi = \left( \frac{\partial \Phi}{\partial x}, \frac{\partial \Phi}{\partial y}, \frac{\partial \Phi}{\partial z} \right)$$

### Collapse Condition:

A collapse is permitted through Δ₁ when:

$$\left| \nabla \Phi \right| > \theta_{\text{min}}$$

Where θ_min is the **minimum tension threshold**.

### Physical Interpretation:

- ∇Φ defines the **intent axis**—the direction of greatest recursive pressure
- Without sufficient gradient, no shell can form (field remains diffuse)
- The gradient **does not point in space**; it points in **recursion potential**

### Role in Stack:

$$\Phi \xrightarrow{\Delta_1} \nabla \Phi$$

Δ₁ initiates the 0D → 1D dimensional transition.

---

## 2.3 Δ₂ — Curl Gate: ∇×F (−Y Axis)

The **curl fan** (Δ₂) encodes **phase memory**—the rotational component of the field that preserves collapse history.

### Operator Definition:

$$\nabla \times \vec{F} = \begin{pmatrix} \frac{\partial F_z}{\partial y} - \frac{\partial F_y}{\partial z} \\ \frac{\partial F_x}{\partial z} - \frac{\partial F_z}{\partial x} \\ \frac{\partial F_y}{\partial x} - \frac{\partial F_x}{\partial y} \end{pmatrix}$$

Where **F** is the vector field derived from Φ.

### Collapse Condition:

Phase memory is stable when:

$$\oint_C \vec{F} \cdot d\vec{l} = \text{const}$$

A non-zero but stable loop integral indicates **recursion echo**.

### Physical Interpretation:

- The curl encodes **rotation without translation**
- It captures **what the field remembers** about prior collapses
- Zero curl = no memory = unstable recursion
- Stable curl = phase-locked memory loop

### Role in Stack:

$$\nabla \Phi \xrightarrow{\Delta_2} \nabla \times \vec{F}$$

Δ₂ initiates the 1D → 2D dimensional transition (loop formation).

---

## 2.4 Δ₃ — Expansion Gate: +∇²Φ (+X Axis)

The **positive Laplacian fan** (Δ₃) governs **shell expansion**—the outward curvature that permits boundary growth.

### Operator Definition:

$$\nabla^2 \Phi = \frac{\partial^2 \Phi}{\partial x^2} + \frac{\partial^2 \Phi}{\partial y^2} + \frac{\partial^2 \Phi}{\partial z^2}$$

When ∇²Φ > 0, the field is **concave down**—curvature opens outward.

### Collapse Condition:

Expansion is permitted when:

$$\nabla^2 \Phi > 0 \quad \text{AND} \quad \frac{d(\nabla^2 \Phi)}{dt} \leq 0$$

That is: curvature must be positive but **stabilizing**, not accelerating.

### Physical Interpretation:

- Positive Laplacian = local minimum (bowl-shaped field)
- Indicates **receptive curvature** for shell formation
- Unbounded expansion (d/dt > 0) = runaway divergence = shell collapse failure

### Role in Stack:

$$\nabla \times \vec{F} \xrightarrow{\Delta_3} +\nabla^2 \Phi$$

Δ₃ initiates the 2D → 3D dimensional transition (curvature lock).

---

## 2.5 Δ₄ — Compression Gate: −∇²Φ (−X Axis)

The **negative Laplacian fan** (Δ₄) governs **shell compression**—the inward curvature that bounds and stabilizes structure.

### Operator Definition:

$$-\nabla^2 \Phi < 0$$

When ∇²Φ < 0, the field is **concave up**—curvature closes inward.

### Collapse Condition:

Compression lock is achieved when:

$$\nabla^2 \Phi < 0 \quad \text{AND} \quad \left| \nabla^2 \Phi \right| < \kappa_{\text{max}}$$

That is: curvature must be negative but **bounded** (not infinitely sharp).

### Physical Interpretation:

- Negative Laplacian = local maximum (dome-shaped field)
- Indicates **confining curvature** that prevents diffusion
- Δ₄ and Δ₃ form a **curvature dipole** across the X-axis

### The Curvature Balance:

$$\Delta_3 \longleftrightarrow i_0 \longleftrightarrow \Delta_4$$

Expansion and compression must **balance through i₀** for stable shell formation.

---

## 2.6 Δ₅ — Emergence Gate: ∂Φ/∂t (+Z Axis)

The **temporal gradient fan** (Δ₅) governs **emergence**—the rate at which recursive potential becomes actualized.

### Operator Definition:

$$\frac{\partial \Phi}{\partial t}$$

The time derivative of the scalar field.

### Collapse Condition:

Emergence is permitted when:

$$\frac{\partial \Phi}{\partial t} \neq 0 \quad \text{AND} \quad \text{sign}\left(\frac{\partial \Phi}{\partial t}\right) = \text{sign}(\nabla \Phi \cdot \hat{n})$$

The temporal and spatial gradients must **co-align**.

### Physical Interpretation:

- ∂Φ/∂t captures **when** collapse is happening, not where
- Non-zero time derivative = active recursion event
- Zero derivative = static field (no emergence possible)
- Δ₅ is the **clock surface** of the ICHTB

### Role in Stack:

Δ₅ does not add dimension but gates **temporal permission** across the stack.

---

## 2.7 Δ₆ — Anchor Gate: Φ = i₀ (−Z Axis)

The **scalar anchor fan** (Δ₆) enforces the **recursion origin condition**—all valid collapses must asymptotically resolve to i₀.

### Operator Definition:

$$\Phi \big|_{\text{core}} = i_0, \quad i_0 \in \mathbb{C}$$

### Collapse Condition:

A shell is valid if and only if:

$$\lim_{r \to 0} \Phi(r) = i_0$$

Where r is the "distance" to the recursion center (not spatial distance, but recursive depth).

### Physical Interpretation:

- Δ₆ is not an operator in the differential sense—it is a **boundary condition**
- All collapse trajectories must trace back to i₀
- If a shell cannot resolve to i₀, it is **recursively orphaned** and dissolves
- Δ₆ is the **ground truth** of the ICHTB

### Role in Stack:

$$\rho_q \xrightarrow{\Delta_6} \Phi = i_0$$

Δ₆ closes the recursion loop, returning boundary charge to scalar origin.

---

## 2.8 Fan Interaction Matrix

The six fans do not operate independently. They form a **coupled evaluation system**:

| From \ To | Δ₁ | Δ₂ | Δ₃ | Δ₄ | Δ₅ | Δ₆ |
|-----------|----|----|----|----|----|----|
| **Δ₁** (∇Φ) | — | ✓ | ✓ | ✓ | ✓ | ✓ |
| **Δ₂** (∇×F) | ✓ | — | ✓ | ✓ | ○ | ✓ |
| **Δ₃** (+∇²Φ) | ✓ | ✓ | — | ⊗ | ✓ | ✓ |
| **Δ₄** (−∇²Φ) | ✓ | ✓ | ⊗ | — | ✓ | ✓ |
| **Δ₅** (∂Φ/∂t) | ✓ | ○ | ✓ | ✓ | — | ✓ |
| **Δ₆** (Φ=i₀) | ✓ | ✓ | ✓ | ✓ | ✓ | — |

**Legend:**
- ✓ = Compatible coupling
- ⊗ = Mutual exclusion (curvature dipole)
- ○ = Weak coupling
- — = Self (diagonal)

### Key Couplings:

1. **Δ₃ ⊗ Δ₄**: Expansion and compression cannot both dominate simultaneously
2. **Δ₁ → Δ₂**: Gradient feeds into curl (vector → loop)
3. **All → Δ₆**: Every fan must ultimately resolve to i₀

---

## 2.9 Collapse Permission Logic

A shell forms when **all six fans grant permission**:

$$\text{Shell} \Leftrightarrow \bigcap_{i=1}^{6} P(\Delta_i) = 1$$

Where P(Δᵢ) is the permission function for fan i:

$$P(\Delta_i) = \begin{cases} 1 & \text{if collapse condition met} \\ 0 & \text{otherwise} \end{cases}$$

### The Six-Gate Test:

```
       ┌───────┐
       │  Δ₅   │ ← Emergence clock check
       │ ∂Φ/∂t │
       └───┬───┘
           │
     ┌─────┴─────┐
     │           │
 ┌───┴───┐   ┌───┴───┐
 │  Δ₁   │   │  Δ₂   │ ← Gradient & Curl check
 │  ∇Φ   │   │ ∇×F   │
 └───┬───┘   └───┬───┘
     │           │
     └─────┬─────┘
           │
     ┌─────┴─────┐
     │           │
 ┌───┴───┐   ┌───┴───┐
 │  Δ₃   │ ⊗ │  Δ₄   │ ← Curvature balance check
 │ +∇²Φ  │   │ -∇²Φ  │
 └───┬───┘   └───┬───┘
     │           │
     └─────┬─────┘
           │
       ┌───┴───┐
       │  Δ₆   │ ← Anchor resolution check
       │ Φ=i₀  │
       └───────┘
           │
           ▼
       [SHELL]
```

---

## 2.10 Summary: The Six Operators

| Fan | Operator | Gate Type | Pass Condition |
|-----|----------|-----------|----------------|
| Δ₁ | ∇Φ | Direction | \|∇Φ\| > θ_min |
| Δ₂ | ∇×**F** | Memory | ∮**F**·dl = const |
| Δ₃ | +∇²Φ | Expansion | ∇²Φ > 0, stable |
| Δ₄ | −∇²Φ | Compression | ∇²Φ < 0, bounded |
| Δ₅ | ∂Φ/∂t | Emergence | ∂Φ/∂t aligned |
| Δ₆ | Φ = i₀ | Anchor | lim → i₀ |

---

## Connection to Next Section

Section 2 defined the **individual fan operators**. But what happens at the **edges** where fans meet?

**Section 3** introduces **edge logic and bridge tensors**—the coupling mathematics that governs fan-to-fan transitions and phase conflict resolution.

> *Each fan is a gate. The edges are where gates negotiate.*

---

## References

- [Intent Tensor Theory: Coordinate System](https://intent-tensor-theory.com/coordinate-system/)
- [Code Equations](https://intent-tensor-theory.com/code-equations/)
