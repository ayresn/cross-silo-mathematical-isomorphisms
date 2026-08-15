---
sid_metadata:
  entry_id: "SID-0031"
  schema_version: "2.0-production"
  maturity_stage: "adversarial-flagged"
provenance:
  company: "Alibaba"
  model_family: "Qwen"
  model_version: "3.8 Max"
  generation_timestamp: "2026-08-09"
  prompt_type: "unsupervised-structural-isomorphism-discovery"
isomorphism_metadata:
  domain_a: "narrow-escape-diffusion-limited-reaction-kinetics"
  domain_b: "polycrystalline-photovoltaic-carrier-lifetime"
  structural_family: "robin-first-passage-capacity-operators"
  triple_correspondence_vectors:
    - "forward_fickian_bulk_first_order_killing_semigroup"
    - "global_probability_carrier_number_balance_law"
    - "robin_radiation_surface_recombination_flux_condition"
    - "adjoint_mean_lifetime_poisson_helmholtz_green_function"
    - "small_disk_capacity_damkohler_crossover_rate"
discovery_rationale:
  why_not_obvious: "distinct_disciplinary_language / different_observables / historically_isolated_communities"
prior_discovery_metrics:
  structural_isomorphism_score: 9.2
  vocabulary_divergence_score: 7.6
  expected_methodological_transfer_score: 8.3
  community_separation_score: 7.4
  representation_mismatch_score: 6.2
  expected_transfer_effort: "low"
  novelty_prior:
    estimate: 7.1
    uncertainty: "±1.3"
relationship_type: "candidate_structural_isomorphism"
validation_status:
  operator_equivalence_confidence: "very_high"
  constitutive_equivalence_confidence: "medium"
  primary_failure_risk: "nonlinear_high_injection_or_trap_memory_breaking_first_order_robin_assumption"
  bibliometric_validation: "pending"
  first_adversarial_review:
    reviewer_model: "Anthropic Claude Sonnet 5"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-14"
    verdict: "FLAG"
    verdict_rationale: "Checks 1–3 and Check 4's asymmetry/falsifiability sub-criteria pass on internal mathematical consistency, but Check 4c recognizes the disk-capacity mathematics as paralleling existing point-contact/spreading-resistance recombination analyses in PV device physics, an advisory prior-art flag rather than a fatal flaw."
    failed_checks: []
    flagged_checks: ["Check 4c: prior-art advisory — the small-patch disk-capacity / resistances-in-series formula (Section 3's K_A(a,κ)/K_B(a,S) and the Da crossover) parallels existing point-contact and spreading-resistance recombination analyses in PV/semiconductor device physics; advisory only, not a rejection basis."]
    quoted_evidence: []
    stage_3_watch_items: ["Verify whether point-contact / local-rear-contact PV literature (e.g. PERC/PERL, passivated-contact cells with local metal openings) already applies a 4Da-type disk-capacity or Maxwell-Holm spreading-resistance formula to patch-scale recombination, independent of narrow-escape-theory terminology.", "Search for Shoup-Szabo-style resistances-in-series partially-absorbing-disk formulas (mirroring Section 3's K_A(a,κ) expression) already cited in the surface-passivation/recombination literature.", "Consider search strings beyond Section 5's list: 'spreading resistance' AND 'point contact recombination'; 'constriction resistance' AND 'surface recombination velocity'."]
  second_adversarial_review:
    reviewer_model: "DeepSeek DeepSeek V4 Pro"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-14"
    verdict: "PASS"
    verdict_rationale: "The entry's equations, operator identifications, and vocabulary mappings are internally consistent, and every listed correspondence vector is explicitly demonstrated in Section 3."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items:
      - "Probe prior art on surface recombination velocity as a Robin/radiation boundary condition and microdisk capacity formulas imported into photovoltaic lifetime extraction."
      - "Verify whether the area-averaged surface-recombination model used as the falsification baseline is the actual state-of-the-art in photovoltaic lifetime analysis."
  third_adversarial_review:
    reviewer_model: "Google Gemini 3.1 Pro"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-14"
    verdict: "PASS"
    verdict_rationale: "The mathematical mappings are perfectly physically and dimensionally consistent, operator equivalence is rigorously established across all claims, and the transfer prediction is exceptionally specific and falsifiable."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items:
      - "Verify whether the application of narrow-escape capacity formulas (e.g., from Ward, Holcman, Schuss) to minority-carrier surface recombination is genuinely novel, or if the photovoltaic community has already adopted matched-asymptotic sink formulations."
  fourth_adversarial_review:
    reviewer_model: "Xiaomi MiMo V2.5 Pro"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-14"
    verdict: "PASS"
    verdict_rationale: "All four equations sets on both sides are genuine parabolic diffusion-reaction PDEs with first-order bulk killing and Robin boundary conditions; all vocabulary mappings pair objects of identical mathematical type with explicit shared operator structure; all five listed correspondence vectors are demonstrated with full equations on both sides; and the transfer is genuinely asymmetric with a specific, numerically grounded falsifiable prediction."
    failed_checks: []
    flagged_checks: ["Check 4c: Potential prior-art recognition"]
    quoted_evidence: []
    stage_3_watch_items:
      - "The core isomorphism — Fickian diffusion with first-order bulk decay and Robin boundary patches — is textbook-level in both chemical physics (Smoluchowski/Berg-Purcell narrow-escape literature) and semiconductor device physics (minority-carrier continuity with surface recombination). The entry acknowledges this via 'distinct_disciplinary_language / different_observables / historically_isolated_communities.' Stage 3 should verify whether the specific framing as a narrow-escape capacity-law mapping to polycrystalline PV grain-boundary recombination has been explicitly published, particularly in work connecting Berg-Purcell capacity arguments to semiconductor recombination (e.g., Bhat & Düring, or PV recombination-diffusion modeling literature)."
  fifth_adversarial_review:
    reviewer_model: "Z.AI GLM-5.2"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-14"
    verdict: "PASS"
    verdict_rationale: "All four checks pass: both equation sets are parabolic diffusion-with-killing and Robin BC of the same class, all vocabulary mappings pair objects of compatible type, all five correspondence vectors are demonstrated with equations in the body, and the falsifiable prediction names specific measurable quantities with thresholds."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items: ["The basic mathematical identity between diffusion-reaction equations and minority-carrier continuity equations is standard in semiconductor device physics (cf. Haynes-Shockley, standard drift-diffusion textbooks); Stage 3 should determine whether the specific application of narrow-escape small-disk capacity formulas (4Da scaling, resistance-in-series Robin formula) to PV recombination patches is novel.", "The screened-Poisson adjoint equation for mean carrier lifetime is the backward Kolmogorov equation applied to the carrier diffusion process; Stage 3 should verify whether this specific adjoint formulation appears in the PV lifetime literature under different terminology.", "The resistance-in-series formula 1/K = 1/(πa²κ) + 1/(4Da) is a leading-order asymptotic approximation; Stage 3 should check whether higher-order corrections or alternative approximations have been used in either community that might affect the claimed isomorphism at the precision level."]
  sixth_adversarial_review:
    reviewer_model: "OpenAI GPT-5.6 Luna"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-14"
    verdict: "FLAG"
    verdict_rationale: "The governing diffusion, Robin, balance-law, adjoint, and small-patch capacity correspondences are internally consistent, but the quantitative falsifiability statement overextends a Da_B=10 threshold to Da_B>10 and the claimed radius-scaling exponent is only asymptotically near 1 rather than approximately 1 throughout that stated regime."
    failed_checks: []
    flagged_checks:
      - "Check 4: The falsification threshold 7.1 D_n a is exactly twice the stated Da_B=10 capacity prediction but is not twice the capacity prediction for general Da_B>10; the claimed log-log exponent is likewise only asymptotically 1."
    quoted_evidence: []
    stage_3_watch_items:
      - "Check 4: Probe whether the finite-reactivity small-disk resistance formula and its use as a quantitative experimental prediction are supported over the stated Da_B regime."
      - "Check 4: Verify that the claimed radius-scaling exponent near 1 is experimentally defined with S held fixed or otherwise controlled, since the displayed K_B(a,S) has a radius-dependent crossover when S is fixed."
      - "Stage 3: Probe the bibliographic record for prior interdisciplinary use of Robin/surface-recombination diffusion mappings and small-patch capacity models in semiconductor carrier-lifetime analysis."
  seventh_adversarial_review:
    reviewer_model: "Microsoft Copilot 1.2"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-14"
    verdict: "PASS"
    verdict_rationale: "All four checks pass: the paired PDEs are of the same parabolic class with consistent operator identification, the vocabulary mappings are type-consistent, every listed correspondence vector is demonstrated in the body, and the transfer claim includes an asymmetric rationale plus a concrete, falsifiable experimental prediction."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items:
      - "Verify numerical prefactors in the small-disk capacity formula and the stated inverse-sum resistance approximation (e.g., the 1/(π a^2 κ) + 1/(4 D a) form) against canonical matched-asymptotics derivations."
      - "Check experimental feasibility and parameter regimes for the falsifiability thresholds (Da_B = 10 and the 'exceeds 7.1 D_n a' cutoff) and whether measurement uncertainty could confound the proposed rejection criteria."
      - "Confirm that the assumed separation regime (well-separated, a ≪ grain length scale) and 'weak total sink capacity' conditions used to derive the τ_eff inverse-sum formula are satisfied in realistic polycrystalline samples."
      - "Probe prior-art overlap: the narrow-escape / Robin-boundary capacity analogy to carrier recombination appears canonical; Stage 3 should check for existing literature that explicitly applies microdisk capacity laws to surface recombination in photovoltaics."
      - "Examine the entry's stated primary failure risk (nonlinear high-injection or trap-memory effects) and whether the submission's linear assumptions are clearly bounded in parameter space for intended experimental tests."
  eighth_adversarial_review:
    reviewer_model: "xAI Grok 4.5 Fast"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-14"
    verdict: "PASS"
    verdict_rationale: "All four checks confirm internal mathematical consistency: identical linear parabolic operators with matching Robin conditions, compatible vocabulary types, every listed correspondence vector demonstrated by explicit equations, and a specific measurable falsifiable prediction under a justified asymmetric transfer direction."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items: []
  ninth_adversarial_review:
    reviewer_model: "Meta Muse Spark 1.1"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-14"
    verdict: "PASS"
    verdict_rationale: "All equations correctly model stated domains with matching parabolic/screend-Poisson class, vocabulary types align without category errors, all five correspondence vectors are fully demonstrated with derivations, and transfer is asymmetric with quantitative falsifiable prediction."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items: ["Underlying diffusion + first-order bulk loss + Robin boundary operator identity is textbook standard across chemical physics and semiconductor device physics; Stage 3 should focus novelty check on small-disk capacity law 4Da and Damkohler crossover applied to PV recombination patches."]
---

# INTERDISCIPLINARY STRUCTURAL MAPPING: ENTRY 0031

## 1. CROSS-SILO SYSTEM DEFINITION
*   **Silo A (Field 1):** Narrow-escape diffusion-limited reaction kinetics: Brownian reactants in a bounded microdomain with small, partially reactive boundary patches; observable is the reaction rate, survival probability, or mean first-passage/lifetime.
*   **Silo B (Field 2):** Polycrystalline photovoltaic carrier lifetime: low-injection excess minority carriers in a grain or flake with small, highly recombining surface patches; observable is the effective carrier lifetime extracted from transient photoluminescence or photoconductance decay.
*   **Mathematical Isomorphism:** In the linear low-injection limit with Fickian diffusion, first-order bulk loss, and localized Robin patches on a three-dimensional domain, the Silo A Smoluchowski survival problem and the Silo B minority-carrier continuity problem are the same self-adjoint diffusion-killing initial-boundary-value problem under the identification of radiation reactivity with surface recombination velocity, producing identical total-number balance, adjoint screened-Poisson lifetime Green’s functions, and leading-order small-disk capacity laws, provided drift, nonlinear Shockley-Read-Hall recombination, trap memory, and patch-patch interaction are negligible.

## 2. DIAGNOSTIC VOCABULARY MATRIX
*   `c_A` ↔ `Δn`
    *   *Operator Role:* Dependent scalar number density with units m^{-3} acted on by the parabolic operator `∂_t - D∇² + λ`. `c_A` is the reactant concentration in Silo A; `Δn` is the excess minority-carrier density in Silo B.
*   `λ_A` ↔ `τ_b^{-1}`
    *   *Operator Role:* Bulk first-order killing rate with units s^{-1} in the operator `D∇² - λ`. `λ_A` is homogeneous reactant decay or bulk reaction loss; `τ_b^{-1}` is the bulk minority-carrier recombination rate.
*   `Q_A` ↔ `Q_B`
    *   *Operator Role:* Integrated scalar charge/probability/carrier number, `Q = ∫_Ω q dV`, whose time derivative is the negative sum of bulk and boundary sink integrals.
*   `κ` ↔ `S`
    *   *Operator Role:* Robin coefficient with units m s^{-1} in the boundary operator `D∂_n + κ` or `D∂_n + S`. `κ` is the radiation-boundary reactivity; `S` is the surface recombination velocity.
*   `u_A` ↔ `u_B`
    *   *Operator Role:* Adjoint mean lifetime field with units s solving the screened-Poisson problem `(D∇² - λ)u = -1` with the same Robin boundary operator.
*   `G_A` ↔ `G_B`
    *   *Operator Role:* Robin Green’s function of the screened-Poisson operator, satisfying `(D∇² - λ)G = -δ` and the same homogeneous Robin boundary condition; `u` is obtained by integrating `G` over the source coordinate.
*   `K_A` ↔ `K_B`
    *   *Operator Role:* Patch rate constant with units m^3 s^{-1} in the steady flux law `J = K c_∞` or `J = K Δn_∞`; in the diffusion-limited disk limit it becomes `4Da`.
*   `Da_A` ↔ `Da_B`
    *   *Operator Role:* Dimensionless Damköhler number `κa/D_A` or `Sa/D_n` controlling the crossover from reaction-limited area scaling to diffusion-limited capacity scaling.

## 3. CORE MATHEMATICAL PARALLELISM
Silo A models the concentration of diffusing reactants in a bounded domain `Ω` with volume `V`. The domain boundary contains `M` small circular reactive patches `Γ_a` of radius `a`; outside these patches the boundary is reflecting. The reactant concentration `c_A` obeys the Smoluchowski diffusion equation with optional bulk first-order loss, while the partially reactive patches impose a radiation, or Robin, boundary condition.

```math
\frac{\partial c_A}{\partial t}
=
D_A \nabla^2 c_A - \lambda_A c_A,
\qquad x\in\Omega
```

```math
D_A \frac{\partial c_A}{\partial n} + \kappa(\mathbf{s}) c_A = 0,
\qquad \mathbf{s}\in\partial\Omega
```

Silo B models low-injection excess minority carriers in a passivated semiconductor grain or flake. The excess minority-carrier density `Δn` obeys the minority-carrier continuity equation with bulk Shockley-Read-Hall lifetime `τ_b`, and small recombination-active surface patches are represented by a local surface recombination velocity `S`. This equation and boundary condition are standard in semiconductor device physics and photovoltaic lifetime analysis.

```math
\frac{\partial \Delta n}{\partial t}
=
D_n \nabla^2 \Delta n - \frac{\Delta n}{\tau_b},
\qquad x\in\Omega
```

```math
D_n \frac{\partial \Delta n}{\partial n} + S(\mathbf{s})\Delta n = 0,
\qquad \mathbf{s}\in\partial\Omega
```

The operator identification is explicit and local:

```math
D_A = D_n,
\qquad
\lambda_A = \tau_b^{-1},
\qquad
\kappa = S,
\qquad
c_A \leftrightarrow \Delta n.
```

Under this identification the forward parabolic semigroups coincide. Integrating the forward equations over `Ω` gives the same global balance law for total reactant number `Q_A` and total excess carrier number `Q_B`:

```math
Q_A(t)=\int_\Omega c_A\,dV,
\qquad
\frac{dQ_A}{dt}
=
-\lambda_A Q_A
-
\int_{\partial\Omega}\kappa c_A\,dA
```

```math
Q_B(t)=\int_\Omega \Delta n\,dV,
\qquad
\frac{dQ_B}{dt}
=
-\frac{Q_B}{\tau_b}
-
\int_{\partial\Omega}S\Delta n\,dA
```

The adjoint mean-lifetime fields are also identical in form. In Silo A, the mean time to bulk decay or boundary absorption, starting from position `x`, satisfies the backward screened-Poisson problem with radiation boundary condition. In Silo B, the corresponding mean carrier lifetime before bulk or surface recombination satisfies the same adjoint problem with surface recombination velocity.

```math
D_A \nabla^2 u_A - \lambda_A u_A = -1,
\qquad
D_A \frac{\partial u_A}{\partial n} + \kappa u_A = 0
```

```math
D_n \nabla^2 u_B - \frac{u_B}{\tau_b} = -1,
\qquad
D_n \frac{\partial u_B}{\partial n} + S u_B = 0
```

The associated Robin Green’s functions obey the same screened-Poisson operator and boundary operator:

```math
\left(D_A\nabla^2-\lambda_A\right)G_A(x,y)=-\delta(x-y),
\qquad
D_A\frac{\partial G_A}{\partial n_y}+\kappa(y)G_A=0,
\qquad
u_A(x)=\int_\Omega G_A(x,y)\,dy
```

```math
\left(D_n\nabla^2-\tau_b^{-1}\right)G_B(x,y)=-\delta(x-y),
\qquad
D_n\frac{\partial G_B}{\partial n_y}+S(y)G_B=0,
\qquad
u_B(x)=\int_\Omega G_B(x,y)\,dy
```

The correspondence extends to the small-patch capacity law. For a single small circular absorbing or recombining disk of radius `a` on an otherwise reflecting boundary, the steady diffusion-limited flux from a far-field concentration `c_∞` or excess carrier density `Δn_∞` is governed by the microdisk capacity `4Da`. With finite surface reactivity, reaction and diffusion resistances add to leading order. In Silo A:

```math
J_A = K_A(a,\kappa)c_\infty,
\qquad
\frac{1}{K_A(a,\kappa)}
\simeq
\frac{1}{\pi a^2\kappa}
+
\frac{1}{4D_A a}
```

```math
\mathrm{Da}_A = \frac{\kappa a}{D_A},
\qquad
K_A \xrightarrow[\kappa\to\infty]{} 4D_A a
```

In Silo B, the same capacity law gives the recombination flux to a small high-velocity patch:

```math
J_{\mathrm{rec},B}=K_B(a,S)\Delta n_\infty,
\qquad
\frac{1}{K_B(a,S)}
\simeq
\frac{1}{\pi a^2 S}
+
\frac{1}{4D_n a}
```

```math
\mathrm{Da}_B = \frac{S a}{D_n},
\qquad
K_B \xrightarrow[S\to\infty]{} 4D_n a
```

For `M` well-separated patches, `a` much smaller than the grain length scale, and weak total sink capacity, the effective lifetime in Silo B is the inverse sum of bulk and patch rates:

```math
\tau_{\mathrm{eff},B}^{-1}
\simeq
\tau_b^{-1}
+
\frac{M K_B(a,S)}{V}
```

```math
\tau_{\mathrm{eff},B}^{-1}
\xrightarrow[S\gg D_n/a]{}
\tau_b^{-1}
+
\frac{4D_n M a}{V}
```

The mapping stops where the linear first-order Robin assumptions fail: strong electric-field drift, high-injection nonlinear recombination, trap-mediated memory kernels, non-Fickian transport, large patches, or closely spaced patches whose diffusion fields strongly overlap.

## 4. ASYMMETRIC METHODOLOGICAL TRANSFER & SCIENTIFIC HYPOTHESIS
*   **Preferred Transfer Direction:** narrow-escape-diffusion-limited-reaction-kinetics → polycrystalline-photovoltaic-carrier-lifetime
*   **Asymmetric Maturity Rationale:** Chemical physics and narrow-escape theory possess mature matched-asymptotic tools, boundary homogenization formulas, Brownian simulation methods, and capacity-based rate laws for sparse small Robin/Dirichlet patches on complex boundaries. Photovoltaic lifetime analysis is mature in drift-diffusion device simulation, transient optical measurement, and bulk SRH parameter extraction, but it lacks compact, geometry-aware capacity models for sparsely distributed nanoscale recombination patches; common practice either homogenizes the patches into an area-averaged surface recombination velocity or resolves them with expensive three-dimensional meshes.
*   **Target Bottleneck Mitigation:** Importing the narrow-escape capacity formula lets a photovoltaic practitioner predict the effective lifetime directly from patch radius, patch count, diffusivity, and bulk lifetime without fitting an effective surface recombination velocity. The specific hypothesis is that nanoscale recombination patches in passivated polycrystalline absorbers act as diffusion-limited capacity sinks, so the patch contribution to recombination scales with patch radius, not patch area, once the local surface reactivity exceeds the diffusion-supply limit.
*   **Falsifiable Prediction:** Prepare a benchmark sample with a known grain volume `V`, independently measured `D_n` and `τ_b`, and `M` engineered circular recombination patches of radius `a` on an otherwise passivated surface. Measure the effective lifetime `τ_eff` by time-resolved photoluminescence or microwave photoconductance decay. Define `Da_B = Sa/D_n`. The capacity model predicts that for `Da_B = 10`,

```math
K_B(Da_B=10)
=
\left(
\frac{1}{10\pi D_n a}
+
\frac{1}{4D_n a}
\right)^{-1}
=
3.55\,D_n a
```

whereas the state-of-the-art area-averaged surface-recombination model predicts

```math
K_{\mathrm{area}}
=
\pi a^2 S
=
10\pi D_n a
=
31.4\,D_n a
```

Thus the capacity model predicts a patch recombination rate smaller by a factor

```math
\frac{31.4}{3.55} \approx 8.9
```

at `Da_B = 10`, and a scaling exponent

```math
\frac{d\ln(\tau_{\mathrm{eff}}^{-1}-\tau_b^{-1})}{d\ln a} \approx 1
```

instead of the area-model exponent `2`. The prediction is falsified if, for independently characterized `D_n`, `a`, and `S` with `Da_B > 10`, the extracted patch rate exceeds `7.1 D_n a` (twice the capacity prediction) or the measured log-log slope versus patch radius exceeds `1.5` while the patches remain small and well separated.

## 5. RELEVANT ACADEMIC SEARCH STRINGS FOR VERIFICATION
*   `"narrow escape" AND "radiation boundary" AND "microdisk electrode"`
*   `"surface recombination velocity" AND "grain boundary" AND "minority carrier lifetime"`
*   `"mean first passage time" AND "surface recombination velocity" AND "grain boundary"`
*   `"narrow escape" AND "minority carrier lifetime" AND "Robin boundary"`
*   `"diffusion-limited recombination" AND "small absorbing patch" AND "photovoltaic lifetime"`

---

## ADVERSARIAL REVIEWS (Stage 2)

### First Adversarial Review
**Reviewer:** Anthropic Claude Sonnet 5
**Protocol:** v2.0
**Verdict:** FLAG
**Review Date:** 2026-08-14

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Both sides use matching linear parabolic reaction–diffusion equations (Silo A: `∂c_A/∂t = D_A∇²c_A − λ_Ac_A` with Robin BC `D_A∂c_A/∂n + κc_A = 0`; Silo B: the standard low-injection minority-carrier continuity equation with a surface-recombination-velocity Robin BC), and the downstream balance-law, adjoint-lifetime, and 4Da-limit capacity relations in Section 3 are all correctly derived and dimensionally consistent, so no equation-class mismatch or misattribution is present.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All eight Section 2 token pairs match compatible mathematical types (field↔field, rate↔rate, Robin coefficient↔Robin coefficient, dimensionless parameter↔dimensionless parameter) and each Operator Role names an explicit shared operator rather than hedged similarity language, so none of the disqualifying category-error patterns (e.g. rate-to-position, local-field-to-global-scalar) applies.
- **CHECK 3 (Correspondence Vector Support):** PASS — All five listed vectors are demonstrated with explicit equations/derivations in Section 3: `forward_fickian_bulk_first_order_killing_semigroup` (the two governing PDEs), `global_probability_carrier_number_balance_law` (the Q_A/Q_B integral identities), `robin_radiation_surface_recombination_flux_condition` (the two Robin BCs), `adjoint_mean_lifetime_poisson_helmholtz_green_function` (the u_A/u_B and G_A/G_B equations), and `small_disk_capacity_damkohler_crossover_rate` (the K(a,·) and Da expressions, further exercised quantitatively in Section 4); none is hedged as speculative in Section 1 or Section 3.
- **CHECK 4 (Transfer and Falsifiability):** FLAG — Asymmetry (4a) and falsifiability (4b) both pass: Section 4 gives a concrete experimental protocol with specific numeric thresholds (3.55 vs. 31.4 `D_na`, an ≈8.9× factor, exponent 1 vs. 2, and explicit falsification bounds of `7.1 D_na` and slope 1.5), not a template non-prediction. However, the underlying disk-capacity/resistances-in-series mathematics (Section 3's `K_A`/`K_B` formulas) is recognizable as closely paralleling existing point-contact and electrical spreading-resistance (Maxwell–Holm) analyses used for local-contact recombination in PV device physics — recorded here as advisory prior art per protocol, not as grounds for rejection.

#### Stage 3 Watch Items
- Verify whether point-contact / local-rear-contact PV literature (e.g. PERC/PERL, passivated-contact cells with local metal openings) already applies a 4Da-type disk-capacity or Maxwell–Holm spreading-resistance formula to patch-scale recombination, independent of narrow-escape-theory terminology.
- Search for Shoup–Szabo-style resistances-in-series partially-absorbing-disk formulas (mirroring Section 3's `K_A(a,κ)` expression) already cited in the surface-passivation/recombination literature.
- Consider search strings beyond Section 5's list: `"spreading resistance" AND "point contact recombination"`; `"constriction resistance" AND "surface recombination velocity"`.

### Second Adversarial Review
**Reviewer:** DeepSeek DeepSeek V4 Pro
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-14

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Both domains use the same linear parabolic diffusion-killing operator with Robin boundary conditions; the forward, adjoint, Green's function, and capacity equations are internally consistent and correctly typed.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — Each mapping pairs objects of the same mathematical type: scalar density, first-order rate, integrated scalar, Robin coefficient, lifetime field, Green's function, rate constant, and dimensionless Damköhler number.
- **CHECK 3 (Correspondence Vector Support):** PASS — All five listed vectors are explicitly demonstrated in Section 3: the forward semigroup via the identified parabolic equations, the global balance law via the integrated \(dQ/dt\) equations, the Robin flux condition via the boundary equations, the adjoint lifetime/Green's function via the screened-Poisson equations, and the small-disk capacity/Damköhler crossover via the \(J=K c_\infty\) formulas.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The transfer direction is asymmetric as justified by source-side capacity-model maturity versus target-side lack of compact geometry-aware capacity models; the prediction gives measurable thresholds (\(K_B > 7.1 D_n a\), log-log slope \(>1.5\)) and is falsifiable. Prior-art recognition is advisory only.

#### Stage 3 Watch Items
- Probe whether surface recombination velocity as a Robin/radiation boundary condition and microdisk capacity formulas have already been explicitly imported into photovoltaic lifetime extraction.
- Verify whether the area-averaged surface-recombination model used as the falsification baseline is the true state-of-the-art for patchy recombination in photovoltaic lifetime analysis.

### Third Adversarial Review
**Reviewer:** Google Gemini 3.1 Pro
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-14

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — All governing equations, boundary conditions, global balance laws, and adjoint derivations match perfectly in class (parabolic forward, elliptic adjoint), structure, and dimension.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — The matrix establishes precise 1:1 correspondences without category errors, explicitly detailing equivalent operator roles and units.
- **CHECK 3 (Correspondence Vector Support):** PASS — All five claimed correspondence vectors (forward semigroup, global balance law, Robin boundary flux, adjoint Green's function, small-disk capacity crossover) are explicitly and completely demonstrated with valid equations in Section 3.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The transfer direction is well-justified based on asymmetric methodological maturity, and the prediction is exceptionally robust, supplying a quantifiable, numerically specific threshold to falsify the hypothesis (a scaling exponent of ~1 vs. 2, and defined deviation bounds at $Da_B > 10$).

#### Stage 3 Watch Items
- Verify whether the application of narrow-escape capacity formulas (e.g., from Ward, Holcman, Schuss) to minority-carrier surface recombination is genuinely novel, or if the photovoltaic community has already adopted matched-asymptotic sink formulations.

### Fourth Adversarial Review
**Reviewer:** Xiaomi MiMo V2.5 Pro
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-14

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Both Silo A and Silo B equations are genuine parabolic diffusion-reaction PDEs with first-order bulk loss and Robin boundary conditions; the operator identification D_A = D_n, λ_A = τ_b⁻¹, κ = S is explicit and consistent across all equation pairs including the forward IBVP, global balance laws, adjoint screened-Poisson problems, Green's functions, and small-disk capacity laws.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All eight paired mappings (c_A ↔ Δn, λ_A ↔ τ_b⁻¹, Q_A ↔ Q_B, κ ↔ S, u_A ↔ u_B, G_A ↔ G_B, K_A ↔ K_B, Da_A ↔ Da_B) pair objects of identical mathematical type with matching units, and each Operator Role specifies the exact shared operator or functional structure rather than hedged similarity language.
- **CHECK 3 (Correspondence Vector Support):** PASS — All five listed vectors are fully demonstrated: (1) forward semigroup by the two parabolic IBVPs and operator identification; (2) global balance law by the two dQ/dt equations; (3) Robin flux condition by the two boundary conditions; (4) adjoint Green's function by the two screened-Poisson problems and Green's function definitions; (5) small-disk capacity/Damköhler crossover by the resistance-in-series capacity formulas and limiting behaviors on both sides.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The transfer direction (narrow-escape theory → PV carrier lifetime) is genuinely asymmetric: chemical physics possesses matched-asymptotic capacity tools that PV analysis lacks for sparse patch geometries. The falsifiable prediction is specific and quantitative: at Da_B = 10, the capacity model yields K_B ≈ 3.55 D_n a versus the area-averaged model's 31.4 D_n a (verified by independent calculation), with explicit falsification thresholds (patch rate > 7.1 D_n a or log-log slope > 1.5). Prior-art advisory: the underlying PDE structure (Fickian diffusion + bulk decay + Robin BC) is canonical in both chemical physics and semiconductor device physics; Stage 3 should verify whether the specific narrow-escape capacity-law framing for PV grain boundaries has been explicitly published.

#### Stage 3 Watch Items
- The isomorphism maps two applications of the same well-known PDE class (parabolic diffusion-killing with Robin patches). The entry's claim to novelty rests on the disciplinary-language gap rather than mathematical novelty. Stage 3 should probe the boundary between "well-known equation applied in two fields" and "explicitly published structural mapping," particularly in the Berg-Purcell / narrow-escape / semiconductor recombination intersection literature.
- The entry's own `primary_failure_risk` field acknowledges that nonlinear high-injection or trap memory breaks the first-order Robin assumption. Stage 3 should verify whether the low-injection linear regime restriction is standard practice in the target field or whether it significantly narrows practical applicability.

### Fifth Adversarial Review
**Reviewer:** Z.AI GLM-5.2
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-14

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Both Silo A (`∂c_A/∂t = D_A∇²c_A − λ_Ac_A`) and Silo B (`∂Δn/∂t = D_n∇²Δn − Δn/τ_b`) are forward parabolic diffusion-with-first-order-killing equations, both paired with identical Robin boundary conditions (`D∂_n + κ` vs. `D∂_n + S`). The adjoint equations are screened-Poisson (elliptic) of identical form. No equation-class mismatch; the operator identification `D_A = D_n, λ_A = τ_b^{-1}, κ = S` is mathematically sound and the capacity law `1/K ≈ 1/(πa²κ) + 1/(4Da)` is the correct leading-order asymptotic for a partially absorbing small disk on a reflecting boundary in 3D. The numerical verification at `Da_B = 10` (K_B ≈ 3.55 D_n a vs. K_area = 31.4 D_n a, ratio ≈ 8.9) is arithmetically correct.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All eight vocabulary pairs map objects of compatible mathematical type: scalar density ↔ scalar density (`c_A ↔ Δn`), rate ↔ rate (`λ_A ↔ τ_b^{-1}`), Robin coefficient ↔ Robin coefficient (`κ ↔ S`), integrated number ↔ integrated number (`Q_A ↔ Q_B`), adjoint field ↔ adjoint field (`u_A ↔ u_B`), Green's function ↔ Green's function (`G_A ↔ G_B`), rate constant ↔ rate constant (`K_A ↔ K_B`), dimensionless parameter ↔ dimensionless parameter (`Da_A ↔ Da_B`). Each Operator Role explanation names the shared mathematical structure (e.g., "Robin coefficient with units m s^{-1} in the boundary operator `D∂_n + κ`") rather than relying on hedged analogy.
- **CHECK 3 (Correspondence Vector Support):** PASS — All five listed vectors are demonstrated in the body with equations: (1) `forward_fickian_bulk_first_order_killing_semigroup` — forward parabolic equations and explicit operator identification in Section 3; (2) `global_probability_carrier_number_balance_law` — integrated balance laws for Q_A and Q_B; (3) `robin_radiation_surface_recombination_flux_condition` — Robin boundary conditions for both silos; (4) `adjoint_mean_lifetime_poisson_helmholtz_green_function` — adjoint screened-Poisson equations and Green's function equations for both silos; (5) `small_disk_capacity_damkohler_crossover_rate` — capacity law formulas, Damköhler numbers, and asymptotic limits for both silos, plus the effective lifetime formula.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The transfer direction (narrow-escape → PV) is genuinely asymmetric: narrow-escape theory possesses matched-asymptotic capacity formulas for sparse Robin patches that PV lifetime analysis lacks, instead homogenizing or mesh-resolving. The falsifiable prediction is specific and measurable: it names a benchmark sample geometry, a measurement technique (TRPL or microwave photoconductance decay), a quantitative threshold (extracted patch rate exceeding 7.1 D_n a at Da_B > 10, or log-log slope vs. patch radius exceeding 1.5), and a clear outcome that would falsify the capacity model. Prior-art recognition: the underlying mathematical identity between diffusion-with-absorption and minority-carrier continuity is standard in semiconductor device physics; the specific importation of narrow-escape capacity formulas into PV lifetime analysis is the claimed novelty and should be verified at Stage 3.

#### Stage 3 Watch Items
- The basic mathematical identity between diffusion-reaction equations and minority-carrier continuity equations is standard in semiconductor device physics (cf. Haynes-Shockley experiment, standard drift-diffusion textbook treatments). Stage 3 should determine whether the specific application of narrow-escape small-disk capacity formulas (the `4Da` scaling and resistance-in-series Robin formula) to nanoscale PV recombination patches is novel against the published record.
- The screened-Poisson adjoint equation for mean carrier lifetime is the backward Kolmogorov equation for the diffusion-with-killing process; Stage 3 should verify whether this adjoint formulation appears in the PV lifetime literature under different terminology (e.g., "lifetime mapping," "recombination probability function").
- The resistance-in-series formula `1/K = 1/(πa²κ) + 1/(4Da)` is a leading-order asymptotic for small `a`; Stage 3 should check whether higher-order corrections or alternative approximation schemes have been published in either community that might qualify the precision of the claimed isomorphism.

### Sixth Adversarial Review
**Reviewer:** OpenAI GPT-5.6 Luna
**Protocol:** v2.0
**Verdict:** FLAG
**Review Date:** 2026-08-14

#### Results by Check
* **CHECK 1 (Equation Validity):** PASS — The forward diffusion-killing equations, Robin conditions, integrated balance laws, adjoint screened-Poisson equations, Green's functions, and small-patch capacity formulas are mutually consistent with the stated linear low-injection/Fickian assumptions.
* **CHECK 2 (Vocabulary Matrix Coherence):** PASS — The paired quantities have compatible mathematical types and the Operator Role descriptions identify explicit shared operators, coefficients, state variables, or dimensionless groups rather than relying solely on analogy.
* **CHECK 3 (Correspondence Vector Support):** PASS — The forward Fickian killing semigroup is established by the operator identification in Section 3; the global number balance by the two integrated balance equations; the Robin surface condition by the paired boundary equations; the adjoint lifetime/Green-function correspondence by the paired screened-Poisson and Green-function equations; and the small-disk capacity/Damköhler crossover by the paired capacity and Damköhler formulas in Section 3.
* **CHECK 4 (Transfer and Falsifiability):** FLAG — The transfer direction is presented as genuinely asymmetric, and the prediction is experimentally measurable, but the statement that `7.1 D_n a` is “twice the capacity prediction” is valid only at `Da_B=10`, not generally for `Da_B>10`, while the claimed radius exponent near 1 is an asymptotic diffusion-limited result rather than the exact exponent of the displayed finite-reactivity formula throughout the stated regime.

#### Stage 3 Watch Items
* Probe whether the displayed finite-reactivity disk resistance formula is supported quantitatively over the proposed experimental `Da_B` range.
* Verify how the radius-scaling experiment controls `S`; with `S` fixed, the displayed finite-reactivity expression has a crossover exponent rather than exactly 1 at finite `Da_B`.
* Probe the bibliographic record for prior interdisciplinary use of Robin/partially absorbing diffusion and surface-recombination boundary mappings in semiconductor carrier-lifetime analysis.

### Seventh Adversarial Review
**Reviewer:** Microsoft Copilot 1.2
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-14

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — The forward parabolic PDEs and Robin boundary conditions in Section 3 are of the same class and the entry explicitly identifies \(D_A=D_n,\ \lambda_A=\tau_b^{-1},\ \kappa=S,\ c_A\leftrightarrow\Delta n\), supporting the claimed shared semigroup and operator structure.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — Each mapped token pair (e.g., **`c_A` ↔ `Δn`**, **`λ_A` ↔ `τ_b^{-1}`**, **`κ` ↔ `S`**) are the same mathematical object type (scalar fields, rates, Robin coefficients) and the Operator Role descriptions specify identical operator action.
- **CHECK 3 (Correspondence Vector Support):** PASS — All five listed vectors are demonstrated in the body:  
  - **forward_fickian_bulk_first_order_killing_semigroup** — shown by the paired parabolic PDEs and explicit operator identification (Section 3, forward equations).  
  - **global_probability_carrier_number_balance_law** — shown by the integrated balance laws for \(Q_A\) and \(Q_B\) (Section 3, integrated equations).  
  - **robin_radiation_surface_recombination_flux_condition** — shown by the Robin BCs for both silos (Section 3, boundary conditions).  
  - **adjoint_mean_lifetime_poisson_helmholtz_green_function** — shown by the screened-Poisson adjoint problems and Robin Green’s functions (Section 3, adjoint and Green’s function equations).  
  - **small_disk_capacity_damkohler_crossover_rate** — shown by the small-patch capacity expressions, Damköhler number definitions, and limiting forms (Section 3, capacity laws). Each vector is supported by equations or asymptotic relations in the text.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The transfer direction is plausibly asymmetric (narrow-escape asymptotics → compact photovoltaic capacity models) and the entry supplies a concrete, measurable falsifiable prediction with numerical thresholds and an experimental protocol; this satisfies falsifiability rather than a non-specific claim. Prior-art similarity is noted as a Stage 3 watch item.

#### Stage 3 Watch Items
- Verify the matched-asymptotic derivation and numerical prefactors in the small-disk capacity inverse-sum formula.
- Assess experimental uncertainty and parameter ranges for the proposed falsification thresholds (Da_B = 10 and the 7.1 \(D_n a\) cutoff).
- Confirm the validity of the well-separated, small-patch, weak-sink approximations in realistic polycrystalline geometries.
- Check for prior literature explicitly applying narrow-escape capacity formulas to photovoltaic surface recombination (advisory).
- Evaluate the practical boundary between the linear regime assumed here and nonlinear/high-injection or trap-memory regimes flagged as primary failure risks.

### Eighth Adversarial Review
**Reviewer:** xAI Grok 4.5 Fast
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-14

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Both sides are the identical linear parabolic diffusion-killing equation with Robin boundary operator; the displayed forward, balance, adjoint screened-Poisson, Green’s-function and capacity formulae are consistent with the claimed domains and support the structural identity under the stated identification.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — Every paired token is of matching mathematical type (scalar density, rate, integrated number, Robin coefficient, lifetime field, Green’s function, rate constant, Damköhler number) and the Operator Role statements name the shared structure without hedging.
- **CHECK 3 (Correspondence Vector Support):** PASS — All five listed vectors are demonstrated by explicit equations or operator identities in Section 3: the forward Fickian killing semigroup, the global number balance law, the Robin flux condition, the adjoint mean-lifetime screened-Poisson/Green’s function, and the small-disk capacity/Damköhler crossover.
- **CHECK 4 (Transfer and Falsifiability):** PASS — Transfer direction is asymmetrically justified by the source field’s mature capacity asymptotics versus the target’s reliance on area-averaged or fully numerical treatments; the prediction supplies concrete numerical thresholds (factor ≈8.9, slope 1 vs 2, falsification bounds 7.1 D_n a and 1.5) that are experimentally measurable.

#### Stage 3 Watch Items
None identified.

### Ninth Adversarial Review
**Reviewer:** Meta Muse Spark 1.1
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-14

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Both sides display identical self-adjoint parabolic operator ∂_t - D∇² + λ with Robin boundary operator D∂_n + κ/S, correctly modeling diffusion-limited reaction and low-injection carrier continuity with no class mismatch or misattribution.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All eight pairs (c_A↔Δn, λ_A↔τ_b^{-1}, Q_A↔Q_B, κ↔S, u_A↔u_B, G_A↔G_B, K_A↔K_B, Da_A↔Da_B) are compatible types with explicit shared mathematical structure in Operator Role, no spatial/temporal or dimensional category errors.
- **CHECK 3 (Correspondence Vector Support):** PASS — All five listed vectors demonstrated in Section 3: forward_fickian_bulk_first_order_killing_semigroup via forward PDEs, global_probability_carrier_number_balance_law via dQ/dt balance laws, robin_radiation_surface_recombination_flux_condition via Robin BCs, adjoint_mean_lifetime_poisson_helmholtz_green_function via D∇²u-λu=-1 and (D∇²-λ)G=-δ, small_disk_capacity_damkohler_crossover_rate via 1/K≈1/(πa²κ)+1/(4Da) and Da=κa/D and τ_eff^{-1}≈τ_b^{-1}+MKB/V.
- **CHECK 4 (Transfer and Falsifiability):** PASS — Asymmetry narrow-escape → PV justified by mature matched-asymptotic capacity tools lacking in PV patch modeling; falsifiable prediction gives specific measurable rates K_B=3.55 D_n a vs K_area=31.4 D_n a (factor 8.9), exponent 1 vs 2, and falsification thresholds 7.1 D_n a and slope 1.5 at Da_B>10; no template non-prediction. Prior-art advisory only: underlying diffusion+Robin identity is standard textbook material.

#### Stage 3 Watch Items
- Underlying operator identity (Fickian diffusion + first-order bulk loss + Robin boundary) is textbook standard in chemical kinetics and semiconductor device physics; Stage 3 bibliometric novelty assessment should focus on the specific application of narrow-escape small-disk capacity law K→4Da and Damköhler crossover to polycrystalline photovoltaic recombination patches.
- Verify experimental feasibility of benchmark with engineered M patches and independent S characterization to distinguish capacity scaling (radius) from area-averaged scaling.