# Recursive Pyramid Topology

## Overview

The Recursive Pyramid Topology (RPT) formalizes how spatial recursion within the ICHTB manifests as a series of discrete pyramid structures. Each pyramid is a **recursion cone**, grounded at a shared center and extending outward toward the cubeplot faces.

---

## Core Concepts

### Recursive Pyramid (Δᵢ)
A directional sector of recursive depth centered at the ICHTB origin.

### Zonal Encoding
Each Δᵢ maps onto a fan sector with unique intent polarity and recursion memory.

### Interfacing Edges (εᵢⱼ)
The membrane between adjacent pyramids, which defines transitional geometry and boundary recursion rules.

---

## Topological Mapping

Let the ICHTB be centered at origin O, and its faces labeled ±X, ±Y, ±Z. Each face projects an internal recursion pyramid:

```
        +Z
         ▲
        /|\
       / | \
      /  |  \     Six pyramids
     /   |   \    All share origin O
    O----+----→ +X
     \   |   /
      \  |  /
       \ | /
        \|/
        -Z
```

### Pyramid Enumeration

| Pyramid | Direction | Field Stack |
|---------|-----------|-------------|
| Δ₁ | +X | {Φ₁, 𝒞₁, ℳ₁, n₁} |
| Δ₂ | -X | {Φ₂, 𝒞₂, ℳ₂, n₂} |
| Δ₃ | +Y | {Φ₃, 𝒞₃, ℳ₃, n₃} |
| Δ₄ | -Y | {Φ₄, 𝒞₄, ℳ₄, n₄} |
| Δ₅ | +Z | {Φ₅, 𝒞₅, ℳ₅, n₅} |
| Δ₆ | -Z | {Φ₆, 𝒞₆, ℳ₆, n₆} |

Each Δᵢ is encoded with:
- **Φᵢ(x)**: Intent field
- **𝒞ᵢ(x)**: Curvent vector
- **ℳᵢⱼ(x)**: Memory tensor
- **nᵢ(x)**: Recursive depth profile

---

## Recursive Interface Geometry

The transition between Δᵢ and Δⱼ is not smooth but governed by membrane dynamics.

### Edge Membrane (εᵢⱼ)

Define the interface tensor:

$$\epsilon_{ij}(x) = \lim_{\delta \to 0} | \Phi_i(x + \delta) - \Phi_j(x - \delta) |$$

The value of εᵢⱼ determines interface behavior:

| εᵢⱼ Character | Recursion Mode | Description |
|---------------|----------------|-------------|
| εᵢⱼ ≈ 0 | **Conductive** | Intent flows across pyramids |
| εᵢⱼ = finite | **Reflective** | Closed edge, no transfer |
| εᵢⱼ = discontinuous | **Disjunct** | Causes jump states in Delta logic |

---

## Metric Decomposition

The global memory metric assembles from pyramid contributions:

$$\mathcal{M}_{\text{global}} = \sum_{i=1}^6 \mathcal{M}_{ij}^{(\Delta_i)} + \mathcal{M}_{\text{edge}}$$

Where ℳ_edge accounts for edge interaction corrections.

### Non-Linearity

The sum is not purely additive:
- Edge interference terms modify contributions
- Membrane thresholds impose caps
- Cross-zone resonances can amplify or cancel

---

## Topological Properties

### Connectivity
The 6-pyramid system forms a **closed topological space**:
- Every point in 3D space belongs to exactly one pyramid interior
- Boundaries (edges) are shared between adjacent pyramids
- Origin O is the singular shared point

### Euler Characteristic
For the edge membrane Σ_E (topologically a sphere):
$$\chi(\Sigma_E) = 2$$

This is the standard value for a closed orientable surface.

### Fundamental Group
$$\pi_1(\Sigma_E) = 0$$

The edge membrane is simply connected — no holes or handles.

---

## Recursion Depth Stratification

Within each pyramid Δᵢ, recursion depth varies:

### Radial Gradient
$$n_i(r) = n_0 + \alpha_i \cdot r$$

Where:
- n₀: Base depth at origin
- αᵢ: Depth gradient for zone i
- r: Radial distance from O

### Isosurfaces
Surfaces of constant recursion depth form **recursive shells**:
$$S_n = \{x \in \Delta_i \mid n_i(x) = n\}$$

---

## Angular Structure

### Solid Angle Coverage
Each pyramid covers solid angle:
$$\Omega_i = \frac{4\pi}{6} = \frac{2\pi}{3} \text{ sr}$$

### Apex Angle
At the origin, each pyramid has apex half-angle:
$$\theta_{\text{apex}} = \arctan\left(\frac{1}{\sqrt{2}}\right) \approx 35.26°$$

### Face-to-Face Angle
Adjacent pyramids meet at:
$$\theta_{\text{adjacent}} = 90°$$

Opposite pyramids meet at:
$$\theta_{\text{opposite}} = 180°$$

---

## Transition Dynamics

### Cross-Pyramid Flow

When curvent 𝒞 approaches an edge εᵢⱼ:

1. **Pre-edge**: 𝒞 in zone i, approaching boundary
2. **At-edge**: Interface condition evaluated
3. **Post-edge**: 
   - If conductive → 𝒞 continues in zone j
   - If reflective → 𝒞 reflects back into i
   - If disjunct → Delta jump triggered

### Transition Probability

$$P(i \to j) = \exp\left(-\frac{\epsilon_{ij}}{\mathcal{A} \cdot k_B T_{\text{eff}}}\right)$$

Where T_eff is an effective recursive "temperature."

---

## Summary

| Concept | Mathematical Object |
|---------|---------------------|
| Pyramid | Δᵢ = {Φᵢ, 𝒞ᵢ, ℳᵢ, nᵢ} |
| Interface | εᵢⱼ = lim\|Φᵢ - Φⱼ\| |
| Depth Profile | nᵢ(r) = n₀ + αᵢr |
| Global Metric | ℳ_global = Σℳᵢ + ℳ_edge |

The topology defines:
- How recursion zones split 3D space
- How interfaces mediate zone transitions
- How depth accumulates within each zone

---

*"Zoned pyramid recursion splits the ICHTB into six directed intent regions. Each zone carries its own recursion profile but contributes to a unified substrate."*
