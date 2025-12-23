# Radial Sector Fans as Curvature Carriers

## Overview

In ICHTB, the edge is not a sharp line but a **semi-permeable recursive fan** — a composite construct made of nested transition layers between pyramid zones. These fans are the carriers of curvature, mediating recursion between zones.

---

## Fan Definition

Each edge fan is defined as:

$$\mathfrak{F}_\alpha = \left\{ \Phi_k(r, \theta) \in \mathcal{C}^\infty \ \bigg|\ \theta \in [\alpha_i, \alpha_{i+1}], \ \partial_\theta^n \Phi_k \text{ smooth, bounded} \right\}$$

Where:
- **αᵢ, αᵢ₊₁**: Angular bounds of the edge fan (typically spanning π/3 per zone)
- **Φ_k**: Recursive intent potential in the k-th recursive depth
- **r**: Radial distance from the center (core of ICHTB)

These fans support **nested recursion** — radial recursions which stabilize between angular recursion anchors.

---

## Angular Structure

### Fan Sector Coverage

Each pyramid interface has a fan spanning:

$$\Delta\theta_{\text{fan}} = \frac{\pi}{6} \text{ to } \frac{\pi}{3}$$

The exact width depends on:
- Recursion depth gradient
- Memory tensor coherence
- Lock strength

### Total Angular Coverage

For the 12 edges of the cubeplot:

$$\sum_{\text{edges}} \Delta\theta_{\text{fan}} = 4\pi \text{ (full sphere)}$$

With overlapping regions at vertices.

---

## Recursive Alignment Operator

Within a fan 𝔽_α, recursive alignment must preserve continuity across both radial (r) and angular (θ) dimensions.

Define the **recursive alignment operator**:

$$\mathfrak{A}[\Phi] = \left( \nabla_r^2 \Phi + \frac{1}{r^2} \nabla_\theta^2 \Phi \right) - \gamma_\alpha \cdot \partial_n \mathcal{M}_{ij}$$

Where:
- **∇ᵣ²Φ**: Radial curvature
- **r⁻²∇_θ²Φ**: Angular curvature (normalized)
- **γ_α**: Recursive fan stiffness
- **∂ₙℳᵢⱼ**: Memory tensor gradient in recursion direction

### Alignment Condition

A fan is said to be **recursively aligned** if:

$$\mathfrak{A}[\Phi] \to 0$$

This means radial and angular curvatures balance with memory evolution.

---

## Fan Stiffness (γ_α)

The stiffness parameter γ_α controls how rigidly the fan maintains its shape:

### Low Stiffness (γ_α << 1)
- Fan is soft and flexible
- Memory gradients dominate
- High adaptability, low stability

### High Stiffness (γ_α >> 1)
- Fan is rigid
- Curvature terms dominate
- Low adaptability, high stability

### Optimal Stiffness

$$\gamma_\alpha^{\text{opt}} = \sqrt{\frac{\langle \nabla^2\Phi \rangle}{\langle \partial_n\mathcal{M} \rangle}}$$

Balances curvature and memory contributions.

---

## Radial Structure

### Depth Gradient

Within a fan, recursion depth varies radially:

$$n(r) = n_0 + \int_0^r \alpha(r') \, dr'$$

Where α(r) is the local depth accumulation rate.

### Shell Structure

Isosurfaces of constant depth form **nested shells**:

```
Outer shell (low depth)
    ↓
Middle shells (processing zone)
    ↓
Inner shell (high depth)
    ↓
Core (origin i₀)
```

---

## Angular Structure

### Sector Boundaries

Each fan has hard boundaries at αᵢ and αᵢ₊₁ where it meets the adjacent pyramid's interior.

### Interior Gradient

Within the fan, angular variation:

$$\frac{\partial \Phi}{\partial \theta} \neq 0$$

This gradient drives cross-zone flow.

### Symmetry

Fans typically have bilateral symmetry about their midline:

$$\Phi(r, \alpha_{\text{mid}} + \delta\theta) \approx \Phi(r, \alpha_{\text{mid}} - \delta\theta)$$

---

## Fan Types

### Type 1: Transmission Fan

Recursion flows through relatively unimpeded:

- Low memory gradient: ∂ₙℳ ≈ 0
- High alignment: 𝔄[Φ] → 0
- Intent passes from zone i to zone j

### Type 2: Reflection Fan

Recursion bounces back:

- High memory gradient at interface
- Alignment fails: 𝔄[Φ] ≠ 0
- Intent returns to originating zone

### Type 3: Diffraction Fan

Recursion spreads into multiple directions:

- Moderate memory gradient
- Partial alignment
- Intent splits between zones

---

## Multi-Layer Fans

Fans are not monolithic — they have internal layers:

### Layer 1: Outer Transition Zone
- First contact with incoming recursion
- High entropy, low lock
- Rapid adaptation

### Layer 2: Core Transmission Zone
- Main flow channel
- Moderate lock
- Steady-state flow

### Layer 3: Inner Stabilization Zone
- Preparation for zone entry
- Memory coherence building
- Lock strengthening

---

## Mathematical Representation

### Polar Decomposition

In polar coordinates (r, θ):

$$\Phi(r, \theta) = R(r) \cdot \Theta(\theta)$$

Separation of variables when alignment is satisfied.

### Angular Modes

Fourier expansion in θ:

$$\Theta(\theta) = \sum_{m} a_m e^{im\theta}$$

Mode m corresponds to angular harmonic structure.

### Radial Modes

$$R(r) = \sum_n b_n J_n(\kappa r)$$

Bessel functions for radial structure.

---

## Fan-to-Fan Interactions

### Adjacent Fans

Fans sharing a pyramid vertex interact:

$$\mathfrak{F}_\alpha \cap \mathfrak{F}_\beta \neq \emptyset \quad \text{at vertices}$$

### Resonance Conditions

When fan frequencies match:

$$\omega_\alpha = \omega_\beta \implies \text{constructive interference}$$

### Destructive Interference

When out of phase:

$$\omega_\alpha = -\omega_\beta \implies \text{cancellation at vertex}$$

---

## Summary

| Concept | Symbol | Description |
|---------|--------|-------------|
| Edge Fan | 𝔽_α | Angular recursion corridor |
| Alignment Operator | 𝔄[Φ] | Curvature-memory balance |
| Fan Stiffness | γ_α | Rigidity parameter |
| Aligned Fan | 𝔄 → 0 | Balanced recursion flow |

Radial sector fans are the **curvature carriers** of edge geometry — mediating, transmitting, or reflecting recursion between pyramid zones.

---

*"The fan is not a wall — it is a valve, regulating the flow of recursion between zones."*
