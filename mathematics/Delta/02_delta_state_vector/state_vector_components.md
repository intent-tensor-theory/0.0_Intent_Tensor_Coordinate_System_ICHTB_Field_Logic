# Delta State Vector Components

## The State Vector

$$\vec{\delta} = \{\mathcal{A}, \sigma_\theta, \mathcal{M}_{ij}, n\}$$

The Delta state vector captures both the **dynamic** and **historical** state of a recursive glyph region in the Collapse Tension Substrate.

---

## Component 1: Alignment Scalar (𝒜)

### Definition

$$\mathcal{A} \in [0, 1]$$

The alignment scalar measures **recursive coherence** — how well the curvent flow tracks the intent gradient.

### Derivation from Identity Kernel

$$\mathcal{A} = 1 - \frac{\|\Delta_{\text{id}}\|}{\|\nabla\Phi\| + \epsilon}$$

Where ε prevents division by zero in flat regions.

### Interpretation

| 𝒜 Value | Meaning |
|---------|---------|
| 𝒜 = 1 | Perfect alignment (Δ_id = 0) |
| 𝒜 = 0.5 | Half-coherent (significant drift) |
| 𝒜 → 0 | Near-total misalignment |

### Role in Transitions

Alignment appears in the transition condition:

$$q_\Phi > \Lambda_L \cdot (1 - \mathcal{A})$$

High alignment (𝒜 → 1) means the system is already coherent — less poke energy needed to transition.
Low alignment (𝒜 → 0) means the system is drifting — more energy needed, but also more unstable.

---

## Component 2: Entropy Production Rate (σ_θ)

### Definition

$$\sigma_\theta \geq 0$$

The entropy rate measures **unbinding** — how fast coherence is being lost to drift.

### Dynamics

Entropy production increases when:
- Identity kernel fluctuates rapidly
- Shell-lock weakens
- Recursive feedback destabilizes

$$\frac{d\sigma_\theta}{d\tau} \propto \|\dot{\Delta}_{\text{id}}\|^2 \cdot (1 - \mathcal{L})$$

### Interpretation

| σ_θ Value | Meaning |
|-----------|---------|
| σ_θ ≈ 0 | Stable, locked state |
| σ_θ moderate | Active processing |
| σ_θ high | Approaching transition |

### Post-Jump Decay

After a transition, entropy decays:

$$\sigma_\theta(\tau') \to \sigma_\theta(\tau') \cdot e^{-k(\tau' - \tau)}$$

The system "settles" into its new configuration.

---

## Component 3: Memory Tensor (ℳ_ij)

### Definition

$$\mathcal{M}_{ij} \in \mathbb{R}^{n \times n}, \quad \mathcal{M}_{ij} = \mathcal{M}_{ji}$$

A symmetric tensor encoding **state coherence** — the accumulated history of intent-curvent interactions.

### Construction

The memory tensor builds from gradient products:

$$\mathcal{M}_{ij} = \int_0^\tau \langle \nabla_i\Phi \cdot \nabla_j\Phi \rangle \, d\tau' + \lambda_M \mathcal{M}_{ij}^{(0)}$$

Where:
- The integral accumulates gradient correlation
- λ_M is a memory persistence factor
- ℳ^(0) is initial/inherited memory

### Key Properties

| Property | Formula | Meaning |
|----------|---------|---------|
| Trace | Tr(ℳ) = Σ ℳ_ii | Total memory coherence |
| Determinant | det(ℳ) | Memory "volume" |
| Eigenvalues | λ_k(ℳ) | Principal memory directions |

### Role in Threshold Functional

The trace appears in both the threshold functional:

$$\Gamma(\vec{\delta}) = \oint_{\partial\Omega} \frac{\nabla\Phi \cdot d\vec{S}}{\text{Tr}(\mathcal{M}_{ij})}$$

And the shell-lock threshold:

$$\Lambda_L = \beta \cdot \frac{\text{Tr}(\mathcal{M})}{\mathcal{A}^2}$$

Higher Tr(ℳ) = stronger memory lock = harder to transition.

### Connection to Collapse Metric

The memory tensor relates to the Collapse Metric from Curvent Calculus:

$$M_{ij}^{\text{collapse}} = \langle\partial_i\Phi \partial_j\Phi\rangle - \lambda\langle F_i F_j\rangle + \mu\delta_{ij}\nabla^2\Phi$$

The first term ⟨∂ᵢΦ ∂ⱼΦ⟩ is essentially the memory tensor contribution.

---

## Component 4: Recursion Depth (n)

### Definition

$$n \in \mathbb{N}$$

The recursion depth counts how many **recursive passes** the fold has undergone — its position in the stack.

### Connection to Hat Count

In the ICHTB coordinate system, recursion depth maps to **hat count**:

| n | Hat Notation | Phase |
|---|--------------|-------|
| 0 | No hat | Raw input |
| 1 | î | First gradient pass |
| 2 | î + ĵ | Curl integration |
| 3 | î + ĵ + k̂ | Curvature lock |
| n>3 | Extended hats | Deep recursion |

### Role in Dynamics

Recursion depth affects:

1. **Shell-lock strength**: Deeper recursion = more accumulated lock
   $$\Lambda_L \propto f(n)$$

2. **Memory tensor size**: More passes = more history
   $$\text{rank}(\mathcal{M}) \leq n$$

3. **Transition cost**: Deeper states cost more entropy to change

### Update Rule

After each recursive pass:

$$n_{t+1} = n_t + 1$$

After a transition (re-folding):

$$n' = n_{\text{reset}} + \Delta n_{\text{inherited}}$$

Some recursion depth may persist through transitions (memory inheritance).

---

## The Complete State Vector

Bringing it together:

$$\vec{\delta} = \begin{pmatrix} \mathcal{A} \\ \sigma_\theta \\ \mathcal{M}_{ij} \\ n \end{pmatrix}$$

| Component | Type | Range | Updates |
|-----------|------|-------|---------|
| 𝒜 | Scalar | [0,1] | Continuously |
| σ_θ | Scalar | [0,∞) | Continuously |
| ℳ_ij | Tensor | Symmetric | Accumulates |
| n | Integer | ℕ | Discretely |

---

## State Vector Evolution

The full evolution equation:

$$\vec{\delta}_{n+1} = \hat{\mathfrak{T}}(q_\Phi) \cdot \vec{\delta}_n$$

Expands to coupled dynamics:

$$\begin{aligned}
\mathcal{A}_{n+1} &= f_\mathcal{A}(\mathcal{A}_n, \Delta_{\text{id}}, q_\Phi) \\
\sigma_{\theta,n+1} &= f_\sigma(\sigma_{\theta,n}, \mathcal{L}, \dot{\Delta}_{\text{id}}) \\
\mathcal{M}_{ij,n+1} &= \mathcal{M}_{ij,n} + \int \nabla_i\Phi \nabla_j\Phi \, d\tau \\
n_{n+1} &= n_n + 1
\end{aligned}$$

---

## Summary Table

| Symbol | Name | Physical Meaning | Mathematical Type |
|--------|------|------------------|-------------------|
| 𝒜 | Alignment | How well tracking matches intent | Normalized scalar |
| σ_θ | Entropy Rate | How fast coherence is lost | Non-negative scalar |
| ℳ_ij | Memory | Accumulated gradient history | Symmetric tensor |
| n | Depth | Recursive stack position | Natural number |

---

*"The state vector is the biography of a fold — what it knows, how aligned it is, how much it has drifted, and how deep it has gone."*
