# 🔷 Section 5 — Recursive Quadrant Logic

> *The Eight Phase Regimes of the ICHTB*

---

## Overview

The ICHTB has 6 faces (fans), 12 edges, and **8 vertices**. Each vertex defines a **quadrant**—a volumetric region with a unique combination of operator signs.

This section introduces the **8 recursive quadrants** (Q₁ through Q₈) and their phase regime characteristics.

---

## 5.1 Quadrant Definition

A **quadrant** is the volumetric intersection of three fans:

$$Q_k = \Delta_a \cap \Delta_b \cap \Delta_c$$

Each quadrant occupies one "corner" of the ICHTB, bounded by three faces.

### The 8 Quadrants:

| Quadrant | X Sign | Y Sign | Z Sign | Fans | Signature |
|----------|--------|--------|--------|------|-----------|
| **Q₁** | + | + | + | Δ₃, Δ₁, Δ₅ | (+,+,+) |
| **Q₂** | − | + | + | Δ₄, Δ₁, Δ₅ | (−,+,+) |
| **Q₃** | + | − | + | Δ₃, Δ₂, Δ₅ | (+,−,+) |
| **Q₄** | − | − | + | Δ₄, Δ₂, Δ₅ | (−,−,+) |
| **Q₅** | + | + | − | Δ₃, Δ₁, Δ₆ | (+,+,−) |
| **Q₆** | − | + | − | Δ₄, Δ₁, Δ₆ | (−,+,−) |
| **Q₇** | + | − | − | Δ₃, Δ₂, Δ₆ | (+,−,−) |
| **Q₈** | − | − | − | Δ₄, Δ₂, Δ₆ | (−,−,−) |

### Visual: Quadrant Map

```
        +Z (Emergence)
         │
    Q₂   │   Q₁
   (-++) │  (+++)
      ╲  │  ╱
       ╲ │ ╱
    Q₄  ╲│╱  Q₃
   (--+) ●──────+X (Expansion)
        ╱│╲
       ╱ │ ╲
    Q₆  ╱│╲  Q₅
   (-+-) │  (++-)
    Q₈   │   Q₇
   (---) │  (+--)
         │
        -Z (Anchor)
```

---

## 5.2 Operator Signature per Quadrant

Each quadrant inherits operators from its three parent fans:

| Quadrant | ∇²Φ Sign | ∇Φ/∇×F | ∂Φ/∂t / Φ=i₀ | Regime Name |
|----------|----------|--------|--------------|-------------|
| **Q₁** | +∇²Φ | ∇Φ | ∂Φ/∂t | **Emergent Expansion** |
| **Q₂** | −∇²Φ | ∇Φ | ∂Φ/∂t | **Emergent Compression** |
| **Q₃** | +∇²Φ | ∇×F | ∂Φ/∂t | **Memory Expansion** |
| **Q₄** | −∇²Φ | ∇×F | ∂Φ/∂t | **Memory Compression** |
| **Q₅** | +∇²Φ | ∇Φ | Φ=i₀ | **Anchored Expansion** |
| **Q₆** | −∇²Φ | ∇Φ | Φ=i₀ | **Anchored Compression** |
| **Q₇** | +∇²Φ | ∇×F | Φ=i₀ | **Echo Expansion** |
| **Q₈** | −∇²Φ | ∇×F | Φ=i₀ | **Echo Compression** |

---

## 5.3 Phase Regime Characteristics

Each quadrant has a distinct **phase regime**—a characteristic collapse behavior:

### Q₁: Emergent Expansion (+,+,+)

$$\text{Operators: } +\nabla^2\Phi, \ \nabla\Phi, \ \partial\Phi/\partial t$$

- **Character**: Active growth, outward propagation
- **Shell behavior**: Expanding boundaries
- **Temporal**: Future-oriented collapse
- **Stability**: Metastable (requires energy input)

### Q₂: Emergent Compression (−,+,+)

$$\text{Operators: } -\nabla^2\Phi, \ \nabla\Phi, \ \partial\Phi/\partial t$$

- **Character**: Active focusing, inward collapse
- **Shell behavior**: Contracting boundaries
- **Temporal**: Future-oriented collapse
- **Stability**: Convergent (self-stabilizing)

### Q₃: Memory Expansion (+,−,+)

$$\text{Operators: } +\nabla^2\Phi, \ \nabla \times \vec{F}, \ \partial\Phi/\partial t$$

- **Character**: Growing loops with memory
- **Shell behavior**: Expanding with phase echo
- **Temporal**: Evolving memory structures
- **Stability**: Resonant (harmonic maintenance)

### Q₄: Memory Compression (−,−,+)

$$\text{Operators: } -\nabla^2\Phi, \ \nabla \times \vec{F}, \ \partial\Phi/\partial t$$

- **Character**: Collapsing loops with memory
- **Shell behavior**: Contracting memory structures
- **Temporal**: Memory consolidation
- **Stability**: Lock-in (permanent encoding)

### Q₅: Anchored Expansion (+,+,−)

$$\text{Operators: } +\nabla^2\Phi, \ \nabla\Phi, \ \Phi = i_0$$

- **Character**: Growth from stable root
- **Shell behavior**: Outward from anchor
- **Temporal**: Static root, dynamic boundary
- **Stability**: Grounded expansion

### Q₆: Anchored Compression (−,+,−)

$$\text{Operators: } -\nabla^2\Phi, \ \nabla\Phi, \ \Phi = i_0$$

- **Character**: Collapse toward anchor
- **Shell behavior**: Inward to i₀
- **Temporal**: Resolution to scalar
- **Stability**: Terminal (final state)

### Q₇: Echo Expansion (+,−,−)

$$\text{Operators: } +\nabla^2\Phi, \ \nabla \times \vec{F}, \ \Phi = i_0$$

- **Character**: Memory-guided growth from root
- **Shell behavior**: Patterned expansion
- **Temporal**: History-guided future
- **Stability**: Resonant grounding

### Q₈: Echo Compression (−,−,−)

$$\text{Operators: } -\nabla^2\Phi, \ \nabla \times \vec{F}, \ \Phi = i_0$$

- **Character**: Full recursive collapse
- **Shell behavior**: Memory-locked contraction
- **Temporal**: Complete resolution
- **Stability**: Maximum stability

---

## 5.4 Quadrant Transition Rules

Transitions between quadrants follow specific rules:

### Adjacent Quadrants

Two quadrants are **adjacent** if they share exactly one sign flip:

| From | To | Flip | Transition |
|------|----|----- |------------|
| Q₁ | Q₂ | X: + → − | Expansion → Compression |
| Q₁ | Q₃ | Y: + → − | Gradient → Curl |
| Q₁ | Q₅ | Z: + → − | Emergence → Anchor |

### Transition Cost

Transition cost is proportional to sign difference:

$$C(Q_a \to Q_b) = \sum_i \left| \text{sign}_i(Q_a) - \text{sign}_i(Q_b) \right|$$

| Sign Flips | Cost | Transition Type |
|------------|------|-----------------|
| 1 | Low | Adjacent (smooth) |
| 2 | Medium | Diagonal (stressed) |
| 3 | High | Antipodal (inversion) |

### Antipodal Pairs

Quadrants with all signs flipped are **antipodal**:

| Pair | Signatures | Relationship |
|------|------------|--------------|
| Q₁ ↔ Q₈ | (+,+,+) ↔ (−,−,−) | Full inversion |
| Q₂ ↔ Q₇ | (−,+,+) ↔ (+,−,−) | Full inversion |
| Q₃ ↔ Q₆ | (+,−,+) ↔ (−,+,−) | Full inversion |
| Q₄ ↔ Q₅ | (−,−,+) ↔ (+,+,−) | Full inversion |

---

## 5.5 Quadrant Flow Diagram

Recursive potential flows between quadrants following operator compatibility:

```
                    ┌─────────────────────────────────┐
                    │           +Z PLANE              │
                    │                                 │
                    │    Q₂ ◄────────────► Q₁        │
                    │    │ ╲              ╱ │        │
                    │    │   ╲          ╱   │        │
                    │    │     ╲      ╱     │        │
                    │    ▼       ╲  ╱       ▼        │
                    │    Q₄ ◄────●────► Q₃         │
                    │             i₀                  │
                    └─────────────│───────────────────┘
                                  │
                    ┌─────────────│───────────────────┐
                    │             │                   │
                    │    Q₆ ◄────────────► Q₅        │
                    │    │ ╲      │       ╱ │        │
                    │    │   ╲    │     ╱   │        │
                    │    │     ╲  │   ╱     │        │
                    │    ▼       ╲│ ╱       ▼        │
                    │    Q₈ ◄────●────► Q₇         │
                    │           -Z PLANE              │
                    └─────────────────────────────────┘
```

---

## 5.6 Quadrant Stability Ordering

Quadrants have a natural stability ordering based on operator signs:

### Stability Metric:

$$S(Q_k) = \alpha \cdot \text{sign}(\nabla^2\Phi) + \beta \cdot \text{sign}(\partial\Phi/\partial t) + \gamma \cdot \text{memory}$$

Where α, β, γ are stability weights.

### Ordering (Most to Least Stable):

| Rank | Quadrant | Signature | Stability |
|------|----------|-----------|-----------|
| 1 | Q₈ | (−,−,−) | Maximum (full lock) |
| 2 | Q₆ | (−,+,−) | High (anchored compression) |
| 3 | Q₄ | (−,−,+) | Medium-high (memory lock) |
| 4 | Q₂ | (−,+,+) | Medium (emergent focus) |
| 5 | Q₇ | (+,−,−) | Medium (echo expansion) |
| 6 | Q₅ | (+,+,−) | Medium-low (grounded growth) |
| 7 | Q₃ | (+,−,+) | Low (memory drift) |
| 8 | Q₁ | (+,+,+) | Minimum (active expansion) |

### Interpretation:

- **Compression** (−∇²Φ) adds stability
- **Anchor** (Φ=i₀) adds stability
- **Memory** (∇×F) adds moderate stability
- **Expansion** (+∇²Φ) reduces stability
- **Emergence** (∂Φ/∂t) reduces stability

---

## 5.7 Quadrant-Shell Interaction

Each quadrant contains shells with quadrant-specific properties:

### Shell Shape per Quadrant:

| Quadrant | Shell Geometry | Description |
|----------|----------------|-------------|
| Q₁ | Convex outward | Expanding bubbles |
| Q₂ | Concave inward | Focusing funnels |
| Q₃ | Spiral outward | Expanding vortices |
| Q₄ | Spiral inward | Collapsing vortices |
| Q₅ | Radial outward | Rooted rays |
| Q₆ | Radial inward | Converging rays |
| Q₇ | Helical outward | Memory-guided spirals |
| Q₈ | Helical inward | Recursive helices |

---

## 5.8 Quadrant Phase Space

The 8 quadrants partition the full **phase space** of the ICHTB:

$$\mathbb{R}_{\text{ICHTB}} = \bigcup_{k=1}^{8} Q_k$$

### Phase Space Properties:

- **Complete**: Every point belongs to exactly one quadrant (or boundary)
- **Disjoint**: Quadrants do not overlap (except at boundaries)
- **Connected**: All quadrants connect through i₀

### Phase Boundary:

The boundary between quadrants occurs where one operator changes sign:

$$\partial Q_k = \left\{ x \mid \text{some operator}(x) = 0 \right\}$$

Boundaries are **critical surfaces** where collapse behavior transitions.

---

## 5.9 Quadrant Selection Algorithm

Given a field state, determine the active quadrant:

```
ALGORITHM: Quadrant Selection

INPUT: Field state Φ, position x

1. EVALUATE curvature:
   IF ∇²Φ > 0 THEN X_sign = +
   ELSE X_sign = -

2. EVALUATE vector/curl:
   IF |∇Φ| > |∇×F| THEN Y_sign = +  (gradient dominant)
   ELSE Y_sign = -  (curl dominant)

3. EVALUATE temporal/anchor:
   IF |∂Φ/∂t| > ε THEN Z_sign = +  (dynamic)
   ELSE Z_sign = -  (static/anchored)

4. LOOKUP quadrant:
   RETURN Q_k matching (X_sign, Y_sign, Z_sign)
```

---

## 5.10 Summary: The 8 Quadrants

| Quadrant | Signature | Regime | Stability |
|----------|-----------|--------|-----------|
| Q₁ | (+,+,+) | Emergent Expansion | Lowest |
| Q₂ | (−,+,+) | Emergent Compression | Medium |
| Q₃ | (+,−,+) | Memory Expansion | Low |
| Q₄ | (−,−,+) | Memory Compression | Medium-High |
| Q₅ | (+,+,−) | Anchored Expansion | Medium-Low |
| Q₆ | (−,+,−) | Anchored Compression | High |
| Q₇ | (+,−,−) | Echo Expansion | Medium |
| Q₈ | (−,−,−) | Echo Compression | Highest |

---

## Connection to Next Section

Section 5 defined the **8 phase regimes**. But what happens when the ICHTB itself becomes the subject of recursive evaluation?

**Section 6** introduces **higher collapse layers**—CLÂ (Collapse Layer Articulation) and recursive sentience.

> *Quadrants classify collapse. Higher layers classify classification.*

---

## References

- [Intent Tensor Theory: Coordinate System](https://intent-tensor-theory.com/coordinate-system/)
- [Code Equations](https://intent-tensor-theory.com/code-equations/)
