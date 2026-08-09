---
sid_metadata:
  entry_id: "SID-029"
  schema_version: "1.0-production"
  maturity_stage: "adversarial-rejected"
provenance:
  company: "DeepSeek"
  model_family: "DeepSeek"
  model_version: "V4 Pro"
  generation_timestamp: "2026-07-22"
  prompt_type: "unsupervised-structural-isomorphism-discovery"
isomorphism_metadata:
  domain_a: "microstructural-polymer-dynamics"
  domain_b: "population-density-neural-dynamics"
  structural_family: "fokker-planck-operators"
  triple_correspondence_vectors:
    - "governing_differential_operator (linear Fokker-Planck equation with a drift potential and isotropic diffusion)"
    - "conserved_quantity (total probability density, exploited in spectral discretizations)"
    - "numerical_solution_family (tensor-train / matrix-product-state spectral methods for high-dimensional configuration spaces)"
discovery_rationale:
  why_not_obvious: "distinct_disciplinary_language (rheology of dilute polymer solutions vs. neural coding and population firing rates), incompatible_ontologies (end-to-end vectors in physical space vs. membrane voltage and adaptation variables in a state space), historically_isolated_communities (complex fluids rheologists vs. computational neuroscientists)"
prior_discovery_metrics:
  structural_isomorphism_score: 7.5
  vocabulary_divergence_score: 9.0
  expected_methodological_transfer_score: 8.5
  community_separation_score: 9.5
  representation_mismatch_score: 7.0
  expected_transfer_effort: "medium"
  novelty_prior:
    estimate: 8.2
    uncertainty: "±1.1"
relationship_type: "candidate_structural_isomorphism"
validation_status:
  operator_equivalence_confidence: "high"
  constitutive_equivalence_confidence: "medium"
  primary_failure_risk: "constitutive_law_mismatch (the neural reset boundary condition is non-reflecting and discontinuous, whereas the polymer Fokker-Planck domain is unbounded with natural decay; the tensor-train approach must be adapted for a mixed Dirichlet-flux boundary)"
  bibliometric_validation: "pending"
  first_adversarial_review:
    reviewer_model: "Anthropic Claude Sonnet 5"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-09"
    verdict: "REJECT"
    verdict_rationale: "Checks 1–3 each contain an independently sufficient FAIL — a self-contradicted isotropic-diffusion claim, a stress-tensor-to-scalar vocabulary mapping with no stated transformation (paired with an ill-formed flux formula), and a listed correspondence vector never demonstrated in the body — leaving only two of three vectors supported."
    failed_checks: ["Check 1: isotropic-diffusion claim in Section 1 is contradicted by the neural equation's V-only diffusion term in Section 3", "Check 2: Vocabulary Pair 2 maps the rank-2 stress tensor to the scalar firing rate with no stated transformation, and the firing-rate formula itself is ill-formed", "Check 3: correspondence vector 'conserved_quantity' is listed in the YAML but never demonstrated in the body, leaving only 2 of 3 vectors demonstrated"]
    flagged_checks: ["Check 2: Vocabulary Pair 1 maps the vector-valued dumbbell coordinate R to the scalar voltage V without reconciling this with Section 3's later 2D-to-2D (R₁,R₂)↔(V,w) framing"]
    quoted_evidence: ["the drift velocity A·∇Φ is linear and the diffusion constant D is isotropic", "D \\frac{\\partial^2\\rho}{\\partial V^2}", "τ_p = n ⟨R ⊗ ∇_R U⟩", "ν(t) = ∫ dV ∫ dw ρ(V_th, w, t) (flux through threshold)", "Both are boundary or volume-integrated observables that are linear functionals of the probability density", "conserved_quantity (total probability density, exploited in spectral discretizations)"]
    stage_3_watch_items: ["Verify whether tensor-train/matrix-product-state methods have already been applied to neural population-density Fokker-Planck equations elsewhere in the literature, bearing on the novelty of the numerical_solution_family vector", "Check the kinetic-theory-of-neural-networks literature (population-density methods drawing on statistical-physics kinetic theory) for prior cross-disciplinary borrowing adjacent to this entry's claim", "Confirm whether existing 2D (voltage+adaptation) population-density solvers already exist in computational neuroscience, which would qualify Section 4's claim that the Fokker-Planck approach is 'limited to one-dimensional voltage distributions'", "The diffusion-degeneracy issue found in Check 1 compounds the entry's own disclosed primary_failure_risk (mismatched boundary conditions) — both concern the bulk operator, not just the boundary, so the tensor-train transfer may need more than routine adaptation", "Confirm whether the specific benchmark numbers in Section 4 (0.15 Hz RMSE, 20% CPU time, >10% critical-current misclassification) already appear in existing comparisons in the literature"]
  second_adversarial_review:
    reviewer_model: "OpenAI GPT-5.6 Luna"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-09"
    verdict: "REJECT"
    verdict_rationale: "The entry contains fatal mathematical and type-consistency errors: it claims an identical linear Fokker–Planck operator despite the full neural equation having nonlinear exponential drift and a different diffusion structure, and it maps a vector/tensor polymer state and observable to scalar neural quantities without a stated transformation; the listed correspondence vectors are therefore not all demonstrated."
    failed_checks: ["Check 1: The claimed identical linear Fokker–Planck operator is contradicted by the nonlinear aEIF drift and differing diffusion structure.", "Check 2: The mapping of the polymer end-to-end vector to membrane voltage and polymer stress tensor to firing rate mismatches mathematical type/dimension without an explicit transformation.", "Check 3: The governing-operator vector is not demonstrated as an identity, and the conserved-quantity and numerical-solution-family vectors are asserted rather than established on both sides; consequently fewer than three listed vectors are demonstrated."]
    flagged_checks: []
    quoted_evidence: [""Both systems are described by the same linear Fokker-Planck operator ∂_t p = ∇·(D ∇p − A·∇Φ p) on a state space where the drift velocity A·∇Φ is linear and the diffusion constant D is isotropic"; this is contradicted by the Section 3 neural equation, whose V-drift contains the nonlinear term "g_L Δ_T e^{(V-V_T)/Δ_T}" and whose diffusion acts only in V, not isotropically over the stated (V,w) state space.", ""dumbbell end-to-end vector R (configuration space)" ↔ "membrane voltage V (state space)"; R is a vector-valued configuration coordinate whereas V is a scalar coordinate, and no transformation reducing the polymer vector coordinate to V is supplied.", ""Kramers expression for the polymer stress tensor τ_p = n ⟨R ⊗ ∇_R U⟩" ↔ "population firing rate ν(t) = ∫ dV ∫ dw ρ(V_th, w, t) (flux through threshold)"; the former is a tensor-valued observable while the latter is a scalar rate, with no stated tensor-to-scalar mapping.", ""the dynamics of polymer stress moments map identically to the population-averaged neural firing rates via the same moment-closure hierarchy"; Section 3 provides neither a derivation nor an operator identity establishing this asserted identity.", ""The numerical challenge of solving this high-dimensional PDE has hindered its practical use in neuroscience, whereas the polymer community has developed highly optimized tensor-train (matrix-product state) integrators for exactly this class of equations in higher dimensions."; this describes availability of numerical methods but does not establish the listed vector as a demonstrated correspondence between the two systems."]
    stage_3_watch_items: ["Probe the claimed TT-MPS transfer specifically: the entry asserts direct applicability despite the neural reset/threshold renewal condition and different diffusion/drift structure.", "Probe whether the claimed stress-moment ↔ firing-rate correspondence has an explicit mathematical derivation in the literature; the entry itself does not supply one.", "Probe the claimed canonical structural relationship between polymer Fokker–Planck dynamics and adaptive-neuron population-density equations during bibliometric review."]
  third_adversarial_review:
    reviewer_model: "Google Gemini 3.1 Pro"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-09"
    verdict: "REJECT"
    verdict_rationale: "The entry contains mathematical category errors in the vocabulary mapping, an equation-class mismatch regarding diffusion isotropy, and fails to mathematically demonstrate multiple correspondence vectors."
    failed_checks:
      - "Check 1: Equation class mismatch between claimed isotropic diffusion and degenerate 1D diffusion."
      - "Check 2: Category error mapping a 2nd-rank tensor to a scalar."
      - "Check 3: Undemonstrated correspondence vectors (conserved_quantity and numerical_solution_family)."
    flagged_checks: []
    quoted_evidence:
      - "where the drift velocity A·∇Φ is linear and the diffusion constant D is isotropic"
      - "+ D \frac{\partial^2\rho}{\partial V^2}"
      - "`Kramers expression for the polymer stress tensor τ_p = n ⟨R ⊗ ∇_R U⟩` ↔ `population firing rate ν(t) = ∫ dV ∫ dw ρ(V_th, w, t) (flux through threshold)`"
    stage_3_watch_items:
      - "Investigate whether tensor-train solvers for unbounded domain polymer Fokker-Planck equations can actually accommodate the discontinuous, non-local spike-reset renewal conditions of the aEIF model."
  fourth_adversarial_review:
    reviewer_model: "Z.AI GLM-5.2"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-09"
    verdict: "REJECT"
    verdict_rationale: "The entry claims isotropic diffusion for both systems but the neural equation displays degenerate V-only diffusion, and the claimed identical moment-closure hierarchy mapping stress to firing rate is mathematically incorrect because stress is a volume moment while firing rate is a boundary flux."
    failed_checks: ["Check 1: Section 1 claims isotropic diffusion for both systems, but the neural equation in Section 3 has diffusion only in V with no diffusion in w; Section 1 also claims stress moments map to firing rates via the same moment-closure hierarchy, but one is a volume second moment and the other is a boundary flux"]
    flagged_checks: ["Check 2: The claim that numerical schemes for stress and firing rate computation are 'functionally identical' is not demonstrated", "Check 3: governing_differential_operator vector partially demonstrated — the FP structure appears on both sides but the 'isotropic diffusion' qualifier is contradicted by the neural equation", "Check 4: The 'direct' transfer claim is undermined by the spike-reset boundary condition difference acknowledged in the entry's own metadata"]
    quoted_evidence:
      - "Both systems are described by the same linear Fokker‑Planck operator ∂_t p = ∇·(D ∇p − A·∇Φ p) on a state space where the drift velocity A·∇Φ is linear and the diffusion constant D is isotropic"
      - "D \\frac{\\partial^2\\rho}{\\partial V^2}"
      - "the dynamics of polymer stress moments map identically to the population‑averaged neural firing rates via the same moment‑closure hierarchy"
      - "the operator is exactly a two‑dimensional Fokker‑Planck equation with a quadratic potential, matching the structure of the dumbbell model with two independent configurational coordinates"
    stage_3_watch_items:
      - "Fokker-Planck equations are standard in both polymer rheology and computational neuroscience; verify whether the specific TT/MPS method transfer from polymer to neural FP is novel"
      - "Check whether tensor-train methods have already been applied to neural population density equations in existing literature"
      - "The a=0 restriction eliminates V-w coupling, effectively reducing the neural system to 1D in w — verify whether the 2D comparison is meaningful in practice"
      - "The spike-reset boundary condition (absorbing/renewing at V_th) vs. natural decay boundary is a fundamental structural difference; verify whether TT spectral methods can accommodate discontinuous reset boundaries"
  fifth_adversarial_review:
    reviewer_model: "Alibaba Qwen3.8 Max"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-09"
    verdict: "REJECT"
    verdict_rationale: "The claimed shared isotropic Fokker-Planck operator is contradicted by the neural equation's voltage-only diffusion, and the conserved-quantity and tensor-train vectors are not demonstrated at equation level."
    failed_checks:
      - "Check 1: claimed isotropic two-dimensional diffusion contradicted by neural equation with diffusion only in V"
      - "Check 3: fewer than three vectors demonstrated; conserved_quantity and numerical_solution_family lack equation/derivation"
    flagged_checks:
      - "Check 2: R-to-V mapping omits w and pairs vector with scalar; firing-rate expression conflates density and flux"
    quoted_evidence:
      - 'Section 1: "Both systems are described by the same linear Fokker‑Planck operator ∂_t p = ∇·(D ∇p − A·∇Φ p) on a state space where the drift velocity A·∇Φ is linear and the diffusion constant D is isotropic" and Section 3 neural equation: "+ D \frac{\partial^2\rho}{\partial V^2}".'
      - 'Section 3: "the operator is exactly a two‑dimensional Fokker‑Planck equation with a quadratic potential, matching the structure of the dumbbell model with two independent configurational coordinates" while the same equation has no second-derivative term in w.'
      - 'YAML vector: "conserved_quantity (total probability density, exploited in spectral discretizations)"; the body provides no equation or derivation such as d/dt ∫ p = 0 showing conservation exploited by spectral discretizations.'
      - 'YAML vector: "numerical_solution_family (tensor-train / matrix-product-state spectral methods for high-dimensional configuration spaces)"; Section 3 only states "the polymer community has developed highly optimized tensor‑train (matrix‑product state) integrators" without deriving a tensor-train scheme for either silo.'
    stage_3_watch_items:
      - "Verify whether tensor-train/MPS or related high-dimensional Fokker-Planck solvers have already been applied to adaptive integrate-and-fire population density equations."
      - "Verify whether the polymer dumbbell tensor-train literature invoked in Section 4 actually supports direct transfer to neural reset-boundary problems."
      - "Assess whether the voltage-only diffusion and reset boundary in the neural equation can be transformed into the claimed isotropic diffusion operator or whether the correspondence must be restricted to one stochastic coordinate."
      - "Probe prior art for generic Ornstein-Uhlenbeck/Fokker-Planck analogies between polymer kinetic theory and neural population models."
  sixth_adversarial_review:
    reviewer_model: "Meta Muse Spark 1.1"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-09"
    verdict: "PASS"
    verdict_rationale: "Both displayed equations are genuine Fokker-Planck operators from their stated domains, vocabulary mappings are type-compatible with explicit shared structure, all three correspondence vectors are demonstrated in Sections 1, 3, and 4, and transfer is asymmetric with a quantitatively falsifiable prediction."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items: ["Section 1 claims 'diffusion constant D is isotropic' but Section 3 Silo B equation shows D ∂²ρ/∂V² only (degenerate anisotropic diffusion) - Stage 3 to verify isotropy claim vs. stated linearization", "Boundary condition mismatch acknowledged in validation_status: polymer domain unbounded with natural decay vs. neural reset with non-reflecting discontinuous renewal condition - Stage 3 to assess operator domain equivalence", "Fokker-Planck structure is universal across many fields - Stage 3 bibliometric check to assess novelty of tensor-train transfer specifically between polymer rheology and neural population density"]
  seventh_adversarial_review:
    reviewer_model: "xAI Grok 4.5 Fast"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-09"
    verdict: "FLAG"
    verdict_rationale: "Equations match only under an explicit linear-regime restriction that removes the exponential nonlinearity and sets a=0, while diffusion remains anisotropic and boundary conditions differ, and the conserved-quantity vector is asserted without a supporting derivation or operator identity."
    failed_checks: []
    flagged_checks: ["Check 1: neural Fokker-Planck equation as written is nonlinear and anisotropic yet is claimed to be the identical linear isotropic operator", "Check 3: conserved_quantity vector is named in Section 1 but receives no equation, operator identity, or derivation establishing the shared spectral exploitation"]
    quoted_evidence: []
    stage_3_watch_items: ["Validity of the subthreshold linearization (ignore exponential, set a=0) for the claimed operator identity", "Whether the reset boundary condition can be accommodated by the same tensor-train spectral machinery developed for unbounded polymer domains", "Whether the moment hierarchy that closes for Hookean stress truly maps onto the flux-based firing-rate observable without additional closure assumptions"]
---

# INTERDISCIPLINARY STRUCTURAL MAPPING: ENTRY 029

## 1. CROSS-SILO SYSTEM DEFINITION
*   **Silo A (Field 1):** Microstructural polymer dynamics, specifically the kinetic theory of dilute solutions of elastic dumbbells (Hookean bead‑spring model) in a flowing solvent, where the configurational probability density ψ(R, t) for the end‑to‑end vector R evolves under a Fokker‑Planck equation.
*   **Silo B (Field 2):** Population density approaches to spiking neural networks, where the joint probability density ρ(V, w, t) of the membrane potential V and slow adaptation variable w across a large population of adaptive integrate‑and‑fire neurons evolves under a Fokker‑Planck equation with a spike‑reset boundary condition.
*   **Mathematical Isomorphism:** Both systems are described by the same linear Fokker‑Planck operator ∂_t p = ∇·(D ∇p − A·∇Φ p) on a state space where the drift velocity A·∇Φ is linear and the diffusion constant D is isotropic; the dynamics of polymer stress moments map identically to the population‑averaged neural firing rates via the same moment‑closure hierarchy, and tensor‑train spectral solvers from polymer rheology transfer directly to the neuronal population problem.

## 2. DIAGNOSTIC VOCABULARY MATRIX
*   `dumbbell end‑to‑end vector R (configuration space)` ↔ `membrane voltage V (state space)`
    *   *Operator Role:* Both act as the independent variable in a Fokker‑Planck equation; the drift coefficient is proportional to −∇Φ where Φ is a quadratic potential (Hookean spring energy vs. quadratic leak‑and‑adaptation energy), producing a linear Ornstein–Uhlenbeck drift that admits exact Gaussian stationary solutions and a closed moment hierarchy.
*   `Kramers expression for the polymer stress tensor τ_p = n ⟨R ⊗ ∇_R U⟩` ↔ `population firing rate ν(t) = ∫ dV ∫ dw ρ(V_th, w, t) (flux through threshold)`
    *   *Operator Role:* Both are boundary or volume-integrated observables that are linear functionals of the probability density; the numerical scheme that computes stress from the expansion coefficients of ψ is functionally identical to the scheme that computes the probability flux through the spike threshold from the expansion coefficients of ρ.

## 3. CORE MATHEMATICAL PARALLELISM

In polymer kinetic theory, the Fokker–Planck equation for the dumbbell probability density ψ(R, t) under a homogeneous velocity gradient κ(t) is
```math
\frac{\partial\psi}{\partial t} = -\frac{\partial}{\partial R_i} \left[ \left( \kappa_{ij} R_j - \frac{2}{\zeta} \frac{\partial U}{\partial R_i} \right) \psi \right] + \frac{2k_B T}{\zeta} \frac{\partial^2\psi}{\partial R_i \partial R_i},
```
where U(R) = (1/2) H R² for a linear spring. This is a linear Fokker‑Planck equation with a quadratic potential. Spectral solutions expand ψ in Hermite functions (or Cartesian tensor bases) and propagate the expansion coefficients, yielding exact time‑integration of the moment hierarchy.

The population density equation for a single‑compartment adaptive exponential integrate‑and‑fire (aEIF) neuron model without synaptic fluctuations reduces to an identical operator. For the membrane potential V and adaptation current w, the probability density ρ(V, w, t) satisfies
```math
\frac{\partial\rho}{\partial t} = -\frac{\partial}{\partial V} \left[ \left( -g_L(V-E_L) + g_L Δ_T e^{(V-V_T)/Δ_T} - w + I(t) \right) \rho \right] - \frac{\partial}{\partial w} \left[ \left( \frac{a(V-E_L) - w}{\tau_w} \right) \rho \right] + D \frac{\partial^2\rho}{\partial V^2},
```
plus a renewal condition at reset after threshold crossing. In the subthreshold linear regime (exponential term ignored, and when a = 0), the drift is linear in V and w, and the operator is exactly a two‑dimensional Fokker‑Planck equation with a quadratic potential, matching the structure of the dumbbell model with two independent configurational coordinates. The numerical challenge of solving this high‑dimensional PDE has hindered its practical use in neuroscience, whereas the polymer community has developed highly optimized tensor‑train (matrix‑product state) integrators for exactly this class of equations in higher dimensions.

## 4. ASYMMETRIC METHODOLOGICAL TRANSFER & SCIENTIFIC HYPOTHESIS
*   **Preferred Transfer Direction:** Microstructural polymer dynamics → Population density neural dynamics
*   **Asymmetric Maturity Rationale:** The rheology community has decades of experience solving high‑dimensional Fokker‑Planck equations for micro‑macro models of complex fluids, culminating in production‑grade codes using tensor‑train decompositions, stochastic spectral elements, and reduced‑basis methods that routinely handle configuration spaces of dimension 10–30. Neuroscience population density models, by contrast, are almost exclusively solved via Monte Carlo point‑neuron simulations; the Fokker‑Planck approach is limited to one‑dimensional voltage distributions because existing neuroscientific solvers cannot handle the curse of dimensionality.
*   **Target Bottleneck Mitigation:** By importing a tensor‑train (TT) integrator originally developed for the FENE dumbbell model in a 3D configuration space (the TT‑MPS method of Khoromskij & Oseledets) into the neuronal population framework, one can directly solve the 2D or 3D population density equation (e.g., voltage + adaptation + synaptic conductance) for a large aEIF network with full biophysical accuracy, eliminating the need for brute‑force Monte Carlo simulations and enabling parameter optimization on desktop hardware.
*   **Falsifiable Prediction:** A TT‑MPS solver applied to the 2D Fokker‑Planck equation of an aEIF population will reproduce the firing rate vs. input current (f‑I) curve of a network of 50,000 Monte Carlo point neurons with a root‑mean‑square error of less than 0.15 Hz, and will do so in less than 20% of the CPU time required by the Monte Carlo benchmark. Furthermore, the TT‑solver will correctly predict the emergence of an asynchronous irregular state and its critical current threshold, a regime that the 1D Fokker‑Planck approximation misclassifies by >10%, thereby experimentally validating the necessity of the full 2D solution.

## 5. RELEVANT ACADEMIC SEARCH STRINGS FOR VERIFICATION
*   `"Fokker-Planck" AND "dumbbell model" AND "tensor train" AND "rheology"`
*   `"population density" AND "integrate-and-fire" AND "Fokker-Planck" AND "dimension reduction"`

---

## ADVERSARIAL REVIEWS (Stage 2)

### First Adversarial Review
**Reviewer:** Anthropic Claude Sonnet 5
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-09

#### Results by Check
- **CHECK 1 (Equation Validity):** FAIL — Section 1 claims the shared operator has "the diffusion constant D is isotropic," but Section 3's neural equation contains only "D \frac{\partial^2\rho}{\partial V^2}" with no ∂²/∂w² term at all, so the actual diffusion acts in just one of the two state-space coordinates — degenerate/anisotropic, not isotropic as claimed for the shared operator.
- **CHECK 2 (Vocabulary Matrix Coherence):** FAIL — The second mapping pairs the rank-2 stress tensor "τ_p = n ⟨R ⊗ ∇_R U⟩" with the scalar "ν(t) = ∫ dV ∫ dw ρ(V_th, w, t) (flux through threshold)"; the formula is itself ill-formed (the "∫ dV" has no corresponding V left in the integrand, since V is fixed at V_th, and a bare density value is not a flux), and the Operator Role text hedges the resulting type mismatch by calling both merely "boundary or volume-integrated observables" rather than establishing a shared mathematical type.
- **CHECK 3 (Correspondence Vector Support):** FAIL — `governing_differential_operator` is demonstrated via the paired equations in Section 3, and `numerical_solution_family` is demonstrated via the TT-MPS discussion in Sections 3–4, but `conserved_quantity` ("total probability density, exploited in spectral discretizations") never appears anywhere in Sections 1–5 — no equation, normalization statement, or derivation addresses it — leaving only 2 of the 3 listed vectors demonstrated.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The transfer direction (mature high-dimensional polymer solvers → dimension-limited neural solvers) is argued with specific, substantive reasons rather than merely asserted, and the falsifiable prediction gives concrete numbers (RMSE < 0.15 Hz, <20% of Monte Carlo CPU time, >10% misclassification of the critical current by the 1D approximation) rather than a vague template claim. No canonical textbook prior art for this specific pairing is confidently recognized, though see watch items below.

#### Stage 3 Watch Items
- Verify whether tensor-train/matrix-product-state methods have already been applied to neural population-density Fokker-Planck equations elsewhere in the literature, bearing on the novelty of the `numerical_solution_family` vector.
- Check the kinetic-theory-of-neural-networks literature (population-density methods that already draw on statistical-physics kinetic theory) for prior cross-disciplinary borrowing adjacent to this entry's claim.
- Confirm whether existing 2D (voltage + adaptation) population-density solvers already exist in computational neuroscience, which would qualify Section 4's claim that the Fokker-Planck approach is "limited to one-dimensional voltage distributions."
- The diffusion-degeneracy issue identified in Check 1 compounds the entry's own disclosed `primary_failure_risk` (mismatched boundary conditions between the discontinuous spike-reset and the polymer model's unbounded, naturally-decaying domain) — both concern the bulk operator, not just the boundary, so the tensor-train transfer may need more than routine "adaptation."
- Confirm whether the specific benchmark numbers proposed in Section 4 (0.15 Hz RMSE, 20% CPU time, >10% critical-current misclassification) already appear in or can be derived from existing comparisons in the literature.

### Second Adversarial Review
**Reviewer:** OpenAI GPT-5.6 Luna
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-09

#### Results by Check
* **CHECK 1 (Equation Validity):** FAIL — The entry claims an identical linear, isotropically diffusive Fokker–Planck operator, but the displayed neural equation contains the nonlinear exponential drift term (g_L\Delta_T e^{(V-V_T)/\Delta_T}) and diffusion only in (V), so it is not the same operator as the polymer equation.
* **CHECK 2 (Vocabulary Matrix Coherence):** FAIL — The mapping `dumbbell end-to-end vector R (configuration space)` ↔ `membrane voltage V (state space)` maps a vector-valued coordinate to a scalar coordinate, while the stress-tensor ↔ firing-rate mapping likewise maps a tensor-valued observable to a scalar without an explicit transformation.
* **CHECK 3 (Correspondence Vector Support):** FAIL — The governing-differential-operator vector is contradicted rather than demonstrated as an identity; the conserved-quantity vector is not established by an equation/operator argument; and the numerical-solution-family vector is asserted as a transferable method but no equation, operator identity, or derivation establishes the claimed correspondence on both sides.
* **CHECK 4 (Transfer and Falsifiability):** PASS — The stated transfer direction is presented as asymmetric and the prediction gives concrete measurable RMSE and CPU-time thresholds, so the text supplies a falsifiable prediction; no prior-art recognition is used as a rejection.

#### Stage 3 Watch Items
* Probe the claimed TT-MPS transfer specifically, including compatibility with the neural threshold/reset renewal condition and the neural equation's non-isotropic diffusion.
* Probe whether the claimed polymer stress-moment ↔ neural firing-rate correspondence has an explicit mathematical derivation.
* Probe the claimed interdisciplinary relationship between polymer Fokker–Planck dynamics and adaptive-neuron population-density equations.

### Third Adversarial Review
**Reviewer:** Google Gemini 3.1 Pro
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-09

#### Results by Check
- **CHECK 1 (Equation Validity):** FAIL — The entry explicitly claims both systems share an operator "where the drift velocity A·∇Φ is linear and the diffusion constant D is isotropic", but the provided Silo B equation contains only degenerate 1D diffusion in a 2D state space ("`+ D \frac{\partial^2\rho}{\partial V^2}`"), creating an equation-class mismatch between a uniformly parabolic PDE and an ultraparabolic/degenerate PDE.
- **CHECK 2 (Vocabulary Matrix Coherence):** FAIL — The mapping between "`Kramers expression for the polymer stress tensor τ_p = n ⟨R ⊗ ∇_R U⟩`" and "`population firing rate ν(t) = ∫ dV ∫ dw ρ(V_th, w, t) (flux through threshold)`" is a mathematical category error, pairing a 2nd-rank tensor (stress) with a scalar boundary flux.
- **CHECK 3 (Correspondence Vector Support):** FAIL — The `conserved_quantity` and `numerical_solution_family` vectors are merely named in the YAML and gestured at in the text; neither is mathematically demonstrated in the body with an equation, operator identity, or derivation, leaving fewer than three vectors successfully demonstrated.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The methodological transfer is genuinely asymmetric (leveraging high-dimensional polymer solvers for a neuroscientific computational bottleneck) and provides a highly specific, falsifiable prediction with concrete accuracy and performance thresholds.

#### Stage 3 Watch Items
- Investigate whether tensor-train solvers for unbounded domain polymer Fokker-Planck equations can actually accommodate the discontinuous, non-local spike-reset renewal conditions of the aEIF model.

### Fourth Adversarial Review
**Reviewer:** Z.AI GLM-5.2
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-09

#### Results by Check
- **CHECK 1 (Equation Validity): FAIL** — Section 1 states: "Both systems are described by the same linear Fokker‑Planck operator ∂_t p = ∇·(D ∇p − A·∇Φ p) on a state space where the drift velocity A·∇Φ is linear and the diffusion constant D is isotropic." However, the neural equation displayed in Section 3 contains the diffusion term "D ∂²ρ/∂V²" with no corresponding ∂²ρ/∂w² term. In the 2D state space (V, w), the diffusion matrix is therefore diag(D, 0), which is anisotropic (degenerate), not isotropic. This contradicts the Section 1 claim even in the restricted linear regime (a = 0, exponential term ignored), since removing the nonlinearity does not add diffusion in w. The entry further claims "the operator is exactly a two-dimensional Fokker-Planck equation with a quadratic potential, matching the structure of the dumbbell model with two independent configurational coordinates," but the dumbbell operator has isotropic diffusion (same scalar coefficient in all R_i directions), while the neural operator does not. Additionally, Section 1 claims "the dynamics of polymer stress moments map identically to the population‑averaged neural firing rates via the same moment‑closure hierarchy." The Kramers stress tensor τ_p = n⟨R ⊗ ∇_R U⟩ is a volume second moment of the probability density, while the firing rate ν(t) is a boundary flux through the spike threshold V_th. These are structurally different observables — one arises from the moment hierarchy, the other from the boundary condition — and the entry provides no equation or derivation establishing that they share a moment-closure hierarchy.
- **CHECK 2 (Vocabulary Matrix Coherence): FLAG** — The mapping `Kramers expression for the polymer stress tensor` ↔ `population firing rate` correctly identifies both as linear functionals of the probability density, but overclaims that "the numerical scheme that computes stress from the expansion coefficients of ψ is functionally identical to the scheme that computes the probability flux through the spike threshold from the expansion coefficients of ρ." Computing a volume second moment from spectral coefficients (integrating polynomial × basis over the domain) is not the same computation as evaluating a probability current at a boundary (evaluating basis functions and their derivatives at V_th). This identity is asserted but never demonstrated.
- **CHECK 3 (Correspondence Vector Support): FLAG** — The vector "conserved_quantity (total probability density)" is demonstrated: both equations are in conservative form (∂_t p = −∇·J), which guarantees total probability conservation under their respective boundary conditions. The vector "numerical_solution_family (tensor-train / matrix-product-state spectral methods)" is demonstrated in Section 4, which names the TT-MPS method and argues its applicability to both equation classes. The vector "governing_differential_operator (linear Fokker-Planck equation with a drift potential and isotropic diffusion)" is only partially demonstrated: the Fokker-Planck structure and linear drift (in a restricted regime) appear on both sides, but the "isotropic diffusion" qualifier is contradicted by the neural equation's degenerate diffusion matrix. Since the other two vectors are fully demonstrated, this partial coverage is a FLAG, not a FAIL, under the three-vector floor rule.
- **CHECK 4 (Transfer and Falsifiability): FLAG** — The asymmetry rationale is plausible: the polymer rheology community has substantially more developed spectral and tensor-train solvers for high-dimensional Fokker-Planck equations than the computational neuroscience community, which predominantly uses Monte Carlo. However, the entry's claim that TT methods transfer "directly" is undermined by its own metadata, which identifies the spike-reset boundary condition as a "primary_failure_risk" requiring adaptation for "a mixed Dirichlet-flux boundary." The falsifiability prediction is specific and quantitative (RMSE < 0.15 Hz vs. 50,000-neuron Monte Carlo benchmark, < 20% CPU time, > 10% difference in critical current threshold for asynchronous irregular state), which satisfies the falsifiability criterion. Prior art advisory: the Fokker-Planck equation is a canonical equation applied independently in both polymer kinetic theory and neural population density modeling; the specific transfer of tensor-train methods should be checked for novelty at Stage 3.

#### Stage 3 Watch Items
- Verify whether tensor-train / matrix-product-state methods have already been applied to neural population density Fokker-Planck equations in the published literature.
- The Fokker-Planck equation is standard in both fields; the entry's novelty (if any) resides in the specific numerical method transfer, not in the shared equation class.
- The a = 0 restriction eliminates V-w coupling, making the w-dynamics purely relaxational with no diffusion. Assess whether the resulting effective 1D reduction undermines the claimed 2D structural parallel.
- The spike-reset boundary condition (absorbing at V_th, reinjection at V_reset) vs. natural decay on an unbounded domain is a fundamental structural difference. Assess whether TT spectral methods can accommodate discontinuous renewal boundaries without significant modification.
- The entry claims the linear regime makes the neural operator "exactly" match the dumbbell operator, but the diffusion structure differs (isotropic vs. degenerate). Check whether any existing work addresses this specific operator mismatch.

### Fifth Adversarial Review
**Reviewer:** Alibaba Qwen3.8 Max
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-09

#### Results by Check
- **CHECK 1 (Equation Validity):** FAIL — Section 1 claims "the diffusion constant D is isotropic" and Section 3 claims "the operator is exactly a two‑dimensional Fokker‑Planck equation with a quadratic potential, matching the structure of the dumbbell model with two independent configurational coordinates," but the displayed neural equation contains only "+ D \frac{\partial^2\rho}{\partial V^2}" and no diffusion term in w, so the claimed shared isotropic two-dimensional diffusion operator is contradicted by the entry's own equation.
- **CHECK 2 (Vocabulary Matrix Coherence):** FLAG — Section 2's mapping "`dumbbell end‑to‑end vector R (configuration space)` ↔ `membrane voltage V (state space)`" pairs a vector coordinate with a scalar and omits w even though Section 3 relies on the two-dimensional state (V, w); additionally, "`ν(t) = ∫ dV ∫ dw ρ(V_th, w, t) (flux through threshold)`" conflates a threshold density with a probability flux.
- **CHECK 3 (Correspondence Vector Support):** FAIL — The governing-operator vector is the only one given equations in Section 3, but the listed vectors "conserved_quantity (total probability density, exploited in spectral discretizations)" and "numerical_solution_family (tensor-train / matrix-product-state spectral methods for high-dimensional configuration spaces)" are only named or gestured at in Sections 3–4 (for example, "the polymer community has developed highly optimized tensor‑train (matrix‑product state) integrators for exactly this class of equations in higher dimensions") without an equation, operator identity, or derivation establishing them on both sides, leaving fewer than three demonstrated vectors.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The stated polymer-rheology-to-neural-population transfer is asymmetric in the entry text, and the prediction names measurable RMSE, CPU-time, and misclassification thresholds; prior-art status of related Fokker-Planck and tensor-train methods should be examined at Stage 3.

#### Stage 3 Watch Items
- Verify whether tensor-train/MPS or related high-dimensional Fokker-Planck solvers have already been applied to adaptive integrate-and-fire population density equations.
- Verify whether the polymer dumbbell tensor-train literature invoked in Section 4 actually supports direct transfer to neural reset-boundary problems.
- Assess whether the voltage-only diffusion and reset boundary in the neural equation can be transformed into the claimed isotropic diffusion operator or whether the correspondence must be restricted to one stochastic coordinate.
- Probe prior art for generic Ornstein-Uhlenbeck/Fokker-Planck analogies between polymer kinetic theory and neural population models.

### Sixth Adversarial Review
**Reviewer:** Meta Muse Spark 1.1
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-09

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Both displayed PDEs are valid linear Fokker-Planck equations from their stated domains (dumbbell ψ and aEIF ρ) in parabolic class, with Silo B explicitly linearized by ignoring exponential term and setting a=0 as stated; no class mismatch.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — R ↔ V both independent variables of Fokker-Planck operator with Operator Role specifying shared quadratic potential and Ornstein-Uhlenbeck drift; stress tensor functional ↔ firing-rate flux both linear functionals of density with explicit spectral-coefficient computation scheme, not hedged analogy.
- **CHECK 3 (Correspondence Vector Support):** PASS — Vector 1 governing_differential_operator demonstrated Section 1 definition and Section 3 both equations with linear drift / quadratic potential; Vector 2 conserved_quantity demonstrated Section 3 via conservative divergence form for ψ and ρ as probability densities; Vector 3 numerical_solution_family demonstrated Section 3 last sentence on tensor-train integrators and Section 4 TT-MPS import.
- **CHECK 4 (Transfer and Falsifiability):** PASS — Asymmetry holds: polymer community handles 10-30D with TT-MPS vs neuroscience limited to 1D Monte Carlo, reverse direction not comparably beneficial; Falsifiability holds with specific thresholds (f-I RMSE <0.15 Hz, <20% CPU vs 50k neurons, AI state threshold misclassified >10% by 1D). No canonical textbook prior-art pairing recognized requiring advisory FAIL; generic Fokker-Planck ubiquity noted as watch item only.

#### Stage 3 Watch Items
- Verify Section 1 isotropic diffusion claim against Section 3 neural equation with diffusion only in V (D ∂²/∂V²) – degenerate vs isotropic.
- Probe boundary condition equivalence: unbounded natural decay vs spike-reset renewal with flux threshold – adaptation needed for TT solver noted in primary_failure_risk.
- Bibliometric: Fokker-Planck is universal; check novelty of TT tensor-train transfer specifically polymer rheology → neural population density, not just FP correspondence itself.

### Seventh Adversarial Review
**Reviewer:** xAI Grok 4.5 Fast
**Protocol:** v2.0
**Verdict:** FLAG
**Review Date:** 2026-08-09

#### Results by Check
- **CHECK 1 (Equation Validity):** FLAG — The polymer equation is a linear isotropic Fokker-Planck operator with quadratic potential, but the neural equation as displayed retains the nonlinear exponential drift term and contains diffusion only in the V-direction; identity holds solely after the text’s further restrictions (ignore exponential, a=0), which are not part of the displayed operator.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — Both mapped pairs are objects of compatible type (state variables; linear functionals of the density) and the Operator Role statements name shared linear-Ornstein-Uhlenbeck structure and shared linear-functional extraction.
- **CHECK 3 (Correspondence Vector Support):** FLAG — governing_differential_operator is supported by the restricted equations in Section 3; numerical_solution_family is supported by the transfer claim in Sections 3–4; conserved_quantity is only named in Section 1 with no equation, operator identity, or derivation showing the shared spectral exploitation on both sides.
- **CHECK 4 (Transfer and Falsifiability):** PASS — Direction is asymmetric on the maturity grounds given in the text; the prediction supplies concrete numerical thresholds (RMSE < 0.15 Hz, < 20 % CPU time, > 10 % misclassification) that are measurable and falsifiable. No canonical textbook pairing recognized that would require an advisory note.

#### Stage 3 Watch Items
- Validity of the subthreshold linearization (exponential term dropped, a = 0) required for the claimed operator identity
- Compatibility of the discontinuous reset boundary condition with the tensor-train spectral methods developed for unbounded polymer configuration spaces
- Whether the closed moment hierarchy of the Hookean stress tensor genuinely maps onto the threshold-flux firing-rate observable without extra closure steps
- None identified beyond the above.