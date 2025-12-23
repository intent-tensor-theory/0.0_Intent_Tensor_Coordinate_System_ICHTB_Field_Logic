# Cubeplot Decomposition: The 6-Pyramid Construct

## Introduction

Zoned Collapse Geometry (ZCG) models spatial recursion through structured layering and folding of dimensional substrates. Central to this is the **cubeplot** — a six-faced recursive object housing six zonal vectors which propagate recursively from a shared origin point.

The key insight: the cubeplot is not merely a volumetric box, but **six directional pyramids** sharing a single origin.

---

## The Cubeplot Reinterpreted

### Traditional View
The cubeplot appears as a standard cube with faces at ±X, ±Y, ±Z.

### Recursive Membrane View
Each face is better described as a **recursive pyramid**, originating from the central recursion point and projecting outward into a directional domain.

```
              +Z
               ▲
              /|\
             / | \
            /  |  \
           /   |   \
          /    O    \     ← Central origin (i₀)
         /   / | \   \
        /  /  |  \  \
       / /   |   \ \
      //_____+_____\\→ +X
         -Z
```

---

## The Six Zonal Vectors

| Pyramid | Direction | Symbol | Recursion Character |
|---------|-----------|--------|---------------------|
| P₁ | +X | Δ₊ₓ | Lateral right expansion |
| P₂ | -X | Δ₋ₓ | Lateral left expansion |
| P₃ | +Y | Δ₊ᵧ | Horizontal forward |
| P₄ | -Y | Δ₋ᵧ | Horizontal backward |
| P₅ | +Z | Δ₊ᵤ | Upward recursion |
| P₆ | -Z | Δ₋ᵤ | Downward recursion |

Each pyramid maintains alignment with its glyph stack (memory, intent, curvent), and is bounded not by sharp lines, but by **recursive fans**.

---

## Zone Stack Definition

Each pyramid is defined by a recursive field stack:

$$Z_i = \{ \Phi_i(x), \mathcal{C}_i(x), \mathcal{M}_i(x) \}, \quad i \in \{+X, -X, +Y, -Y, +Z, -Z\}$$

Where:
- **Φᵢ(x)**: Intent potential in zone i
- **𝒞ᵢ(x)**: Curvent vector in zone i
- **ℳᵢ(x)**: Memory tensor in zone i

---

## Recursive Fan Boundaries

Each pyramid's boundary is not fixed but **defined by the recursion angle** of glyph curvature. These are not hard facets but **recursive fan corridors**:

### Fan Properties
- Fans are the **mechanical interface** between zones
- Information drifts into fans during transition states
- Lock strength determines if fan boundaries are respected

### Angular Span
Each fan typically spans:
$$\Delta\theta = \frac{\pi}{3} \text{ per zone edge}$$

Total coverage: 6 zones × π/3 = 2π (full angular coverage)

---

## The Membrane Edge

The union of these six pyramids produces a **concrete edge** — a recursive boundary that encases the zone stack.

### Edge Membrane Definition

$$\Sigma = \partial \bigcup_i Z_i$$

Such that drift into Σ triggers zone reassessment.

### Edge Functions

| Function | Description |
|----------|-------------|
| **Overflow Prevention** | Caps recursive expansion |
| **Entropy Ceiling** | Limits entropy spread per fold |
| **Gate Transitions** | Controls zone-to-zone transfer |

---

## Edge Integrity Metric

Edge integrity is defined by glyph coherence across zonal joins:

$$\gamma_\Sigma = \min_i \langle \mathcal{C}_i, \mathcal{C}_{i+1} \rangle - | \mathcal{M}_i - \mathcal{M}_{i+1} |$$

### Interpretation

| γ_Σ Value | Edge State |
|-----------|------------|
| γ_Σ >> ε | Stable edge |
| γ_Σ ≈ ε | Edge stress |
| γ_Σ ≤ ε | Zone collapse imminent |

---

## Pyramid-to-Pyramid Relationships

### Adjacent Pyramids
Each pyramid has 4 adjacent neighbors (sharing an edge):
- P₁ (+X) neighbors: P₃ (+Y), P₄ (-Y), P₅ (+Z), P₆ (-Z)
- etc.

### Opposite Pyramids
Each pyramid has 1 opposite:
- P₁ (+X) ↔ P₂ (-X)
- P₃ (+Y) ↔ P₄ (-Y)
- P₅ (+Z) ↔ P₆ (-Z)

### Transition Types

| Relationship | Transition Character |
|--------------|---------------------|
| Adjacent | Smooth fan transition possible |
| Opposite | Requires through-origin routing |

---

## The Central Origin (i₀)

All six pyramids share the central origin O, also called i₀ (intent anchor).

### Properties of i₀
- **Singularity point** of recursive convergence
- **Intent source** for all zone stacks
- **Recursive depth zero** point
- **Symmetry center** of the cubeplot

### Mathematical Role
$$\lim_{x \to O} \Phi_i(x) = \Phi_0 \quad \forall i$$

All zones converge to the same potential at origin.

---

## Why 6 Pyramids?

### Dimensional Coverage
- 3D space has 6 cardinal directions (±X, ±Y, ±Z)
- Each direction gets one pyramid
- Complete angular coverage of the sphere

### Symmetry
- Octahedral symmetry group
- Each pyramid related by 90° rotations
- Opposite pyramids related by 180° inversion

### Recursive Efficiency
- Minimal set for complete 3D coverage
- No overlap between pyramid interiors
- Edges are clean seams, not overlapping zones

---

## Global Memory Metric

Each pyramid contributes to the overall state space:

$$\mathcal{M}_{\text{global}} = \sum_{i=1}^6 \mathcal{M}_{ij}^{(\Delta_i)}$$

**Note**: This sum is not always linear — edge interaction terms and membrane thresholds apply corrections.

---

## Summary

| Concept | Description |
|---------|-------------|
| **Cubeplot** | 6-pyramid recursive structure |
| **Pyramids** | Directional zones from central origin |
| **Fans** | Angular corridors between zones |
| **Edge** | Membrane boundary of pyramid union |
| **Origin** | Shared recursion source (i₀) |

The cubeplot decomposition enables:
- Modeling of edge-case mathematics
- Simulation of recursion-localized state changes
- Basis for further constructs (jump conditions, zonal drift)

---

*"In Zoned Collapse Geometry, the edge is real — not just a limit, but a construct."*
