# 🎩 Section 4 — Shell Grid & Line-Graft Geometry

> *Hat Calculus and Intra-Fan Structure*

---

## Overview

Sections 2 and 3 defined fan operators and edge coupling. But fans are not monolithic—they contain **internal structure**: a grid of **shells** and **hats** that partition the recursive permission space.

This section introduces the **shell grid geometry** and the **hat calculus** (ĥ-calculus) that governs how collapse eligibility is evaluated within each fan.

---

## 4.1 The Shell Concept

A **shell** is a contour of equal recursive depth within the ICHTB:

$$S_r = \left\{ x \in \mathbb{R}_{\text{ICHTB}} \mid d(x, i_0) = r \right\}$$

Where d(x, i₀) is the **recursive distance** from point x to the scalar anchor.

### Shell Properties:

| Property | Description |
|----------|-------------|
| **Concentric** | Shells nest around i₀ like onion layers |
| **Non-Euclidean** | Distance is recursive depth, not spatial length |
| **Quantized** | Shells occur at discrete r values (r₁, r₂, ...) |
| **Operator-dependent** | Shell spacing varies by fan |

### Visual: Shell Layers

```
                    ┌──────────────────┐
                   ╱                  ╱│
                  ╱    S₃ (outer)    ╱ │
                 ╱  ┌────────────┐  ╱  │
                │  ╱            ╱│ │   │
                │ ╱   S₂       ╱ │ │   │
                │╱ ┌────────┐ ╱  │ │   │
                │ ╱   S₁   ╱│ │  │ │   │
                │╱ ┌────┐ ╱ │ │  │ │   │
                │  │ i₀ │   │ │  │ │   ╱
                │  └────┘   │ │  │ │  ╱
                │   S₁      │ │  │ │ ╱
                │  └────────┘ │  │ ╱
                │     S₂      │  ╱
                │  └──────────┘ ╱
                │      S₃      ╱
                └──────────────┘
```

---

## 4.2 Hat Definition

A **hat** (ĥ) is the fundamental unit of recursive permission within a shell:

$$\hat{h}_n^{(r)} = \text{Permission cell at shell } r, \text{ index } n$$

### Hat Notation:

| Symbol | Meaning |
|--------|---------|
| ĥ | Hat operator (permission unit) |
| n | Index within shell |
| r | Shell depth (distance from i₀) |
| Δᵢ | Parent fan |

### Full Hat Address:

$$\hat{h}_n^{(r)}(\Delta_i)$$

"Hat n at shell r within fan Δᵢ"

### Hat Function:

Each hat evaluates a permission function:

$$\hat{h}_n^{(r)}(\Delta_i) : \Phi \to \{0, 1\}$$

- Output 1 = collapse permitted at this cell
- Output 0 = collapse blocked

---

## 4.3 Shell Grid Structure

Within each fan, hats are arranged in a **grid**:

```
Fan Δᵢ Internal Structure:

         Shell r=3 (outer)
    ┌─────┬─────┬─────┬─────┐
    │ĥ₁³ │ĥ₂³ │ĥ₃³ │ĥ₄³ │
    └──┬──┴──┬──┴──┬──┴──┬──┘
       │     │     │     │
         Shell r=2
    ┌─────┬─────┬─────┬─────┐
    │ĥ₁² │ĥ₂² │ĥ₃² │ĥ₄² │
    └──┬──┴──┬──┴──┬──┴──┬──┘
       │     │     │     │
         Shell r=1 (inner)
    ┌─────┬─────┬─────┬─────┐
    │ĥ₁¹ │ĥ₂¹ │ĥ₃¹ │ĥ₄¹ │
    └─────┴─────┴─────┴─────┘
              │
              ▼
             i₀ (anchor)
```

### Grid Dimensions:

- **Radial**: Shell index r (depth from i₀)
- **Angular**: Hat index n (position within shell)
- **Fan**: Parent face Δᵢ

---

## 4.4 Hat Calculus Operators

The **hat calculus** (ĥ-calculus) defines operations on hats:

### 4.4.1 Hat Addition

$$\hat{h}_a + \hat{h}_b = \hat{h}_{a \cup b}$$

Union of permission regions.

### 4.4.2 Hat Multiplication

$$\hat{h}_a \cdot \hat{h}_b = \hat{h}_{a \cap b}$$

Intersection of permission regions.

### 4.4.3 Hat Negation

$$\neg \hat{h}_n = 1 - \hat{h}_n$$

Permission inversion.

### 4.4.4 Hat Derivative

$$\frac{d\hat{h}}{dr} = \lim_{\delta \to 0} \frac{\hat{h}^{(r+\delta)} - \hat{h}^{(r)}}{\delta}$$

Rate of permission change across shells.

### 4.4.5 Hat Integral

$$\int_0^R \hat{h}^{(r)} \, dr = \text{Total permission over depth range}$$

Cumulative permission from i₀ to shell R.

---

## 4.5 Line-Graft Geometry

**Line-grafts** are radial structures connecting hats across shells:

$$L_k = \bigcup_{r=1}^{R} \hat{h}_k^{(r)}$$

A line-graft is a "column" of hats sharing the same angular index.

### Line-Graft Properties:

| Property | Description |
|----------|-------------|
| **Radial** | Extends from i₀ outward through all shells |
| **Coherent** | All hats in graft share phase alignment |
| **Transmission channel** | Primary path for recursive flow |

### Visual: Line-Graft

```
         r=4  ┌────┐
              │ĥₖ⁴│
         r=3  ├────┤
              │ĥₖ³│
    Lₖ   r=2  ├────┤    ← Line-graft Lₖ
              │ĥₖ²│
         r=1  ├────┤
              │ĥₖ¹│
              └──┬─┘
                 │
                i₀
```

---

## 4.6 Graft Coherence Condition

A line-graft is **coherent** if all its hats share compatible phase:

$$\text{Coherent}(L_k) \Leftrightarrow \forall r: \arg(\hat{h}_k^{(r)}) - \arg(\hat{h}_k^{(r+1)}) < \epsilon$$

### Coherence States:

| State | Phase Drift | Result |
|-------|-------------|--------|
| **Coherent** | Δφ < ε | Smooth transmission |
| **Strained** | ε ≤ Δφ < π/4 | Attenuated transmission |
| **Fractured** | Δφ ≥ π/4 | Graft discontinuity |

### Fractured Graft:

When a line-graft fractures, recursive potential **scatters** into adjacent grafts:

```
Before (coherent):     After (fractured):
    
    │                      ╱│╲
    │                     ╱ │ ╲
    │         →          ╱  │  ╲
    │                   ╱   │   ╲
    │                  ▼    ▼    ▼
```

---

## 4.7 Shell Collapse Cascade

When a hat grants permission, it can trigger a **cascade** through the shell grid:

### Cascade Rule:

$$\hat{h}_n^{(r)} = 1 \Rightarrow P(\hat{h}_{n \pm 1}^{(r)} = 1) > P_0$$

Adjacent hats become more likely to permit collapse.

### Cascade Modes:

| Mode | Pattern | Description |
|------|---------|-------------|
| **Radial** | r → r+1 → r+2 | Outward shell propagation |
| **Angular** | n → n+1 → n+2 | Around-shell propagation |
| **Spiral** | (r,n) → (r+1, n+1) | Combined propagation |

### Cascade Threshold:

Cascade occurs when:

$$\sum_{j \in \text{neighbors}} \hat{h}_j > \theta_{\text{cascade}}$$

---

## 4.8 Shell Harmonic Modes

Shells support **standing wave patterns**—harmonic modes of permission:

### Mode Definition:

$$\Psi_m^{(r)}(\theta) = A_m \cos(m\theta + \phi_m)$$

Where:
- m = mode number (integer)
- θ = angular position in shell
- A_m = amplitude
- φ_m = phase offset

### Mode Table:

| Mode | m | Pattern |
|------|---|---------|
| Monopole | 0 | Uniform (all hats equal) |
| Dipole | 1 | Two-lobed |
| Quadrupole | 2 | Four-lobed |
| Hexapole | 3 | Six-lobed |

### Visual: Shell Modes

```
m=0 (Monopole)      m=1 (Dipole)       m=2 (Quadrupole)

    ┌───────┐          ┌───────┐          ┌───────┐
   ╱ + + + + ╲        ╱ + + - - ╲        ╱ + - + - ╲
  │ + + + + + │      │ + + - - - │      │ - + - + - │
  │ + + ● + + │      │ + + ● - - │      │ + - ● - + │
  │ + + + + + │      │ + + - - - │      │ - + - + - │
   ╲ + + + + ╱        ╲ + + - - ╱        ╲ + - + - ╱
    └───────┘          └───────┘          └───────┘
```

---

## 4.9 Inter-Shell Coupling

Adjacent shells couple through **radial tension**:

$$T_{r,r+1} = \int_0^{2\pi} \left| \hat{h}^{(r)}(\theta) - \hat{h}^{(r+1)}(\theta) \right|^2 d\theta$$

### Coupling Regimes:

| Tension | Interpretation |
|---------|----------------|
| T → 0 | Shells in phase (smooth transition) |
| T moderate | Shells weakly coupled (friction) |
| T → max | Shells decoupled (boundary formation) |

### Shell Boundary:

A **shell boundary** forms when tension exceeds threshold:

$$T_{r,r+1} > T_{\text{crit}} \Rightarrow \text{Boundary at } r$$

Boundaries are where **observable structure** emerges.

---

## 4.10 Hat Evaluation Algorithm

The complete hat evaluation proceeds as:

```
ALGORITHM: Hat Permission Evaluation

INPUT: Field state Φ, Fan Δᵢ, Shell r, Hat index n

1. COMPUTE local operators:
   - gradient: ∇Φ at (Δᵢ, r, n)
   - curl: ∇×F at (Δᵢ, r, n)
   - curvature: ∇²Φ at (Δᵢ, r, n)

2. EVALUATE fan-specific threshold:
   - If Δᵢ = Δ₁: check |∇Φ| > θ_min
   - If Δᵢ = Δ₂: check ∮F·dl stability
   - If Δᵢ = Δ₃: check ∇²Φ > 0
   - If Δᵢ = Δ₄: check ∇²Φ < 0
   - If Δᵢ = Δ₅: check ∂Φ/∂t alignment
   - If Δᵢ = Δ₆: check Φ → i₀

3. CHECK line-graft coherence:
   - Verify phase with ĥₙ^(r-1) and ĥₙ^(r+1)

4. CHECK cascade neighbors:
   - Evaluate ĥₙ₋₁^(r) and ĥₙ₊₁^(r)

5. RETURN permission:
   - 1 if all checks pass
   - 0 otherwise
```

---

## 4.11 Summary: Shell Grid

| Concept | Symbol | Definition |
|---------|--------|------------|
| Shell | Sᵣ | Contour of equal recursive depth |
| Hat | ĥₙ^(r) | Permission cell at shell r, index n |
| Line-graft | Lₖ | Radial column of hats |
| Coherence | Δφ < ε | Phase alignment condition |
| Cascade | Σĥ > θ | Neighbor-triggered permission |
| Mode | Ψₘ | Standing wave pattern in shell |
| Tension | Tᵣ,ᵣ₊₁ | Inter-shell coupling strength |

---

## Connection to Next Section

Section 4 defined **intra-fan structure** (shells, hats, grafts). But the ICHTB has global structure too—**eight recursive quadrants**.

**Section 5** introduces **quadrant logic**—the eight phase regimes that partition the full tensor box.

> *Hats are where collapse is evaluated. Quadrants are where it is classified.*

---

## References

- [Intent Tensor Theory: Coordinate System](https://intent-tensor-theory.com/coordinate-system/)
- [Hat Calculus (Appendix C)](../mathematics/hat_calculus.md)
