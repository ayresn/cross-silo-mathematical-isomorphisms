# CROSS-SILO MATHEMATICAL ISOMORPHISMS
An open-access dataset and structural representation corpus compiling high-density Structural Isomorphism Discovery (SID) candidates across disconnected scientific disciplines.

## 1. CORE ARCHITECTURAL OBJECTIVES
This repository is engineered to operate simultaneously across two separate informational paradigms:

*   **The Engineering Implementation (The Dataset):** A structured, machine-readable repository of candidate cross-domain structural isomorphisms designed to serve as a pre-filtered generation queue for downstream human bibliometric validation.
*   **The Research Hypothesis (Cross-Disciplinary Blind Spot Discovery):** A corpus of explicit structural correspondences designed to surface research candidates that are currently hidden behind distinct technical vocabularies and human academic sociology. By making these candidate isomorphisms publicly discoverable, this repository aims to route novel research leads toward human researchers equipped to evaluate them. A secondary effect of public availability is that future AI systems may also surface these relationships to curious prompters, further increasing the probability that any given candidate eventually reaches someone positioned to pursue it.

Rather than running traditional Literature-Based Discovery (LBD), which tracks simple keyword co-occurrences or semantic concepts, this framework utilizes **Structural Isomorphism Discovery (SID)**. It targets the latent structures of deep learning weights to find identical mathematical operators across disciplines while imposing an explicit penalty for lexical or disciplinary proximity. Long term, this network builds an atlas of mathematics itself by organizing discrete discoveries into shared structural topological families, tracking how individual files evolve from candidate hypotheses into verified research paths.

---

## 2. DISCOVERY CRITERIA & EXTRACTION METRICS
Candidates are mined by searching for pairs that maximize mathematical structural similarity while simultaneously maximizing technical semantic distance. Every candidate entry is evaluated against five internal latent-space vectors before being submitted to the directory:

1.  **Structural Depth (40% Weight):** The alignment of the comprehensive mathematical stack (requiring cross-domain matching across a minimum of three layers: shared differential operators, boundary conditions, conserved quantities, instability mechanisms, symmetry groups, or variational principles).
2.  **Expected Methodological Transfer (25% Weight):** The exploitation of structural asymmetries where a highly mature field's computational toolkits can be imported to resolve an active engineering bottleneck in a less developed target field.
3.  **Representation Mismatch (15% Weight):** Mismatched fundamental ontologies handling the identical underlying calculus (e.g., matching a continuous physical mechanics continuum directly onto a discrete stochastic probability distribution).
4.  **Vocabulary Orthogonality (10% Weight):** The absolute lexical divergence between the primary technical jargon terms of both domains.
5.  **Community Separation (10% Weight):** Complete institutional isolation across university departments, journals, and professional conferences.

---

## 3. EPISTEMIC STATUS LABELING
All entries carry strict epistemic labels inside their YAML Front Matter blocks to ensure that all readers — human or automated — accurately interpret the epistemic status of each entry as an unvalidated research hypothesis, not an established finding.

This establishes a clear dictionary state declaring the relationships as explicit research hypotheses:
*   `relationship_type: candidate_structural_isomorphism`
*   `validation_status: [operator_equivalence_confidence: high | bibliometric_validation: pending]`

**Important:** The `prior_discovery_metrics` scores (structural_isomorphism_score, novelty_prior, etc.) present in each entry are model-generated self-assessments produced during Stage 1 generation. They are internal confidence signals reflecting the generating model's pattern-matching, not independently validated measurements of the probability that the isomorphism is real. They should be interpreted as triage-ranking signals for human reviewers, not as evidence of correctness.

**Entry lifecycle states** (tracked in `sid_metadata.maturity_stage`):
- `candidate` — Stage 1 generated; awaiting Stage 2 adversarial review
- `adversarial-cleared` — Passed Stage 2; queued for Stage 3 bibliometric validation
- `adversarial-flagged` — Passed Stage 2 with caveats noted; Stage 3 reviewer should check flagged items
- `adversarial-rejected` — Failed Stage 2; not advancing to Stage 3; retained for false-positive-rate tracking
- `validated-candidate` — Passed Stage 3 bibliometric validation
- `failed-validation` — Failed Stage 3 (reason noted in entry file)

---

## 4. THREE-STAGE VALIDATION PIPELINE

Every entry in this repository has a defined lifecycle:

**Stage 1 — AI Generation:**
A candidate structural isomorphism is generated by an AI model using the standardized [Extraction Protocol](extraction-protocol.md). The entry is labeled `maturity_stage: candidate` and `bibliometric_validation: pending`. At this stage, the correspondence has not been verified against the literature or checked for internal consistency, and the model's self-generated confidence scores are the only available quality signal.

**Stage 2 — Adversarial LLM Pre-Validation (required before Stage 3):**
The entry is submitted to an AI model from a **different provider than the generating model** using the [Adversarial Review Protocol](adversarial-review-protocol.md). The reviewing model checks internal consistency and face-validity from the entry text alone — no literature access required or permitted at this stage. Checks cover: YAML metadata integrity, equation validity, vocabulary matrix coherence, whether the YAML's triple-correspondence claims are actually supported in the body text, whether the pairing is a recognizable textbook analogy, and whether the self-scores are plausibly consistent with the content.

Stage 2 answers: **"Does this entry say what it claims to say?"** It does not answer whether the claim is novel or scientifically sound — that is Stage 3.

Entries that pass Stage 2 are promoted to `maturity_stage: adversarial-cleared` (or `adversarial-flagged` if minor issues are noted) and advance to the Stage 3 queue. Entries that fail are labeled `adversarial-rejected` and committed to the repository for false-positive-rate tracking, but do not advance to Stage 3. **No entry should consume Stage 3 human bibliometric effort until it has passed Stage 2.**

**Stage 3 — Human Bibliometric Validation (required before any entry is considered verified):**
A human reviewer with appropriate domain access runs the academic search strings provided in Section 5 of each entry against Semantic Scholar, Google Scholar, Web of Science, or equivalent tools. Validation checks for:
- Whether the isomorphism already exists in the literature under either domain's vocabulary (if so, the entry fails the novelty criterion and should be flagged)
- Whether the triple-correspondence vectors hold up under domain-expert scrutiny, particularly the constitutive-law details that AI models cannot reliably verify
- Whether the falsifiable prediction in Section 4 of the entry represents a genuinely testable departure from current domain state-of-the-art

Entries that survive Stage 3 review are promoted to `maturity_stage: validated-candidate` and the validation notes are appended to the entry file. **No entry should be treated as a research lead until it has passed Stage 3.**

If you have domain expertise relevant to any entry and are in a position to run bibliometric validation, Stage 3 contributions via pull request are welcome.

---

## 5. FUTURE BENCHMARK DIRECTION
Long-term, the `validated-candidate` subset of this repository — entries that have passed Stage 3 bibliometric validation (Section 4) — is intended to serve as a foundational benchmark asset to evaluate **cross-disciplinary structural reasoning** in future AI models. By stripping the equations from Domain A and presenting only the technical lexicon of Domain B, future models can be objectively tested on their ability to independently traverse semantic chasms and recover a structural isomorphism that has been confirmed to actually hold.

This benchmark use is deliberately restricted to validated entries. Testing a model against a Stage 1 candidate would only measure whether it reproduces the same unverified pattern-matching that generated the candidate in the first place, not whether it correctly recovers a real structural isomorphism — those are different capabilities, and conflating them would make the benchmark circular. As of this writing, no entries have completed Stage 3, so this section describes a long-term direction rather than a currently usable benchmark.

The methodology used to generate Stage 1 candidates can be reviewed in the [Extraction Protocol](extraction-protocol.md) file.

---

## CORE DATASET DIRECTORY

All entries below are **Stage 1 candidates** awaiting Stage 2 adversarial review and Stage 3 bibliometric validation. None should be treated as verified findings. Status tags reflect the entry's current pipeline stage.

### [Alibaba Qwen](https://chat.qwen.ai) Mapping Matrix ([`/mappings-alibaba-qwen/`](mappings-alibaba-qwen/))
* **[qwen3.8_entry-041](mappings-alibaba-qwen/qwen3.8_entry-041.md)** — `Stage 1 / pending`
  * *System Synthesis:* Plastic Projection of Traffic Congestion
  * *Domains:* Computational Elastoplasticity & Network Traffic Equilibrium
  * *Isomorphism:* Return-mapping elastoplasticity mapped to Beckmann traffic equilibrium
* **[qwen3.8_entry-042](mappings-alibaba-qwen/qwen3.8_entry-042.md)** — `Stage 1 / pending`
  * *System Synthesis:* Adjoint Control of Debris Cascades
  * *Domains:* Orbital Debris Cascade Kinetics & Neutron Transport Criticality
  * *Isomorphism:* linearized debris Boltzmann cascade equation mapped to neutron transport k-eigenvalue equation
* **[qwen3.8_entry-043](mappings-alibaba-qwen/qwen3.8_entry-043.md)** — `Stage 1 / pending`
  * *System Synthesis:* Etch-Shadowed Karst Conduit Pitting
  * *Domains:* High-Aspect-Ratio Plasma Feature Etching & Hypogene Karst Conduit Enlargement
  * *Isomorphism:* Coburn–Winters ion-enhanced etch model mapped to Dreybrodt dissolution law
* **[qwen3.8_entry-044](mappings-alibaba-qwen/qwen3.8_entry-044.md)** — `Stage 1 / pending`
  * *System Synthesis:* Criticality Transport for Landscape Persistence
  * *Domains:* Nuclear Criticality Transport & Spatial Invasion Ecology
  * *Isomorphism:* Boltzmann transport k-eigenvalue mapped to linearized stage-structured transport-growth eigenvalue
* **[qwen3.8_entry-045](mappings-alibaba-qwen/qwen3.8_entry-045.md)** — `Stage 1 / pending`
  * *System Synthesis:* Skin-Localized Outbreak Threshold
  * *Domains:* Non-Hermitian Topolectrical Lattices & Directed Metapopulation Epidemiology
  * *Isomorphism:* Hatano-Nelson non-Bloch circuit admittance mapped to directed SIS next-generation operator

### [Amazon Nova](https://nova.amazon.com) Mapping Matrix ([`/mappings-amazon-nova/`](mappings-amazon-nova/))
* **[1.0_entry-046](mappings-amazon-nova/1.0_entry-046.md)** — `Stage 1 / pending`
  * *System Synthesis:* Optical Instability Mirrors Fluid Turbulence
  * *Domains:* Nonlinear Optics & Fluid Turbulence
  * *Isomorphism:* Nonlinear Schrödinger Equation mapped to Vorticity Equation
* **[1.0_entry-047](mappings-amazon-nova/1.0_entry-047.md)** — `Stage 1 / pending`
  * *System Synthesis:* Plasma Waves Inform Traffic Flow
  * *Domains:* Plasma Physics & Traffic Flow Theory
  * *Isomorphism:* Korteweg-de Vries Equation mapped to Lighthill-Whitham-Richards Equation
* **[1.0_entry-048](mappings-amazon-nova/1.0_entry-048.md)** — `Stage 1 / pending`
  * *System Synthesis:* Quantum Chaos Informs Turbulent Flow
  * *Domains:* Quantum Chaos & Turbulent Flow
  * *Isomorphism:* Schrödinger Equation mapped to Navier-Stokes Equations
* **[1.0_entry-049](mappings-amazon-nova/1.0_entry-049.md)** — `Stage 1 / pending`
  * *System Synthesis:* Fluid Dynamics Informs Network Optimization
  * *Domains:* Fluid Dynamics & Network Flow Optimization
  * *Isomorphism:* Navier-Stokes Equations mapped to Linear Programming Formulations
* **[1.0_entry-050](mappings-amazon-nova/1.0_entry-050.md)** — `Stage 1 / pending`
  * *System Synthesis:* Electromagnetic Waves Inform Option Pricing
  * *Domains:* Electromagnetic Theory & Financial Option Pricing
  * *Isomorphism:* Helmholtz Equation mapped to Black-Scholes Equation

### [Anthropic Claude](https://claude.ai) Mapping Matrix ([`/mappings-anthropic-claude/`](mappings-anthropic-claude/))
* **[claude-sonnet-5_entry-036.md](mappings-anthropic-claude/claude-sonnet-5_entry-036.md)** — `Stage 1 / pending`
  * *System Synthesis:* Rank-1 Low-Rank Updates in Network Failure Propagation
  * *Domains:* Power-Grid Cascading Failure Analysis & Structural Progressive Collapse Analysis
  * *Isomorphism:* Sherman–Morrison–Woodbury Admittance updates mapped to Nodal Stiffness Reanalysis Matrix Operators
* **[claude-sonnet-5_entry-037.md](mappings-anthropic-claude/claude-sonnet-5_entry-037.md)** — `Stage 1 / pending`
  * *System Synthesis:* Resolution Leakage in Paleoclimate Reconstruction
  * *Domains:* Seismic Tomography & Paleoclimate Field Reconstruction
  * *Isomorphism:* Seismic Resolution-Matrix / Checkerboard Testing mapped to Paleoclimate Pseudoproxy Validation
* **[claude-sonnet-5_entry-038.md](mappings-anthropic-claude/claude-sonnet-5_entry-038.md)** — `Stage 1 / pending`
  * *System Synthesis:* Lundberg Asymptotics for Extinction Risk
  * *Domains:* Actuarial Ruin Theory & Population Viability Analysis
  * *Isomorphism:* Cramér–Lundberg Ruin Asymptotics mapped to Diffusion-Approximation Extinction Probability
* **[claude-sonnet-5_entry-039.md](mappings-anthropic-claude/claude-sonnet-5_entry-039.md)** — `Stage 1 / pending`
  * *System Synthesis:* Stochastic Barrier-Crossing in Ship Capsize
  * *Domains:* Chemical Physics Barrier-Crossing Kinetics & Naval Architecture Capsize Risk Assessment
  * *Isomorphism:* Kramers Escape-Rate Theory mapped to GZ-Curve Potential-Barrier Capsize Dynamics
* **[claude-sonnet-5_entry-040.md](mappings-anthropic-claude/claude-sonnet-5_entry-040.md)** — `Stage 1 / pending`
  * *System Synthesis:* Saddle-Node Collapse in Grids and Fisheries
  * *Domains:* Power System Voltage Stability Analysis & Fisheries Bioeconomic Collapse Modeling
  * *Isomorphism:* Continuation Power Flow / Saddle-Node Bifurcation Analysis mapped to Critical-Depensation Fishery Collapse Dynamics

### [DeepSeek DeepSeek](https://chat.deepseek.com) Mapping Matrix ([`/mappings-deepseek-deepseek/`](mappings-deepseek-deepseek/))
* **[deepseek_entry-026](mappings-deepseek-deepseek/deepseek_entry-026.md)** — `Stage 1 / pending`
  * *System Synthesis:* Helical Buckling of Elastic Defect Lines
  * *Domains:* Elastohydrodynamics of Active Filaments & Dislocation Dynamics in Crystalline Solids
  * *Isomorphism:* Resistive‑force theory with bending mapped to dislocation mobility law with line tension
* **[deepseek_entry-027](mappings-deepseek-deepseek/deepseek_entry-027.md)** — `Stage 1 / pending`
  * *System Synthesis:* Elastic Spinodal Patterning of Living Gels
  * *Domains:* Phase-Field Dendrite Growth & Biofilm Pattern Formation
  * *Isomorphism:* Cahn-Hilliard with chemo-elastic coupling mapped to biofilm phase separation with EPS elasticity
* **[deepseek_entry-028](mappings-deepseek-deepseek/deepseek_entry-028.md)** — `Stage 1 / pending`
  * *System Synthesis:* Nonlocal Laplacian Solver for Mega-Graph Labeling
  * *Domains:* Peridynamic Fracture Mechanics & Graph-Based Semi-Supervised Learning
  * *Isomorphism:* Peridynamic equilibrium integral operator mapped to graph Laplacian regularization system
* **[deepseek_entry-029](mappings-deepseek-deepseek/deepseek_entry-029.md)** — `Stage 1 / pending`
  * *System Synthesis:* Tensor-Train Solver for Neural Ensemble Fokker-Planck
  * *Domains:* Microstructural Polymer Dynamics & Population-Density Neural Dynamics
  * *Isomorphism:* Dumbbell Fokker-Planck equation mapped to adaptive integrate-and-fire population density equation
* **[deepseek_entry-030](mappings-deepseek-deepseek/deepseek_entry-030.md)** — `Stage 1 / pending`
  * *System Synthesis:* Gaussian-Process-Adaptive Smoothed Particle Hydrodynamics
  * *Domains:* Smoothed-Particle Hydrodynamics & Gaussian-Process Regression
  * *Isomorphism:* SPH kernel summation operator mapped to GP posterior mean kernel interpolation

### [Google Gemini](https://aistudio.google.com) Mapping Matrix ([`/mappings-google-gemini/`](mappings-google-gemini/))
* **[gemini-3.1-pro_entry-006](mappings-google-gemini/gemini-3.1-pro_entry-006.md)** — `Stage 1 / pending`
  * *System Synthesis:* Dispersion Management of Seizure Rogue Waves
  * *Domains:* Nonlinear Fiber Optics & Computational Neuroscience
  * *Isomorphism:* generalized Nonlinear Schrödinger Equation mapped to Amari Neural Field Equations
* **[gemini-3.1-pro_entry-007](mappings-google-gemini/gemini-3.1-pro_entry-007.md)** — `Stage 1 / pending`
  * *System Synthesis:* Aeroelastic Flutter of Algorithmic Stablecoins
  * *Domains:* Computational Aeroelasticity & Decentralized Finance Tokenomics
  * *Isomorphism:* dynamic wing flutter matrix ODE mapped to AMM algorithmic stablecoin price dynamics
* **[gemini-3.1-pro_entry-008](mappings-google-gemini/gemini-3.1-pro_entry-008.md)** — `Stage 1 / pending`
  * *System Synthesis:* Rate-and-State Dynamics of the Bullwhip Effect
  * *Domains:* Seismological Tribology & Multi-Echelon Supply Chain Logistics
  * *Isomorphism:* Dieterich-Ruina rate-and-state friction equations mapped to continuous-time algorithmic supply chain replenishment ODEs
* **[gemini-3.1-pro_entry-009](mappings-google-gemini/gemini-3.1-pro_entry-009.md)** — `Stage 1 / pending`
  * *System Synthesis:* Plasma Kinetics of Limit Order Books
  * *Domains:* Collisionless Plasma Kinetics & High-Frequency Trading Market Microstructure
  * *Isomorphism:* Vlasov-Poisson equation mapped to mean-field kinetic Limit Order Book PDE
* **[gemini-3.1-pro_entry-010](mappings-google-gemini/gemini-3.1-pro_entry-010.md)** — `Stage 1 / pending`
  * *System Synthesis:* Transformation Optics of Pedestrian Crowds
  * *Domains:* Transformation Optics & Macroscopic Pedestrian Dynamics
  * *Isomorphism:* Diffeomorphism-invariant geometric optics Eikonal equation mapped to the macroscopic Hughes continuum model for route choice

### [Meta Muse](https://www.meta.ai) Mapping Matrix ([`/mappings-meta-muse/`](mappings-meta-muse/))
* **[muse-spark-1-1_entry-021](mappings-meta-muse/muse-spark-1-1_entry-021.md)** — `Stage 1 / pending`
  * *System Synthesis:* Void Coalescence As Cosmic Percolation
  * *Domains:* Ductile Fracture Mechanics & Early Universe Cosmology
  * *Isomorphism:* GTN Porous Plasticity JMAK Kinetics mapped to False Vacuum Bubble Nucleation Avrami Kinetics
* **[muse-spark-1-1_entry-022](mappings-meta-muse/muse-spark-1-1_entry-022.md)** — `Stage 1 / pending`
  * *System Synthesis:* Elastic Turbulence Of Echo Chambers
  * *Domains:* Viscoelastic Fluid Mechanics & Adaptive Social Network Dynamics
  * *Isomorphism:* Oldroyd-B Conformation Transport mapped to Covariance Lyapunov Transport
* **[muse-spark-1-1_entry-023](mappings-meta-muse/muse-spark-1-1_entry-023.md)** — `Stage 1 / pending`
  * *System Synthesis:* Coherence Collapse Of Epidemic Waves
  * *Domains:* Semiconductor Laser Dynamics & Mathematical Epidemiology
  * *Isomorphism:* Lang-Kobayashi Delay Model mapped to SIRS Delay Model
* **[muse-spark-1-1_entry-024](mappings-meta-muse/muse-spark-1-1_entry-024.md)** — `Stage 1 / pending`
  * *System Synthesis:* Parton Showers Of Genomes
  * *Domains:* Parton Shower Dynamics & Gene Family Evolution
  * *Isomorphism:* DGLAP Evolution Equation mapped to Duplication Loss Master Equation
* **[muse-spark-1-1_entry-025](mappings-meta-muse/muse-spark-1-1_entry-025.md)** — `Stage 1 / pending`
  * *System Synthesis:* Seismic Faults As Forgetting Synapses
  * *Domains:* Earthquake Friction Mechanics & Synaptic Plasticity Dynamics
  * *Isomorphism:* Rate And State Friction Law mapped to Tsodyks-Markram Plasticity Model

### [Microsoft Copilot](https://copilot.microsoft.com) Mapping Matrix ([`/mappings-microsoft-copilot/`](mappings-microsoft-copilot/))
* **[copilot_entry-016](mappings-microsoft-copilot/copilot_entry-016.md)** — `Stage 1 / pending`
  * *System Synthesis:* Energy‑Driven Polarization Mapping
  * *Domains:* Variational Phase‑Field Fracture & Kinetic Opinion Dynamics
  * *Isomorphism:* Variational phase‑field gradient flow mapped to nonlocal Fokker‑Planck aggregation–diffusion
* **[copilot_entry-017](mappings-microsoft-copilot/copilot_entry-017.md)** — `Stage 1 / pending`
  * *System Synthesis:* Kinked Slip‑Reconnection Analogy
  * *Domains:* Resistive Magnetohydrodynamics & Interfacial Delamination
  * *Isomorphism:* Reduced MHD reconnection operator mapped to Interfacial integro‑differential slip evolution
* **[copilot_entry-018](mappings-microsoft-copilot/copilot_entry-018.md)** — `Stage 1 / pending`
  * *System Synthesis:* Localized Influence Bifurcation
  * *Domains:* Elasto Plasticity Of Amorphous Solids & Opinion Dynamics On Weighted Social Networks
  * *Isomorphism:* Nonlocal elasto-plastic continuum (Eshelby kernel) mapped to adaptive graph-Laplacian master equation
* **[copilot_entry-019](mappings-microsoft-copilot/copilot_entry-019.md)** — `Stage 1 / pending`
  * *System Synthesis:* Graph Phase‑Field Cascades
  * *Domains:* Phase Field Fracture & Information Cascade Fronts
  * *Isomorphism:* Griffith phase-field variational method mapped to graph-cut / Laplacian gradient flow
* **[copilot_entry-020](mappings-microsoft-copilot/copilot_entry-020.md)** — `Stage 1 / pending`
  * *System Synthesis:* Turbulent Closure for Cortical Waves
  * *Domains:* Wall Bounded Turbulent Boundary Layer & Cortical Spiking Neural Field
  * *Isomorphism:* Filtered Navier–Stokes (LES Smagorinsky/Germano) mapped to Wilson–Cowan/integro-differential neural-field closures

### [Moonshot AI Kimi](https://www.kimi.com) Mapping Matrix ([`/mappings-moonshotai-kimi/`](mappings-moonshotai-kimi/))
Entries to be added later, when Kimi is no longer at capacity due to Moonshot AI's release of its version K3 model.

### [OpenAI ChatGPT](https://chatgpt.com) Mapping Matrix ([`/mappings-openai-chatgpt/`](mappings-openai-chatgpt/))
* **[gpt-5.5_entry-001](mappings-openai-chatgpt/gpt-5.5_entry-001.md)** — `Stage 1 / pending`
  * *System Synthesis:* Energy-Stable Belief Morphogenesis
  * *Domains:* Computational Morphogenesis & Bayesian Active Inference On Probabilistic Graphs
  * *Isomorphism:* Allen-Cahn Gradient Flow mapped to Variational Free-Energy Gradient Flow
* **[gpt-5.5_entry-002](mappings-openai-chatgpt/gpt-5.5_entry-002.md)** — `Stage 1 / pending`
  * *System Synthesis:* Conservative Probability Transport Across Trees
  * *Domains:* Stochastic Chemical Reaction Network Theory & Phylogenetic Sequential Monte Carlo
  * *Isomorphism:* Chemical Master Equation mapped to Sequential Monte Carlo Measure Evolution
* **[gpt-5.5_entry-003](mappings-openai-chatgpt/gpt-5.5_entry-003.md)** — `Stage 1 / pending`
  * *System Synthesis:* Geometric Stewardship Through Split Dynamics
  * *Domains:* Nonlinear Accelerator Beam Dynamics & Adaptive Ecosystem Management
  * *Isomorphism:* Lie-Algebraic Symplectic Map mapped to Discrete Intervention Operator Splitting
* **[gpt-5.5_entry-004](mappings-openai-chatgpt/gpt-5.5_entry-004.md)** — `Stage 1 / pending`
  * *System Synthesis:* Defect Transport Mirrors Belief Flow
  * *Domains:* Crystal Plasticity Dislocation Dynamics & Streaming Variational Bayesian Learning
  * *Isomorphism:* Continuum Dislocation Density Transport Equation mapped to Streaming Variational Probability Transport Equation
* **[gpt-5.5_entry-005](mappings-openai-chatgpt/gpt-5.5_entry-005.md)** — `Stage 1 / pending`
  * *System Synthesis:* Irreversible Graph Fracture Dynamics
  * *Domains:* Continuum Damage Mechanics & Bayesian Network Structure Learning
  * *Isomorphism:* Variational Phase-Field Fracture Minimization mapped to Score-Based Bayesian Network Structure Optimization

### [xAI Grok](https://grok.com) Mapping Matrix ([`/mappings-xai-grok/`](mappings-xai-grok/))
* **[grok-beta_entry-011](mappings-xai-grok/grok-beta_entry-011.md)** — `Stage 1 / pending`
  * *System Synthesis:* Quasinormal Ringing Across Spacetime and Structures
  * *Domains:* Black Hole Perturbation Theory & Structural Vibration Analysis
  * *Isomorphism:* Linearised wave operator spectrum mapped to generalised eigenvalue problem
* **[grok-beta_entry-012](mappings-xai-grok/grok-beta_entry-012.md)** — `Stage 1 / pending`
  * *System Synthesis:* Coupled Pressure-Driven Deformation Waves
  * *Domains:* Poroelasticity & Agent-based Epidemic Modeling
  * *Isomorphism:* Biot consolidation operator mapped to mean-field mobility-infection system
* **[grok-beta_entry-013](mappings-xai-grok/grok-beta_entry-013.md)** — `Stage 1 / pending`
  * *System Synthesis:* Discrete Slip in Crystals and Strategies
  * *Domains:* Crystal Plasticity & Evolutionary Game Dynamics
  * *Isomorphism:* Schmid law flow rule mapped to replicator payoff dynamics
* **[grok-beta_entry-014](mappings-xai-grok/grok-beta_entry-014.md)** — `Stage 1 / pending`
  * *System Synthesis:* Nonlocal Regularization of Softening Fronts
  * *Domains:* Nonlocal Damage Mechanics & Spatial Epidemiology
  * *Isomorphism:* Nonlocal integral operator mapped to mobility convolution kernel
* **[grok-beta_entry-015](mappings-xai-grok/grok-beta_entry-015.md)** — `Stage 1 / pending`
  * *System Synthesis:* Backward Duals for Forward Calibration
  * *Domains:* Adjoint Sensitivity Analysis & Inverse Problem Ecology
  * *Isomorphism:* Adjoint operator mapped to ecological data-misfit gradients

### [Z.AI GLM](https://chat.z.ai) Mapping Matrix ([`/mappings-zai-glm/`](mappings-zai-glm/))
* **[glm-5-2_entry-031](mappings-zai-glm/glm-5-2_entry-031.md)** — `Stage 1 / pending`
  * *System Synthesis:* Gyroscopic Destabilization of Flowing Magnetic Flux Tubes
  * *Domains:* Axially Moving Continua Mechanics & Solar Coronal Loop MHD
  * *Isomorphism:* Convective Wave Operator mapped to Thin Flux Tube MHD Equations
* **[glm-5-2_entry-032](mappings-zai-glm/glm-5-2_entry-032.md)** — `Stage 1 / pending`
  * *System Synthesis:* Topological Auxetics of Dirac Strings
  * *Domains:* Topological Structural Mechanics & Artificial Spin Ice
  * *Isomorphism:* Force Method Equilibrium Matrix mapped to Discrete Spin Flux Divergence
* **[glm-5-2_entry-033](mappings-zai-glm/glm-5-2_entry-033.md)** — `Stage 1 / pending`
  * *System Synthesis:* Spacetime Buckling of Gravitational Waves
  * *Domains:* Thin Plate Elasticity & General Relativity Colliding Waves
  * *Isomorphism:* Föppl-von Kármán Equations mapped to Szekeres Plane Wave Metric
* **[glm-5-2_entry-034](mappings-zai-glm/glm-5-2_entry-034.md)** — `Stage 1 / pending`
  * *System Synthesis:* Densification Limits of Solidification Kinetics
  * *Domains:* Stochastic Geometry Wireless Communications & Phase Transformation Kinetics Additive Manufacturing
  * *Isomorphism:* Poisson Point Process Generating Functional mapped to JMAK Extended Volume Operator
* **[glm-5-2_entry-035](mappings-zai-glm/glm-5-2_entry-035.md)** — `Stage 1 / pending`
  * *System Synthesis:* Topological Gauge Fixing of Truss Collapse
  * *Domains:* Quantum Information Science & Computational Structural Mechanics
  * *Isomorphism:* Surface Code Boundary Operator mapped to Truss Equilibrium Matrix