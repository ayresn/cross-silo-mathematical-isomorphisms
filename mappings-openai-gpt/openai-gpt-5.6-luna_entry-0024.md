---
sid_metadata:
  entry_id: "SID-0024"
  schema_version: "2.0-production"
  maturity_stage: "adversarial-flagged"
provenance:
  company: "OpenAI"
  model_family: "GPT"
  model_version: "5.6 Luna"
  generation_timestamp: "2026-08-10"
  prompt_type: "unsupervised-structural-isomorphism-discovery"
isomorphism_metadata:
  domain_a: "dendritic-metal-solidification"
  domain_b: "ice-lens-growth-in-frost-heave"
  structural_family: "moving-phase-boundary-and-capillary-regularized-free-boundary-growth"
  triple_correspondence_vectors:
    - "Gibbs-Thomson-curvature-corrected-interface-temperature"
    - "Stefan-latent-heat-interface-balance"
    - "diffusion-field-similarity-parameter"
discovery_rationale:
  why_not_obvious: "distinct_disciplinary_language / historically_isolated_communities / porous-soil-versus-metallurgical-ontology"
prior_discovery_metrics:
  structural_isomorphism_score: 8.1
  vocabulary_divergence_score: 8.8
  expected_methodological_transfer_score: 8.5
  community_separation_score: 8.7
  representation_mismatch_score: 7.9
  expected_transfer_effort: "medium"
  novelty_prior:
    estimate: 7.4
    uncertainty: "±1.3"
relationship_type: "candidate_structural_isomorphism"
validation_status:
  operator_equivalence_confidence: "high"
  constitutive_equivalence_confidence: "medium"
  primary_failure_risk: "constitutive_law_mismatch"
  bibliometric_validation: "pending"
  first_adversarial_review:
    reviewer_model: "Anthropic Claude Sonnet 5"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-14"
    verdict: "FLAG"
    verdict_rationale: "Every equation, vocabulary pairing, and correspondence vector is mathematically sound with no class mismatch, misattribution, or undemonstrated vector, but one vocabulary label misnames a dimensionless parameter as a length and the domain pairing matches literature Stage 3 should verify."
    failed_checks: []
    flagged_checks: ["Check 2: vocabulary item 3 ('thermal diffusion length' <-> 'frost-heave thermal diffusion length') is labeled as a length scale, but its own Operator Role text and the Section 3 derivation construct and use the dimensionless Peclet-type similarity parameter Pe = VR/alpha, matching the YAML vector name 'diffusion-field-similarity-parameter' rather than a length.", "Check 4c: prior art (advisory only) - this domain pairing (curvature/Gibbs-Thomson premelting physics linking solidification and frost heave) resembles a recognized line of work in the premelting-dynamics literature; not used as grounds for rejection."]
    quoted_evidence: []
    stage_3_watch_items: ["Bibliometric check against the premelting-dynamics literature connecting frost heave to solidification/crystal-growth theory via curvature (Gibbs-Thomson) effects on interfacial equilibrium temperature, a line of work associated with authors such as Wettlaufer, Worster, and Rempel on continuum frost-heave models; confirm whether this entry's specific three-vector packaging is already published.", "Reconcile the Section 2 vocabulary item 3 label ('thermal diffusion length') with the dimensionless similarity parameter (Peclet number) it actually denotes in Section 3 and in the YAML vector name 'diffusion-field-similarity-parameter'."]
  second_adversarial_review:
    reviewer_model: "Alibaba Qwen 3.8 Max"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-14"
    verdict: "FLAG"
    verdict_rationale: "The displayed equations and correspondence vectors are internally consistent, but the Gibbs-Thomson/Stefan moving-boundary analogy is recognizable prior art and should be checked in Stage 3."
    failed_checks: []
    flagged_checks: ["Check 4: prior-art advisory for Section 1 and Section 3's claim of a shared Gibbs-Thomson/Stefan moving-boundary structure between dendritic solidification and frost-heave ice-lens growth."]
    quoted_evidence: []
    stage_3_watch_items: ["Verify whether dendritic-solidification phase-field or sharp-interface methods have already been applied to ice-lens growth or freezing-soil models.", "Check whether the Peclet-number similarity and Stefan/Gibbs-Thomson pairing is treated as canonical in phase-change textbooks or reviews, e.g. classical Stefan-problem literature.", "Confirm whether frost-heave literature represents ice-interface curvature effects using the same Gibbs-Thomson form displayed here or through pressure/premelting-film closures."]
  third_adversarial_review:
    reviewer_model: "DeepSeek DeepSeek V4 Pro"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-14"
    verdict: "PASS"
    verdict_rationale: "The displayed equations are internally consistent, the vocabulary pairs are type-compatible, and all three listed correspondence vectors are explicitly derived or equated in the body."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items:
      - "Probe whether the Gibbs-Thomson/Stefan sharp-interface mapping between metal solidification and frost-heave ice-lens growth is already established in geocryology or solidification literature."
      - "Check whether the omitted kinetic undercooling term (beta V_n) has a frost-heave counterpart in premelting or kinetic interface laws, and whether its omission affects the claimed capillary-limit isomorphism."
      - "Verify that the local Stefan heat-flux balance for ice-lens growth remains valid once full poromechanical/hydraulic closures are included."
  fourth_adversarial_review:
    reviewer_model: "Google Gemini 3.1 Pro"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-14"
    verdict: "FLAG"
    verdict_rationale: "The mathematical correspondences are rigorously supported, but the structural isomorphism is a canonical textbook identity (freezing of water versus freezing of metal are both classical Stefan problems)."
    failed_checks: []
    flagged_checks: ["Check 4c: Prior art recognized (The Stefan problem originated in ice formation and its equivalence to metal solidification is canonical)."]
    quoted_evidence: []
    stage_3_watch_items: ["Investigate the novelty of applying curvature-regularized phase-field/moving-boundary solvers to frost heave, as phase-field models for ice lenses in porous media already exist in the geophysics literature.", "Check whether the equivalence is too trivial (ice freezing vs. metal freezing) to constitute a structural discovery, as both are instances of the exact same physical mechanism."]
  fifth_adversarial_review:
    reviewer_model: "Xiaomi MiMo V2.5 Pro"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-14"
    verdict: "PASS"
    verdict_rationale: "All three correspondence vectors are demonstrated with explicit equations of compatible class and type, the transfer direction is genuinely asymmetric, and the falsifiable prediction names specific measurable thresholds and falsification conditions."
    failed_checks: []
    flagged_checks: ["Check 4c: Prior-art advisory — the Gibbs-Thomson + Stefan moving-boundary analogy between dendritic solidification and ice-lens growth is a well-established pairing in the cold-regions and solidification communities"]
    quoted_evidence: []
    stage_3_watch_items:
      - "Prior art: The Gibbs-Thomson / Stefan moving-boundary isomorphism between metal solidification and ice-lens frost heave is discussed in Worster's mushy-zone work and in phase-field studies of ice growth (e.g., Rycroft and collaborators). The human reviewer should verify whether the specific claim of novelty — that the local ice-lens morphology has not been systematically treated as a capillary-regularized moving boundary resolved by imported metallurgical solvers — is supported by the bibliometric record."
      - "Vocabulary matrix item 3 names the mapped quantity as 'thermal diffusion length' but the Operator Role and Section 3 describe the Péclet number (a dimensionless ratio). While the mathematical content in Section 3 is unambiguous and correct, the human reviewer may wish to confirm whether 'thermal diffusion length' is the conventional term in either community for the Pe similarity parameter, or whether this is a terminology artifact."
  sixth_adversarial_review:
    reviewer_model: "Z.AI GLM-5.2"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-14"
    verdict: "PASS"
    verdict_rationale: "All four checks pass: both equation sets are parabolic diffusion equations with Stefan/Gibbs-Thomson moving-boundary conditions of the same operator class, all three vocabulary mappings name shared mathematical structure between compatible types, every listed correspondence vector is demonstrated with explicit equations in the body, and the falsifiable prediction names a specific measurable convergence threshold with explicit falsification conditions."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items: ["The Stefan problem with Gibbs-Thomson curvature regularization is textbook material in both solidification physics and ice/cryosphere physics individually; Stage 3 should verify whether the specific cross-domain pairing of dendritic-metal-solidification with frost-heave-ice-lens-growth has been explicitly published as an isomorphism.", "The entry explicitly excludes the kinetic undercooling term βV_n from the frost-heave side and scopes the isomorphism to the local sharp-interface limit only; Stage 3 should verify whether frost-heave models in the literature typically include or omit kinetic undercooling, as this scoping choice materially affects the claimed correspondence breadth."]
  seventh_adversarial_review:
    reviewer_model: "Microsoft Copilot 1.2"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-14"
    verdict: "PASS"
    verdict_rationale: "The entry presents mathematically consistent parabolic diffusion equations, matching curvature-corrected interfacial conditions, a Stefan flux balance, and a clear nondimensional Pe mapping; all three listed correspondence vectors are demonstrated and the transfer claim is falsifiable."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items:
      - "Verify prior-art overlap between solidification Stefan/Gibbs-Thomson mappings and frost-heave literature (search for explicit prior isomorphisms)."
      - "Examine constitutive closures outside the local interface (soil hydraulic and poromechanical laws) to ensure they do not implicitly break the assumed local isomorphism when coupled numerically."
      - "Confirm numerical implementation details for the proposed benchmark (definition of 'interface-resolution length' and baseline discretization) to ensure the 1%/5% thresholds are operationally meaningful."
  eighth_adversarial_review:
    reviewer_model: "xAI Grok 4.5 Fast"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-14"
    verdict: "PASS"
    verdict_rationale: "All four checks pass: equations are class-consistent free-boundary Stefan systems with matching operators, vocabulary pairs share mathematical type and structure, all three listed vectors are demonstrated by explicit operator identities in Section 3, and the transfer is asymmetric with a quantitative falsifiable prediction."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items: ["Confirm whether the local capillary-regularized Stefan reduction for ice-lens growth is already standard in the frost-heave literature or remains under-developed relative to dendritic solidification solvers."]
  ninth_adversarial_review:
    reviewer_model: "Meta Muse Spark 1.1"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-14"
    verdict: "PASS"
    verdict_rationale: "All three correspondence vectors are demonstrated with compatible parabolic Stefan-Gibbs-Thomson operator structure, vocabulary types are mathematically compatible, and asymmetric falsifiable transfer is specified."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items: ["Both sides are standard Gibbs-Thomson-regularized Stefan problems; Stage 3 should verify whether this specific material pairing is already documented as the same operator in free-boundary texts/reviews (e.g., Alexiades & Solomon Mathematical Modeling of Melting and Freezing, Davis Theory of Solidification).", "Verify bibliometrically whether transfer of curvature-regularized adaptive/phase-field solvers to frost-heave ice-lens morphology has already been published."]
---

# INTERDISCIPLINARY STRUCTURAL MAPPING: ENTRY 0024

## 1. CROSS-SILO SYSTEM DEFINITION

* **Silo A (Field 1):** Dendritic metal solidification, specifically diffusion-controlled growth of a solid-liquid interface with capillary/Gibbs-Thomson regularization.
* **Silo B (Field 2):** Ice-lens growth during frost heave, specifically the local advance of an ice-water interface supplied by diffusive heat/mass transport in a porous soil matrix.
* **Mathematical Isomorphism:** Under a local sharp-interface reduction in which the interfacial temperature is represented by a curvature-corrected Gibbs-Thomson condition, the latent-heat/phase-change balance is represented by a Stefan condition, and transport is nondimensionalized by the same diffusion-field similarity parameter, both systems possess the same moving-boundary operator structure even though their constitutive closures and physical driving fields differ.

## 2. DIAGNOSTIC VOCABULARY MATRIX

* **Gibbs-Thomson temperature** ↔ **ice-interface equilibrium temperature**

  * *Operator Role:* Both are scalar interfacial boundary fields entering a curvature-dependent Dirichlet condition for the temperature/diffusion field. The shared mathematical type is a scalar boundary value, with curvature supplying the geometric correction.

* **Stefan condition** ↔ **ice-lens latent-heat balance**

  * *Operator Role:* Both impose a normal-velocity boundary constraint equating latent-energy consumption to the jump in normal conductive heat flux. The shared mathematical type is a scalar flux-balance condition on the moving interface.

* **thermal diffusion length** ↔ **frost-heave thermal diffusion length**

  * *Operator Role:* Both normalize the diffusion equation through a moving-interface similarity variable, producing the dimensionless ratio of interface velocity to diffusive transport.

## 3. CORE MATHEMATICAL PARALLELISM

In dendritic solidification, the temperature field in each phase is commonly represented by a diffusion equation, while the interface is advanced through a Stefan balance. A curvature-dependent Gibbs-Thomson relation supplies capillary regularization of the otherwise ill-posed sharp-interface growth problem:

```math
\frac{\partial T}{\partial t}
=
\alpha \nabla^2 T,
\qquad
T_i=T_m-\Gamma\kappa-\beta V_n,
\qquad
\rho L V_n
=
k_s\partial_nT_s-k_l\partial_nT_l .
```

Here (T_i) is the interfacial temperature, (T_m) the planar equilibrium melting temperature, (\Gamma) the Gibbs-Thomson capillary coefficient, (\kappa) interface curvature, (V_n) normal interface velocity, (L) latent heat per unit mass, and (k_s,k_l) the thermal conductivities of solid and liquid. The first equation establishes the transport operator; the second establishes curvature regularization; and the third establishes the phase-change flux balance.

For frost-heave ice-lens growth, the local temperature field in the unfrozen/frozen regions can likewise be reduced to diffusion with a moving ice-water interface. The interfacial equilibrium temperature is curvature-sensitive at the scale where capillary effects are retained, while latent heat released or absorbed at the advancing interface produces a Stefan-type flux condition:

```math
\frac{\partial T_f}{\partial t}
=
\alpha_f\nabla^2T_f,
\qquad
T_i=T_m-\Gamma_i\kappa,
\qquad
\rho_i L_i V_n
=
k_f\partial_nT_f-k_u\partial_nT_u .
```

The subscripts (f,u,i) denote the relevant frozen/unfrozen phases and ice interface. This representation deliberately isolates the local phase-boundary physics from the additional poromechanical and hydraulic laws governing macroscopic frost heave.

The first correspondence is therefore the curvature-corrected interfacial condition:

```math
T_i-T_m=-\Gamma\kappa-\beta V_n
\quad\longleftrightarrow\quad
T_i-T_m=-\Gamma_i\kappa
```

The correspondence extends only to the capillary sharp-interface limit; the kinetic term (\beta V_n) has no demonstrated universal counterpart in the frost-heave formulation above and is therefore not included as a correspondence vector.

The second correspondence is the Stefan interface operator. Dividing each flux balance by its latent-heat coefficient gives the common normal-velocity form:

```math
V_n
=
\frac{k_s\partial_nT_s-k_l\partial_nT_l}{\rho L}
\quad\longleftrightarrow\quad
V_n
=
\frac{k_f\partial_nT_f-k_u\partial_nT_u}{\rho_iL_i}.
```

Thus the interface velocity is determined by a jump in normal diffusive flux divided by the latent phase-change scale in both systems.

The third correspondence follows from nondimensionalizing the diffusion equation with a characteristic interface speed (V) and length (R). Defining

```math
\xi=\frac{x}{R},
\qquad
\tau=\frac{Vt}{R},
\qquad
Pe=\frac{VR}{\alpha},
```

the transport equation becomes

```math
\frac{\partial T}{\partial \tau}
=
\frac{1}{Pe}\nabla_\xi^2T
```

for both the metal-solidification and local frost-heave temperature fields, with

```math
Pe_m=\frac{V_mR_m}{\alpha_m}
\quad\longleftrightarrow\quad
Pe_f=\frac{V_fR_f}{\alpha_f}.
```

The shared structural quantity is therefore not equality of the dimensional thermal properties but equality of the nondimensional transport operator at matched (Pe). The mapping stops there: soil permeability, unfrozen-water retention, pore pressure, and mechanical stress have no demonstrated counterpart in the metal-solidification equations displayed above and are not claimed to be isomorphic.

## 4. ASYMMETRIC METHODOLOGICAL TRANSFER & SCIENTIFIC HYPOTHESIS

* **Preferred Transfer Direction:** Dendritic-metal-solidification → ice-lens-growth-in-frost-heave
* **Asymmetric Maturity Rationale:** Metal solidification has a mature family of curvature-regularized moving-boundary solvers, including phase-field/sharp-interface formulations and adaptive interface-resolution strategies designed specifically to resolve curvature-dependent growth and latent-heat transport. The target frost-heave problem is mature in poromechanics and soil-water transport, but the local morphology of an advancing ice interface is less systematically resolved as a capillary-regularized moving boundary. The proposed transfer is therefore narrow: import moving-interface resolution and curvature regularization, not the metallurgical constitutive model.
* **Target Bottleneck Mitigation:** A curvature-regularized adaptive moving-interface solver should reduce the dependence of predicted ice-lens morphology on the numerical interface thickness or mesh scale while retaining the existing frost-heave hydraulic and mechanical closures outside the local phase boundary.
* **Falsifiable Prediction:** For a one-dimensional-to-axisymmetric ice-lens-growth benchmark in which (Pe_f=1) is imposed by nondimensional matching, the imported curvature-regularized moving-interface method should produce a converged nondimensional interface velocity (V_nR/\alpha_f) whose change under halving the interface-resolution length is below (1%), while the named baseline—an unregularized fixed-grid enthalpy/Stefan discretization at the same nominal mesh resolution—should exhibit a change exceeding (5%). The hypothesis is falsified if the baseline also remains below (1%), or if the transferred method fails to achieve the (1%) convergence criterion.

## 5. RELEVANT ACADEMIC SEARCH STRINGS FOR VERIFICATION

* `"dendritic solidification" AND "ice lens" AND "Gibbs-Thomson" AND "Stefan"`
* `"frost heave" AND "curvature" AND "moving boundary" AND "phase field"`
* `"ice lens growth" AND "adaptive mesh" AND "Stefan problem" AND "solidification"`
* `"ice lens" AND "dendritic growth" AND "Gibbs-Thomson" AND "phase-field"`

---

## ADVERSARIAL REVIEWS (Stage 2)

### First Adversarial Review
**Reviewer:** Anthropic Claude Sonnet 5
**Protocol:** v2.0
**Verdict:** FLAG
**Review Date:** 2026-08-14

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Both silos pair the same equation classes (parabolic diffusion, a curvature-corrected Dirichlet interface temperature, and a Stefan-type flux-jump balance); each equation is dimensionally consistent with the physical role claimed for it, and the Section 3 nondimensionalization (Pe = VR/α) is correctly derived from the stated diffusion equation, with no equation-class mismatch or misattribution from a third field.
- **CHECK 2 (Vocabulary Matrix Coherence):** FLAG — Items 1 ("Gibbs-Thomson temperature ↔ ice-interface equilibrium temperature") and 2 ("Stefan condition ↔ ice-lens latent-heat balance") are type-compatible and each Operator Role names a specific shared structure rather than hedged similarity. Item 3, "thermal diffusion length ↔ frost-heave thermal diffusion length," names a length scale, but its own Operator Role text and the Section 3 math construct a dimensionless ratio (Pe = VR/α) rather than a length — matching the YAML vector name "diffusion-field-similarity-parameter" instead.
- **CHECK 3 (Correspondence Vector Support):** PASS — Every listed YAML vector is demonstrated in Section 3 with an explicit equation: the Gibbs-Thomson correspondence via T_i − T_m = −Γκ − βV_n ↔ T_i − T_m = −Γ_iκ, the Stefan correspondence via the paired flux-ratio expressions for V_n, and the diffusion-similarity correspondence via Pe_m ↔ Pe_f. None are hedged as candidate or speculative; the entry explicitly excludes the kinetic term βV_n and the poromechanical terms from the claimed vectors rather than overclaiming them.
- **CHECK 4 (Transfer and Falsifiability):** FLAG — (a) Asymmetry: the transfer names a specific capability (curvature-regularized adaptive interface-resolution numerics from solidification) while explicitly excluding frost heave's own area of relative maturity (poromechanics/hydraulics), so this is not a direction that could plausibly run either way with equal benefit. (b) Falsifiability: the prediction names a specific measured quantity (nondimensional interface velocity V_nR/α_f under mesh-resolution halving), numeric thresholds (<1% vs. >5%), a named baseline (unregularized fixed-grid enthalpy/Stefan discretization), and explicit falsification conditions — well clear of the template non-prediction form. (c) Advisory: this pairing resembles a recognized line of work in the premelting-dynamics literature linking frost heave to solidification/crystal-growth theory through curvature (Gibbs-Thomson) effects; flagged for Stage 3 bibliometric check, not used as rejection grounds.

#### Stage 3 Watch Items
- Bibliometric check against the premelting-dynamics literature connecting frost heave to solidification/crystal-growth theory via curvature (Gibbs-Thomson) effects on interfacial equilibrium temperature — a line of work associated with authors such as Wettlaufer, Worster, and Rempel on continuum frost-heave models. Confirm whether this entry's specific three-vector packaging (Gibbs-Thomson condition + Stefan balance + Peclet-number similarity) is already published or is a novel packaging of a known analogy.
- Reconcile the Section 2 vocabulary item 3 label ("thermal diffusion length") with the dimensionless similarity parameter (Peclet number) it actually denotes in Section 3 and in the YAML vector name "diffusion-field-similarity-parameter."

### Second Adversarial Review
**Reviewer:** Alibaba Qwen 3.8 Max
**Protocol:** v2.0
**Verdict:** FLAG
**Review Date:** 2026-08-14

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Both silos display parabolic diffusion equations with Stefan flux balances and curvature-corrected interfacial temperature conditions; no equation-class mismatch or misattribution is apparent from the entry text alone.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — The mapped tokens are compatible mathematical objects: scalar interfacial boundary conditions are mapped to scalar interfacial boundary conditions, Stefan flux balances to Stefan flux balances, and diffusion-length/similarity-scale concepts to corresponding diffusion-scaling concepts.
- **CHECK 3 (Correspondence Vector Support):** PASS — The Gibbs-Thomson vector is supported by the paired curvature-corrected interface-temperature equations in Section 3; the Stefan vector is supported by the paired normal-velocity flux-balance equations; the diffusion-field similarity vector is supported by the nondimensionalization to the Peclet number and the matched nondimensional diffusion equation.
- **CHECK 4 (Transfer and Falsifiability):** FLAG — The transfer direction is asymmetric and the 1% versus 5% resolution-sensitivity benchmark is falsifiable; however, the shared Stefan/Gibbs-Thomson phase-change structure is recognizable from classical moving-boundary and solidification literature, so prior-art review is needed.

#### Stage 3 Watch Items
- Verify whether dendritic-solidification phase-field or sharp-interface methods have already been applied to ice-lens growth or freezing-soil models.
- Check whether the Peclet-number similarity and Stefan/Gibbs-Thomson pairing is treated as canonical in phase-change textbooks or reviews, especially classical Stefan-problem literature.
- Confirm whether frost-heave literature represents ice-interface curvature effects using the same Gibbs-Thomson form displayed here or through pressure/premelting-film closures.

### Third Adversarial Review
**Reviewer:** DeepSeek DeepSeek V4 Pro
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-14

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Both sides are parabolic diffusion equations with curvature-dependent Dirichlet interface conditions and Stefan flux balances; no equation-class mismatch or misattributed equation was found.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — The paired tokens are scalar interfacial boundary values, scalar flux-balance conditions, and compatible diffusion-length/similarity parameters; no category errors were found.
- **CHECK 3 (Correspondence Vector Support):** PASS — The Gibbs-Thomson vector is demonstrated by the displayed curvature-corrected interface equations; the Stefan vector by the derived normal-velocity flux-balance equations; and the diffusion-field-similarity vector by the Pe nondimensionalization in Section 3.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The proposed transfer is narrow and directional; the falsifiable prediction gives a quantitative convergence threshold and explicit falsification conditions. No canonical prior-art source was recognized from training.

#### Stage 3 Watch Items
- Probe whether the Gibbs-Thomson/Stefan sharp-interface mapping between metal solidification and frost-heave ice-lens growth is already established in geocryology or solidification literature.
- Check whether the omitted kinetic undercooling term (β V_n) has a frost-heave counterpart in premelting or kinetic interface laws, and whether its omission affects the claimed capillary-limit isomorphism.
- Verify that the local Stefan heat-flux balance for ice-lens growth remains valid once full poromechanical/hydraulic closures are included.

### Fourth Adversarial Review
**Reviewer:** Google Gemini 3.1 Pro
**Protocol:** v2.0
**Verdict:** FLAG
**Review Date:** 2026-08-14

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Both the classical dendritic metal solidification system and the simplified local ice-lens moving-boundary representations accurately reflect standard Stefan/Gibbs-Thomson parabolic phase-change equations without mismatch.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — Mapped concepts align correctly in mathematical type, properly linking scalar boundary conditions, normal flux balances, and normalization variables.
- **CHECK 3 (Correspondence Vector Support):** PASS — All three vectors listed in the YAML (`Gibbs-Thomson-curvature-corrected-interface-temperature`, `Stefan-latent-heat-interface-balance`, `diffusion-field-similarity-parameter`) are explicitly derived and demonstrated via operator correspondences in Section 3.
- **CHECK 4 (Transfer and Falsifiability):** FLAG — The transfer direction and falsifiability criteria are valid and rigorously defined, but this pairing is a canonical moving boundary analogy. The Stefan problem was originally formulated precisely for ice formation (J. Stefan, 1889) and its structural equivalence to metallurgical phase change is standard textbook thermodynamics.

#### Stage 3 Watch Items
- Investigate the novelty of applying curvature-regularized phase-field or adaptive moving-boundary solvers to frost heave, as phase-field modeling of ice lenses in soils is already an active area of geophysics and materials research.
- Consider whether the equivalence is too mathematically identical (ice freezing vs. metal freezing) to constitute a cross-silo discovery, as both are fundamentally the exact same physical process (solidification of a melt) differing only in material properties and the presence of the unmodeled porous matrix.

### Fifth Adversarial Review
**Reviewer:** Xiaomi MiMo V2.5 Pro
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-14

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Both silo equations are genuine parabolic diffusion with Gibbs-Thomson algebraic boundary conditions and Stefan flux-balance conditions; equation classes match on both sides and are consistent with the stated physical domains.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All three paired mappings (scalar boundary field ↔ scalar boundary field, scalar flux-balance condition ↔ scalar flux-balance condition, dimensionless transport parameter ↔ dimensionless transport parameter) are of compatible mathematical type with explicitly described shared structure.
- **CHECK 3 (Correspondence Vector Support):** PASS — All three listed vectors are demonstrated: Vector 1 (Gibbs-Thomson) with the paired curvature-corrected interface equations and honest exclusion of the kinetic undercooling term; Vector 2 (Stefan balance) with the paired normal-velocity flux-balance equations; Vector 3 (diffusion-field similarity parameter) with the explicit nondimensionalization yielding identical Pe-scaled transport operators.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The transfer direction (metallurgical moving-boundary solvers → frost-heave interface resolution) is genuinely asymmetric based on the stated maturity difference in curvature-regularized interface methods. The falsifiable prediction is specific: a 1% vs. 5% convergence threshold on nondimensional interface velocity under halved interface-resolution length, with explicit falsification conditions.

#### Stage 3 Watch Items
- **Prior-art advisory:** The Gibbs-Thomson + Stefan moving-boundary analogy between dendritic solidification and ice-lens frost heave is a well-established pairing in the cold-regions and solidification communities (Worster's mushy-zone framework; Rycroft and collaborators on phase-field models of ice growth). The human reviewer should verify whether the entry's specific novelty claim — that the local ice-lens morphology has not been systematically treated as a capillary-regularized moving boundary resolved by imported metallurgical solvers — is supported by the bibliometric record.
- **Terminology check:** Vocabulary matrix item 3 names the mapped quantity as "thermal diffusion length" but the Operator Role and Section 3 describe the Péclet number Pe = VR/α, a dimensionless ratio. The mathematical content is correct and unambiguous, but the reviewer may wish to verify whether "thermal diffusion length" is the conventional term in either community for this similarity parameter.

### Sixth Adversarial Review
**Reviewer:** Z.AI GLM-5.2
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-14

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Both equation sets are parabolic diffusion equations (∂T/∂t = α∇²T) with moving-boundary conditions of the same class: a curvature-corrected Dirichlet condition (Gibbs-Thomson) and a flux-jump Stefan condition. No equation-class mismatch. The entry honestly notes the kinetic term βV_n lacks a frost-heave counterpart and excludes it from the claimed correspondence rather than asserting false equivalence.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All three mappings pair objects of compatible mathematical type: scalar interfacial boundary fields ↔ scalar interfacial boundary fields, flux-balance conditions ↔ flux-balance conditions, and dimensionless transport ratios ↔ dimensionless transport ratios. Each Operator Role entry names a specific shared mathematical structure (curvature-dependent Dirichlet condition, scalar flux-balance on moving interface, dimensionless ratio normalizing diffusion equation) rather than hedging with "analogous to" language.
- **CHECK 3 (Correspondence Vector Support):** PASS — All three listed vectors are demonstrated with explicit equations: (1) the Gibbs-Thomson correspondence is shown as T_i−T_m=−Γκ−βV_n ⟷ T_i−T_m=−Γ_iκ with the kinetic term explicitly excluded; (2) the Stefan correspondence is shown by dividing both flux balances by latent-heat coefficients to yield the common V_n = (flux jump)/(latent heat) form; (3) the diffusion-field similarity parameter is demonstrated via nondimensionalization to ∂T/∂τ = (1/Pe)∇²_ξ T with Pe_m ⟷ Pe_f.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The transfer direction (metallurgy → frost heave) is genuinely asymmetric: metal solidification possesses mature curvature-regularized adaptive moving-interface solvers, while frost-heave modeling is mature in poromechanics but less developed in capillary-regularized local interface morphology. The falsifiable prediction is specific: a nondimensional interface velocity V_nR/α_f must change by less than 1% under interface-resolution halving, while a baseline unregularized enthalpy/Stefan discretization should change by more than 5%, with explicit falsification conditions stated if either threshold is not met.

#### Stage 3 Watch Items
- The Stefan problem with Gibbs-Thomson curvature regularization is textbook material in both solidification physics and ice/cryosphere physics individually; Stage 3 should verify whether the specific cross-domain pairing of dendritic-metal-solidification with frost-heave-ice-lens-growth has been explicitly published as an isomorphism.
- The entry explicitly excludes the kinetic undercooling term βV_n from the frost-heave side and scopes the isomorphism to the local sharp-interface limit only; Stage 3 should verify whether frost-heave models in the literature typically include or omit kinetic undercooling, as this scoping choice materially affects the claimed correspondence breadth.

### Seventh Adversarial Review
**Reviewer:** Microsoft Copilot 1.2
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-14

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Both silos are modeled by parabolic diffusion PDEs with curvature-corrected interfacial Dirichlet conditions and Stefan-type flux balances; the equations shown for dendritic solidification and for ice-lens growth belong to the same operator class and the entry explicitly notes the absence of a kinetic term counterpart in the frost-heave side.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — Each paired token in Section 2 maps objects of the same mathematical type (scalar interfacial field ↔ scalar interfacial field; flux-balance operator ↔ flux-balance operator; diffusion length ↔ diffusion length), and the Operator Role descriptions specify shared structure rather than hedged analogy.
- **CHECK 3 (Correspondence Vector Support):** PASS — The three listed vectors are demonstrated in the body: (1) Gibbs-Thomson-curvature-corrected-interface-temperature is shown by the curvature-corrected interfacial condition in Section 3; (2) Stefan-latent-heat-interface-balance is shown by the flux-balance equations and their divided normal-velocity forms; (3) diffusion-field-similarity-parameter is shown by the nondimensionalization producing matching \(Pe\) forms (see the displayed nondimensional PDE and Pe definitions).
- **CHECK 4 (Transfer and Falsifiability):** PASS — The transfer direction (metal → frost-heave) is plausibly asymmetric and justified in Section 4, and the falsifiable benchmark specifies measurable nondimensional convergence thresholds (1% vs 5%) and a concrete test (Pe_f = 1) that would falsify the hypothesis if not met.

#### Stage 3 Watch Items
- Verify prior-art overlap between solidification Stefan/Gibbs-Thomson mappings and frost-heave literature; the human reviewer should search for explicit prior isomorphisms.
- Examine whether coupling to soil hydraulic and poromechanical constitutive laws (omitted from the local reduction) could invalidate the local isomorphism when implemented numerically.
- Confirm precise numerical definitions used in the falsifiable benchmark (interface-resolution length, baseline discretization) so the 1%/5% thresholds are reproducible.
- Check whether the provenance metadata (model/version) or any claimed implementation details in Stage 3 include references to phase-field solver adaptations that already exist for porous media.

### Eighth Adversarial Review
**Reviewer:** xAI Grok 4.5 Fast
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-14

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Both displayed systems are parabolic diffusion equations closed by a curvature-corrected Dirichlet condition and a Stefan flux balance of identical mathematical class; the kinetic undercooling term is explicitly excluded from the claimed correspondence.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — Each paired token is of matching type (scalar interfacial Dirichlet data; scalar normal-flux jump condition; nondimensional diffusion-length ratio) and the Operator Role statements name the shared structure without hedge.
- **CHECK 3 (Correspondence Vector Support):** PASS — All three vectors (Gibbs-Thomson curvature correction, Stefan latent-heat balance, diffusion-field similarity parameter Pe) are demonstrated by explicit operator identities and nondimensionalization in Section 3.
- **CHECK 4 (Transfer and Falsifiability):** PASS — Direction is asymmetrically justified by maturity of curvature-regularized moving-boundary solvers; the prediction supplies quantitative convergence thresholds (1 % versus 5 %) under mesh halving that are experimentally distinguishable.

#### Stage 3 Watch Items
- Confirm whether the local capillary-regularized Stefan reduction for ice-lens growth is already standard in the frost-heave literature or remains under-developed relative to dendritic solidification solvers.

### Ninth Adversarial Review
**Reviewer:** Meta Muse Spark 1.1
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-14

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Both sides correctly present parabolic diffusion ∂T/∂t = α∇²T, curvature-dependent Dirichlet Gibbs-Thomson condition T_i = T_m - Γκ (-βV_n), and Stefan flux balance ρLV_n = k_s∂_nT_s - k_l∂_nT_l, same operator class and consistent with the claimed diffusion-controlled moving-boundary domain, supporting Section 1.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All three pairs are type-compatible (scalar interfacial boundary field ↔ scalar interfacial boundary field; scalar flux-balance operator ↔ scalar flux-balance operator; diffusion length / similarity length ↔ diffusion length) and each Operator Role specifies shared mathematical structure, not hedged assertion.
- **CHECK 3 (Correspondence Vector Support):** PASS — All three YAML vectors demonstrated in Section 3: Gibbs-Thomson-curvature-corrected-interface-temperature via T_i-T_m=-Γκ equations, Stefan-latent-heat-interface-balance via V_n = (k∂_nT jumps)/ρL forms, diffusion-field-similarity-parameter via ξ=x/R, τ=Vt/R, Pe=VR/α and ∂T/∂τ = (1/Pe)∇_ξ²T with Pe_m ↔ Pe_f mapping.
- **CHECK 4 (Transfer and Falsifiability):** PASS — Transfer Dendritic-metal-solidification → ice-lens-growth is asymmetric as stated (mature curvature-regularized moving-boundary/phase-field solvers in metallurgy vs. less resolved local ice-interface morphology in poromechanics, with explicit narrow scope). Prediction is falsifiable with specific measurable thresholds: Pe_f=1 benchmark, converged nondimensional velocity V_nR/α_f change <1% under halved interface resolution vs. >5% for unregularized fixed-grid enthalpy/Stefan baseline, with explicit falsification criteria.

#### Stage 3 Watch Items
- Both sides are canonical Gibbs-Thomson-regularized Stefan problems; probe Stage 3 bibliometrics for whether this operator identity (dendritic solidification ↔ ice lens) is already noted in free-boundary literature as the same Stefan problem in different materials.
- Probe whether adaptive curvature-regularized / phase-field methods have already been applied to frost-heave ice-lens growth, which would affect novelty of the proposed methodological transfer.