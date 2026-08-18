---
sid_metadata:
  entry_id: "SID-0050"
  schema_version: "2.0-production"
  maturity_stage: "adversarial-flagged"
provenance:
  company: "Anthropic"
  model_family: "Claude"
  model_version: "Sonnet 5"
  generation_timestamp: "2026-08-10"
  prompt_type: "unsupervised-structural-isomorphism-discovery"
isomorphism_metadata:
  domain_a: "chromatographic-equilibrium-theory"
  domain_b: "macroscopic-traffic-flow-theory"
  structural_family: "periodically-reconfigured-scalar-hyperbolic-conservation-law-networks"
  triple_correspondence_vectors:
    - "langmuir_isotherm_fundamental_diagram_constitutive_closure"
    - "rankine_hugoniot_lax_entropy_shock_construction"
    - "van_deemter_payne_whitham_diffusive_regularization"
    - "periodic_node_reconfiguration_boundary_condition"
discovery_rationale:
  why_not_obvious: "distinct_disciplinary_language / historically_isolated_practitioner_communities / convergent_independent_terminology_for_the_same_operator_class"
prior_discovery_metrics:
  structural_isomorphism_score: 7.5
  vocabulary_divergence_score: 9.0
  expected_methodological_transfer_score: 6.5
  community_separation_score: 9.0
  representation_mismatch_score: 3.0
  expected_transfer_effort: "medium"
  novelty_prior:
    estimate: 5.5
    uncertainty: "±2.0"
relationship_type: "candidate_structural_isomorphism"
validation_status:
  operator_equivalence_confidence: "high"
  constitutive_equivalence_confidence: "low"
  primary_failure_risk: "the generic operator-level claim (scalar hyperbolic conservation law with concave constitutive closure) is not itself unclaimed territory: a narrow pure-math 'delta-shock wave' literature has separately analyzed 'the chromatography equations' (Sun 2013; Zhang 2016) and Aw-Rascle-type traffic models (Shao & Huang) under the same singular-solution machinery without cross-citation, so Vectors 1-2 in isolation would not clear novelty. The entry's defensible novel content is narrower: the applied transfer of traffic's network-junction/demand-supply node formalism into SMB port-switching design (Vector 4, Section 4), which assumes the SMB ring's rotating column-role assignment maps onto a fixed-topology traffic node with time-varying control - a mapping that has not been checked against cases where the 'network topology itself' effectively reconfigures rather than just the flow-split at a static junction, and may require an extension the traffic literature has not needed to make."
  bibliometric_validation: "pending"
  first_adversarial_review:
    reviewer_model: "Alibaba Qwen3.8 Max"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-16"
    verdict: "REJECT"
    verdict_rationale: "The Vector-3 diffusive-regularization claim fails equation validity because the entry's own definition of the Payne-Whitham sound speed gives a velocity, not a velocity squared, so τ c_0^2 is not a diffusivity."
    failed_checks: ["Check 1: Vector 3's Payne-Whitham sound-speed definition gives c_0^2 dimensions of velocity, not velocity squared, so tau c_0^2 is not a diffusivity."]
    flagged_checks: ["Check 3: Vector 3 is only partially supported; the reduced parabolic traffic equation is not displayed and the asserted D_eff is dimensionally inconsistent, while Vectors 1, 2, and 4 are otherwise supported."]
    quoted_evidence:
      - >-
        (relaxation time $\tau$, traffic "sound speed" $c_0^2(\rho)=-\rho\,V'(\rho)$), reduces under a Chapman–Enskog-type small-$\tau$ expansion to a diffusively-corrected LWR equation of the same form as the ED model above, with $D_{\rm eff}(\rho)\propto \tau\, c_0^2(\rho)$ (dimensionally a diffusivity, since $[\tau][c_0^2]=$ time $\times$ (length/time)$^2$ = length$^2$/time).
      - >-
        with $V(\rho)$ a decreasing equilibrium speed–density relation, e.g. Greenshields' $V(\rho)=v_f(1-\rho/\rho_{\max})$
    stage_3_watch_items:
      - >-
        Verify whether the scalar-conservation-law/Rankine-Hugoniot/Lax analogy between chromatography and traffic, including Langmuir isotherm versus fundamental diagram, already appears in kinematic-wave or hyperbolic-conservation-law textbooks/reviews.
      - >-
        Check the delta-shock and Aw-Rascle/chromatography literature named in the entry for prior treatment of Vectors 1-2.
      - >-
        Ask whether the Payne-Whitham reduction requires an additional velocity scale or an explicit nondimensionalization to make c_0^2 a true squared speed and D_eff a true diffusivity.
  second_adversarial_review:
    reviewer_model: "DeepSeek DeepSeek V4 Pro"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-16"
    verdict: "REJECT"
    verdict_rationale: "The central constitutive-closure mapping misstates the role of the Langmuir isotherm in the Silo A conservation law: q(C) appears in the time-derivative accumulation term, not in the spatial flux term, so it is not a flux closure analogous to the fundamental diagram."
    failed_checks:
      - "Check 1: Section 1 claims the Silo A flux is closed by the Langmuir isotherm, but the displayed chromatography equation has spatial flux εu∂C/∂x independent of q(C)."
      - "Check 2: The Langmuir isotherm ↔ fundamental diagram Operator Role states both enter the flux term; q(C) enters the accumulation term in Silo A."
    flagged_checks:
      - "Check 3: Vector 3 (van_deemter_payne_whitham_diffusive_regularization) is only partially demonstrated; the Chapman–Enskog reduction of Payne–Whitham to D_eff ∝ τ c_0^2 is asserted, not derived, and no sign/stability check is provided."
      - "Check 4: Prior-art advisory — the LWR/chromatography scalar-hyperbolic correspondence is already visible in the delta-shock literature named in the entry's own validation_status (Sun 2013; Zhang 2016; Shao & Huang)."
    quoted_evidence:
      - "Both systems are governed by a scalar first-order hyperbolic conservation law whose flux is closed by a state-dependent, saturating constitutive function — the Langmuir isotherm q(C) in Silo A and the Greenshields-type fundamental diagram Q(ρ) in Silo B"
      - "Both are the scalar, concave, saturating constitutive closure entering the flux term of a first-order quasilinear PDE ∂u/∂t + ∂F(u)/∂x = 0-type system"
      - "ε∂C/∂t+(1−ε)∂q(C)/∂t+εu∂C/∂x=0"
    stage_3_watch_items:
      - "Determine whether the Langmuir isotherm ↔ fundamental diagram mapping can be repaired as an accumulation-side vs flux-side nonlinearity, and whether that changes the claimed operator equivalence."
      - "Probe the novelty of the generic scalar-hyperbolic correspondence against Sun 2013, Zhang 2016, and Shao & Huang delta-shock work, as the entry's validation_status already warns."
      - "Check the Payne–Whitham D_eff reduction for sign/stability and whether its parabolic regularization is genuinely of ED-model type."
      - "Examine the claimed transfer from static-topology traffic node solvers to SMB's periodically rotating port-role node; the entry itself flags this as unverified."
  third_adversarial_review:
    reviewer_model: "Google Gemini 3.1 Pro"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-16"
    verdict: "REJECT"
    verdict_rationale: "The vocabulary matrix contains a fundamental mathematical category error by defining rarefaction fans as discontinuities arising from crossing characteristics."
    failed_checks: ["Check 2: Vocabulary Matrix Coherence"]
    flagged_checks: []
    quoted_evidence: ["\"Both are constant states separated by a discontinuity satisfying the Rankine-Hugoniot jump condition $\\sigma = [F(u_L)-F(u_R)]/(u_L-u_R)$ and admissible only under the Lax entropy inequality; both arise from crossing characteristics under genuine nonlinearity of the same constitutive closure named above.\""]
    stage_3_watch_items: ["The pairing of chromatography and traffic flow equations under the LWR/kinematic-wave framework may already be canonical in conservation law literature (e.g., Rhee, Aris, & Amundson's foundational texts on first-order PDEs).", "Verify if the proposed 'node-Riemann-solver' formulation for SMB switching is genuinely novel or if similar finite-volume interface treatments already exist in modern chromatography simulations."]
  fourth_adversarial_review:
    reviewer_model: "Xiaomi MiMo V2.5 Pro"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-16"
    verdict: "PASS"
    verdict_rationale: "All four checks pass: equations are valid and correctly attributed to their stated domains, vocabulary mappings pair objects of compatible mathematical type with explicit shared operator structure, all four correspondence vectors are demonstrated in the body with equations or derivations, and the transfer direction is genuinely asymmetric with a quantified falsifiable prediction including explicit threshold values."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items:
      - "The entry itself identifies its primary novelty risk: Sun (2013, Appl. Math. Lett. 26(6):631-637), Zhang (2016, ZAMP 67), and Shao & Huang independently treat chromatography equations and traffic/traffic-related models under the same delta-shock / singular-solution machinery without cross-citation. The human reviewer should verify whether these works already subsume Vectors 1-2 and whether they touch Vector 4 (network-node level)."
      - "The van Deemter diffusivity D_L is treated as constant in the ED model while D_eff(rho) is state-dependent in the Payne-Whitham reduction. Both are valid as parabolic regularization coefficients, but the reviewer should confirm whether published SMB dynamic simulators actually use constant D_L or density/position-dependent variants, which would affect whether the operator-level claim ('same parabolic regularization') holds exactly."
      - "Vector 4 claims the traffic demand-supply node-Riemann-solver formalism has not been applied to SMB port-switching. The reviewer should search specifically for any SMB literature importing network-flow or conservation-law junction solvers, including work by Duennebail, Kloppenburg, or any process-systems engineering group that may have independently developed equivalent node models."
  fifth_adversarial_review:
    reviewer_model: "Z.AI GLM-5.2"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-17"
    verdict: "FLAG"
    verdict_rationale: "All four checks pass at the equation/category level — the displayed PDEs are correctly derived, both silos are genuinely scalar first-order hyperbolic conservation laws with parabolic diffusive regularizations, all four vocabulary mappings are type-coherent, and all four correspondence vectors are demonstrated with equations — but the chromatography↔traffic operator-level correspondence is an instance of Whitham's canonical kinematic-wave framework, warranting a Stage-3 prior-art probe."
    failed_checks: []
    flagged_checks: ["Check 4(c): prior-art recognition — the operator-level correspondence (scalar hyperbolic conservation law closed by a saturating constitutive function, with Rankine-Hugoniot/Lax-entropy shock construction) is the canonical kinematic-wave framework of Whitham, Linear and Nonlinear Waves (1974), which treats traffic flow and the adsorption/chromatography conservation-law family under the same machinery; the entry's own validation_status concedes the generic operator-level claim is 'not itself unclaimed territory.'"]
    quoted_evidence: []
    stage_3_watch_items: ["Prior art (advisory, never grounds for rejection): confirm whether the chromatography↔traffic pairing is explicitly named as an interdisciplinary analogy in Whitham (1974), LeVeque (Finite Volume Methods for Hyperbolic Problems), or Dafermos (Hyperbolic Conservation Laws in Continuum Physics), beyond generic 'both are scalar conservation laws' pedagogy; LeVeque uses traffic flow as the canonical scalar-law example and chromatography/adsorption appears in the same conservation-law tradition.", "Delta-shock overlap the entry self-identifies (Sun 2013, Appl. Math. Lett. 26(6):631–637; Zhang 2016, ZAMP 67; Shao & Huang on Aw-Rascle delta-shocks): verify these references exist and whether their independent treatment of 'the chromatography equations' and traffic models under common singular-solution machinery bears on Vectors 1–2 novelty as the entry's own primary_failure_risk asserts.", "Vector 4 transfer feasibility — convex-vs-concave flux curvature: in the conserved variable U=εC+(1−ε)q(C) the chromatography flux F(U)=εuC(U) is convex (characteristic speed increases with C, so F''(U)>0), whereas the traffic flux Q(ρ)=ρV(ρ) is concave (Q''<0). The entry acknowledges the monotonicity sign differs but calls it 'a physical labeling difference, not a mathematical one.' Probe whether importing traffic's concave-flux demand/supply node-Riemann-solver (Daganzo/Lebacque; Coclite-Garavello-Piccoli 2005; Herty-Lebacque-Moutari 2009) into a convex-flux SMB system requires curvature-specific adaptation the entry does not address, since Riemann-solver shock/rarefaction branches are swapped under opposite flux curvature.", "Vector 4 topology: confirm whether SMB's rotating column-role assignment role(k,t)=role₀((k−⌊t/t_s⌋) mod N_col) is genuinely reducible to a fixed-topology node with time-varying control (the traffic formalism's setting), or whether the periodic topology reconfiguration requires an extension the traffic literature has not developed — this is the entry's claimed novel content and its own stated primary_failure_risk.", "Falsifiable prediction: verify arXiv:2405.09328 exists and provides a single-column characteristic-based WENO scheme for the chromatography ED model as claimed; confirm whether industrial dynamic SMB simulators already employ flux-limited/Godunov schemes that would narrow the claimed numerical-diffusion gap (Pe_num≈2N≈200, ρ_H≥5) underpinning the falsification thresholds (ρ_H≤1.25 target; ≤1.5 falsification gate; upwind ρ_H<3 disconfirmation)."]
  sixth_adversarial_review:
    reviewer_model: "OpenAI GPT-5.6 Luna"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-16"
    verdict: "REJECT"
    verdict_rationale: "The entry contains a fatal category error in the core constitutive mapping and a dimensionally inconsistent Payne–Whitham reduction, so the claimed shared operator/constitutive structure is not mathematically supported by the displayed equations."
    failed_checks: ["Check 1: The Payne–Whitham equation is paired with a dimensionally incorrect definition of c_0^2 and an unsupported diffusivity reduction.", "Check 2: The Langmuir isotherm q(C) is incorrectly identified as a flux constitutive closure analogous to the traffic flux Q(rho)."]
    flagged_checks: ["Check 3: Vector 3 is not actually established by a derivation of the stated D_eff proportionality; Vector 4 asserts a shared node structure without an equation establishing the SMB switching event as the same node-Riemann problem.", "Check 4: The falsifiable prediction is quantitatively specific, but its stated HETP-inflation estimate omits the physical diffusivity contribution in H_sim/H_phys."]
    quoted_evidence: ['Silo B''s Payne (1971)/Whitham second-order model, `math\n\\frac{\\partial \\rho}{\\partial t}+\\frac{\\partial(\\rho v)}{\\partial x}=0,\\qquad\n\\frac{\\partial v}{\\partial t}+v\\frac{\\partial v}{\\partial x}=\\frac{V(\\rho)-v}{\\tau}-\\frac{c_0^2(\\rho)}{\\rho}\\frac{\\partial \\rho}{\\partial x}\n` (relaxation time $\tau$, traffic "sound speed" $c_0^2(\rho)=-\rho\,V''(\rho)$), reduces under a Chapman–Enskog-type small-$\tau$ expansion to a diffusively-corrected LWR equation of the same form as the ED model above, with $D_{\rm eff}(\rho)\propto \tau\, c_0^2(\rho)$ (dimensionally a diffusivity, since $[\tau][c_0^2]=$ time $\times$ (length/time)$^2$ = length$^2$/time).', 'Langmuir isotherm $q(C)$ ↔ Fundamental diagram / Greenshields relation $Q(\rho)=\rho V(\rho)$\n    *   *Operator Role:* Both are the scalar, concave, saturating constitutive closure entering the flux term of a first-order quasilinear PDE $\partial u/\partial t + \partial F(u)/\partial x = 0$-type system; both are scalar functions of a scalar conserved density, so no type transformation is needed.']
    stage_3_watch_items: ["Probe the entry's own cited overlap between the chromatography equations and traffic-model singular-solution machinery (the Sun (2013), Zhang (2016), and Shao & Huang items named in primary_failure_risk/search strings) during bibliometric review.", "Check whether the proposed periodically-reconfigured SMB node is mathematically a topology-changing network rather than merely a periodically forced fixed-topology junction; the entry itself identifies this as an unresolved assumption.", "Verify the quantitative numerical-diffusion/HETP prediction: with physical and numerical diffusivities both present, the simple ratio implied by the displayed modified-equation estimate is not the stated Pe_phys/Pe_num expression."]
  seventh_adversarial_review:
    reviewer_model: "Microsoft Copilot 1.2"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-16"
    verdict: "PASS"
    verdict_rationale: "The entry consistently demonstrates a genuine operator-level isomorphism between scalar hyperbolic conservation laws (including shock admissibility and Chapman–Enskog diffusive regularization) across all four listed correspondence vectors with no equation-class or category errors."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items:
      - "Entry cites Sun (2013), Zhang (2016), and Shao & Huang in the validation_status as potentially overlapping work on 'delta-shock' treatments; human reviewers should verify these citations and whether they already establish the claimed operator-level correspondences."
      - "The falsifiable numerical prediction in Section 4 uses specific thresholds (e.g., $Pe_{\\rm phys}\\ge1000$, $N=100$, baseline $Pe_{\\rm num}=2N\\approx200$, predicted $\\rho_H\\ge5$, target $\\rho_H\\le1.5$); Stage 3 should check the realism of these parameter choices against typical industrial SMB grids and the referenced single-column WENO implementation (arXiv:2405.09328)."
      - "The claim that node-Riemann-solver formalisms for static-topology, time-varying-control networks have not been applied to periodically-rotating-topology SMB nodes is a literature-gap assertion; Stage 3 should search for any prior work applying demand/supply node solvers to rotating or reconfiguring boundary-role networks in chromatography."
      - "Verify the arXiv:2405.09328 single-column WENO extension feasibility and whether its numerical diffusivity estimates align with the modified-equation arguments used in the falsification test."
  eighth_adversarial_review:
    reviewer_model: "xAI Grok 4.5 Fast"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-16"
    verdict: "FLAG"
    verdict_rationale: "All mathematical correspondences and equations are internally consistent and demonstrated; the sole issue is recognition of the core scalar hyperbolic conservation-law structure with concave constitutive closure as a canonical textbook pairing between chromatography and LWR traffic models."
    failed_checks: []
    flagged_checks: ["Check 4: prior-art recognition of canonical chromatography–LWR isomorphism"]
    quoted_evidence: []
    stage_3_watch_items: ["Canonical status of scalar hyperbolic conservation laws with concave flux (Langmuir vs. fundamental diagram) already treated jointly in the pure-math delta-shock literature (Sun 2013; Zhang 2016; Shao & Huang on Aw-Rascle) without cross-citation; verify whether Vector 4 (rotating-topology node) is genuinely absent from prior SMB or traffic-network work"]
  ninth_adversarial_review:
    reviewer_model: "Meta Muse Spark 1.1"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-16"
    verdict: "PASS"
    verdict_rationale: "All four vectors are demonstrated with correct scalar hyperbolic conservation laws and compatible vocabulary types, and Section 4 provides asymmetric transfer with quantitatively falsifiable HETP thresholds; no equation-class mismatch or category error found."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items: ["Generic operator claim Vectors 1-2 (concave flux scalar conservation law) overlaps with textbook examples of LWR and chromatography as standard concave-flux cases and with delta-shock literature cited in entry itself (Sun 2013 Appl Math Lett 26(6):631-637; Zhang 2016 ZAMP 67; Shao & Huang Aw-Rascle) - probe whether Vector 4 periodic node reconfiguration is the defensible novel content per validation_status primary_failure_risk", "Verify Vector 4 mapping from rotating-topology SMB node to static-topology traffic demand-supply node does not require topology-reconfiguration extension beyond existing traffic node well-posedness theory (Coclite-Garavello-Piccoli 2005; Herty-Lebacque-Moutari 2009)"]
---

# INTERDISCIPLINARY STRUCTURAL MAPPING: ENTRY 0050

## 1. CROSS-SILO SYSTEM DEFINITION
*   **Silo A (Field 1):** Local-equilibrium (ideal) theory of nonlinear preparative and simulated-moving-bed (SMB) liquid chromatography, where solute concentration bands self-sharpen into fronts or spread into diffuse patterns according to adsorption-isotherm curvature.
*   **Silo B (Field 2):** Macroscopic (kinematic-wave) traffic flow theory, where vehicle density bands self-sharpen into stop-and-go shockwaves or spread into acceleration fans according to fundamental-diagram curvature, extended to networks of roads joined at signal-controlled junctions.
*   **Mathematical Isomorphism:** Both systems are governed by a scalar first-order hyperbolic conservation law whose flux is closed by a state-dependent, saturating constitutive function — the Langmuir isotherm $q(C)$ in Silo A and the Greenshields-type fundamental diagram $Q(\rho)$ in Silo B — such that shock formation and admissibility follow the identical Rankine-Hugoniot/Lax-entropy construction (Vectors 1–2); finite front width in both is governed by an emergent parabolic regularization obtained by a Chapman–Enskog-type reduction of a more microscopic kinetic description, mass-transfer resistance versus driver relaxation dynamics (Vector 3); and both admit networks of such conservation laws joined at nodes whose flux-allocation rule is forced by an externally imposed period-$P$ schedule, SMB port switching versus signal-phase cycling (Vector 4). The correspondence is restricted to this operator- and boundary-condition-level structure and does **not** extend to the underlying constitutive physics, which are unrelated (adsorption thermodynamics versus car-following psychology) — this is a formal, not a physical, unification.

## 2. DIAGNOSTIC VOCABULARY MATRIX
*   **Langmuir isotherm $q(C)$** ↔ **Fundamental diagram / Greenshields relation $Q(\rho)=\rho V(\rho)$**
    *   *Operator Role:* Both are the scalar, concave, saturating constitutive closure entering the flux term of a first-order quasilinear PDE $\partial u/\partial t + \partial F(u)/\partial x = 0$-type system; both are scalar functions of a scalar conserved density, so no type transformation is needed. Their derivatives set the characteristic (kinematic-wave) speed in each field.
*   **Self-sharpening front / "proportionate pattern" (favorable vs. unfavorable isotherm)** ↔ **Traffic shockwave / rarefaction (acceleration) fan**
    *   *Operator Role:* Both are constant states separated by a discontinuity satisfying the Rankine-Hugoniot jump condition $\sigma = [F(u_L)-F(u_R)]/(u_L-u_R)$ and admissible only under the Lax entropy inequality; both arise from crossing characteristics under genuine nonlinearity of the same constitutive closure named above.
*   **HETP / van Deemter axial dispersion coefficient $D_L$** ↔ **Payne–Whitham anticipation–relaxation emergent diffusivity $D_{\rm eff}(\rho)$**
    *   *Operator Role:* Both are the coefficient of a parabolic regularization term $\partial/\partial x[D\,\partial u/\partial x]$ appended to the hyperbolic operator, and both are derived by collapsing a more microscopic two-variable (or two-phase) kinetic description down to a single effective diffusivity in a small-parameter (Chapman–Enskog-type) limit.
*   **SMB port-switching schedule (zone role reassignment every $t_s$)** ↔ **Signal-controlled junction (phase reassignment every $T_{\rm cycle}$)**
    *   *Operator Role:* Both are a time-periodic reallocation of the boundary/source flux at a fixed spatial node of a network of 1-D conservation-law segments, $s_j(t) = s_j(t \bmod P)$, requiring a node-level Riemann/demand–supply solver to resolve the flux split consistently with each segment's own entropy solution.

## 3. CORE MATHEMATICAL PARALLELISM

**Silo A.** Under local-equilibrium (ideal) chromatography theory — the Rhee–Aris–Amundson tradition built on the DeVault/Glueckauf equilibrium-theory line and still the basis of modern SMB design work (Storti, Mazzotti, Morbidelli; Rajendran & Mazzotti's generalized-Langmuir extensions) — a solute of mobile-phase concentration $C(x,t)$ in a bed of voidage $\varepsilon$, interstitial velocity $u$, and instantaneously-equilibrated adsorbed-phase concentration $q(C)$ (e.g. the Langmuir isotherm $q(C)=q_s KC/(1+KC)$) obeys the mass balance

```math
\varepsilon\frac{\partial C}{\partial t}+(1-\varepsilon)\frac{\partial q(C)}{\partial t}+\varepsilon u\frac{\partial C}{\partial x}=0
```

which is a scalar quasilinear hyperbolic PDE whose characteristics carry constant $C$ at the state-dependent speed

```math
\left.\frac{dx}{dt}\right|_{C}=\frac{\varepsilon u}{\varepsilon+(1-\varepsilon)\,q'(C)}
```

Because the Langmuir isotherm is concave ($q''(C)<0$), $q'(C)$ decreases with $C$, so this characteristic speed *increases* with $C$: higher-concentration levels outrun lower ones, and for a step increase in feed concentration (adsorption/loading), faster high-$C$ characteristics catch up to slower low-$C$ characteristics ahead of them, crossing and producing a self-sharpening shock front — the classical "favorable isotherm" result.

**Silo B.** Under the Lighthill–Whitham (1955) / Richards (1956) kinematic-wave (LWR) theory, vehicle density $\rho(x,t)$ obeys

```math
\frac{\partial \rho}{\partial t}+\frac{\partial Q(\rho)}{\partial x}=0,\qquad Q(\rho)=\rho\,V(\rho)
```

with $V(\rho)$ a decreasing equilibrium speed–density relation, e.g. Greenshields' $V(\rho)=v_f(1-\rho/\rho_{\max})$, giving characteristic speed $dx/dt|_\rho = Q'(\rho)=v_f(1-2\rho/\rho_{\max})$, which *decreases* with $\rho$ (eventually going negative). Upstream of a bottleneck, faster low-density characteristics catch up to slower high-density characteristics ahead, crossing and producing the classic backward-propagating jam shockwave.

**Bridge (Vectors 1–2).** $C(x,t)$ and $\rho(x,t)$ are the same mathematical object — nonnegative scalar densities obeying a scalar conservation law closed by a concave, saturating constitutive function — so no type transformation is required. The *sign* of the monotonicity differs (higher $C$ is faster; higher $\rho$ is slower), but this is a physical labeling difference, not a mathematical one: both obey the identical Rankine-Hugoniot condition

```math
\sigma_{\rm chrom}=\frac{\varepsilon u}{\varepsilon+(1-\varepsilon)\,\dfrac{q(C_L)-q(C_R)}{C_L-C_R}}\ ,\qquad
\sigma_{\rm traffic}=\frac{Q(\rho_L)-Q(\rho_R)}{\rho_L-\rho_R}
```

and the identical Lax entropy admissibility test (characteristic speed ahead of the shock $<$ shock speed $<$ characteristic speed behind it) governs which side of each constitutive curve produces a shock versus a rarefaction fan in both fields. The correspondence extends cleanly to this operator/entropy level; it does **not** claim the physical mechanisms coincide.

**Vector 3 (diffusive regularization).** Silo A's equilibrium-dispersive (ED) model adds a Fickian correction,

```math
\varepsilon\frac{\partial C}{\partial t}+(1-\varepsilon)\frac{\partial q(C)}{\partial t}+\varepsilon u\frac{\partial C}{\partial x}=\varepsilon D_L\frac{\partial^2 C}{\partial x^2}
```

with $D_L$ tied to the van Deemter (1956) plate-height equation $H=A+B/u+Cu$ via the classical plate-theory/rate-theory equivalence $H\approx 2D_L/u$. Silo B's Payne (1971)/Whitham second-order model,

```math
\frac{\partial \rho}{\partial t}+\frac{\partial(\rho v)}{\partial x}=0,\qquad
\frac{\partial v}{\partial t}+v\frac{\partial v}{\partial x}=\frac{V(\rho)-v}{\tau}-\frac{c_0^2(\rho)}{\rho}\frac{\partial \rho}{\partial x}
```

(relaxation time $\tau$, traffic "sound speed" $c_0^2(\rho)=-\rho\,V'(\rho)$), reduces under a Chapman–Enskog-type small-$\tau$ expansion to a diffusively-corrected LWR equation of the same form as the ED model above, with $D_{\rm eff}(\rho)\propto \tau\, c_0^2(\rho)$ (dimensionally a diffusivity, since $[\tau][c_0^2]=$ time $\times$ (length/time)$^2$ = length$^2$/time). Both diffusivities are thus emergent, small-parameter reductions of a more microscopic two-variable kinetic description (mass-transfer-resistance kinetics vs. driver-relaxation kinetics) — not independently postulated Fickian terms.

**Vector 4 (periodic node reconfiguration).** In SMB, column $k$'s role (feed/desorbent inlet, extract/raffinate outlet, or interior) is reassigned every switching interval $t_s$: $\text{role}(k,t)=\text{role}_0\big((k-\lfloor t/t_s\rfloor)\bmod N_{\rm col}\big)$, and dynamic SMB simulators (single-column linearizations, finite-volume multi-column solvers) currently re-impose this boundary condition by direct re-simulation at each switch. In a signal-controlled traffic network, a node with $m$ incoming and $n$ outgoing links resolves flux via the demand/supply Riemann solver of Daganzo (1995) and Lebacque (1996),

```math
q_a(x_a,t)=Q_a\!\big(\min\{k_{a,c},k_a\}\big)\ \ (\text{demand}),\qquad
s_a(x_a,t)=Q_a\!\big(\max\{k_{a,c},k_a\}\big)\ \ (\text{supply})
```

with signal control imposing $\xi_i(t)=\xi_i(t \bmod T_{\rm cycle})$ on the allowable split, and this general node-Riemann-solver formalism has been extended to arbitrary junction topologies with existence/well-posedness results (Coclite, Garavello & Piccoli 2005; Herty, Lebacque & Moutari 2009). Both are conservation-law networks whose node-flux rule is periodically forced; the formalism developed for Silo B's *static-topology, time-varying-control* node has not, to this entry's knowledge, been applied to Silo A's *periodically-rotating-topology* node — the gap named in Section 4.

## 4. ASYMMETRIC METHODOLOGICAL TRANSFER & SCIENTIFIC HYPOTHESIS
*   **Preferred Transfer Direction:** Macroscopic Traffic-Network Flow Theory → SMB Chromatography Process Engineering
*   **Asymmetric Maturity Rationale:** Traffic engineering has a mature, decades-deep toolkit specifically for *networks* of scalar conservation laws joined at periodically-reconfigured nodes: the Daganzo/Lebacque demand–supply node solver, general-junction well-posedness theory (Coclite–Garavello–Piccoli 2005; Herty–Lebacque–Moutari 2009), and Godunov-family high-resolution schemes (the Cell Transmission Model is explicitly a Godunov discretization of LWR) validated against real sensor data. Chromatography, by contrast, is genuinely mature at *single-column* equilibrium theory (competitive-Langmuir Riemann problems are fully solved analytically for binary systems) and at *steady-periodic* SMB design via TMB-equivalence "triangle theory" (Storti/Mazzotti/Morbidelli), and as of 2024 has imported characteristic-based WENO schemes for the single-column ED model (arXiv:2405.09328) — so the target is not broadly immature. The narrow, specific gap is *transient, switching-induced* behavior at the network-node level: no generalized periodically-forced node-Riemann-solver formalism appears to have been applied to the SMB switching event itself, which is instead handled by direct re-simulation or local linearization at each switch.
*   **Target Bottleneck Mitigation:** Reformulating each SMB switching event as a Riemann problem at a periodically-relabeled network node — importing the demand/supply node formalism together with characteristic-based high-resolution shock-capturing already validated for the single-column ED model — should let SMB transient and cyclic-steady-state simulators resolve the competitive-Langmuir shock front through each switch without the artificial numerical smearing that coarse, non-flux-limited re-simulation currently introduces, narrowing the gap between predicted and observed cyclic-steady-state purity that presently drives conservative operating-point selection in industrial SMB design.
*   **Falsifiable Prediction:** For a two-component competitive-Langmuir SMB case with physical column Péclet number $Pe_{\rm phys}=uL/D_L\ge 1000$ (from $H_{\rm phys}=2D_L/u$ and reduced plate heights $h=H_{\rm phys}/d_p\in[2,5]$), a standard first-order-upwind finite-volume baseline at $N=100$ axial nodes per zone (representative of published dynamic multi-column SMB grids) has modified-equation numerical diffusivity $D_{\rm num}\approx u\Delta x/2$, giving $Pe_{\rm num}=2N\approx 200$ and predicted apparent-HETP inflation ratio $\rho_H=H_{\rm sim}/H_{\rm phys}\ge Pe_{\rm phys}/Pe_{\rm num}\ge 5$. Replacing this baseline with a 3rd-order characteristic-based WENO scheme at the *same* $N=100$, extended from the single-column formulation in arXiv:2405.09328 to the periodically-switched multi-column case via the node-Riemann-solver reformulation above, should recover $\rho_H\le 1.25$. **Falsification:** the transfer claim fails if, at matched $N=100$ and $Pe_{\rm phys}\ge1000$, either the upwind baseline shows $\rho_H<3$ (numerical diffusion not actually dominant, contradicting the modified-equation estimate) or the WENO/node-solver result does not close to $\rho_H\le1.5$.

## 5. RELEVANT ACADEMIC SEARCH STRINGS FOR VERIFICATION
*   `"equilibrium theory" AND "Langmuir isotherm" AND "Riemann problem" AND chromatography`
*   `"Lighthill-Whitham-Richards" AND "fundamental diagram" AND "shock wave" AND "entropy condition"`
*   `"simulated moving bed" AND "port switching" AND ("node model" OR "supply-demand" OR "network junction")`
*   `"chromatography equations" AND "delta shock" AND "traffic flow"` — deliberate self-falsification string; surfaces Sun (2013, *Appl. Math. Lett.* 26(6):631–637), Zhang (2016, *ZAMP* 67), and Shao & Huang on Aw-Rascle delta-shocks, which independently treat "the chromatography equations" and traffic models under the same singular-solution machinery without cross-citing each other — evidence bearing directly on this entry's novelty claim (see `primary_failure_risk`).

---

## ADVERSARIAL REVIEWS (Stage 2)

### First Adversarial Review
**Reviewer:** Alibaba Qwen3.8 Max
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-16

#### Results by Check
- **CHECK 1 (Equation Validity):** FAIL — The entry defines traffic "sound speed" as "$c_0^2(\rho)=-\rho\,V'(\rho)$" and claims "$D_{\rm eff}(\rho)\propto \tau\, c_0^2(\rho)$ (dimensionally a diffusivity, since $[\tau][c_0^2]=$ time $\times$ (length/time)$^2$ = length$^2$/time)"; with its own Greenshields relation "$V(\rho)=v_f(1-\rho/\rho_{\max})$", this gives $c_0^2=v_f\rho/\rho_{\max}$, a velocity, so $\tau c_0^2$ has dimensions of length and the claimed diffusive regularization is not mathematically supported.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — The paired tokens are type-compatible as scalar closure functions or diffusivity coefficients, and the Operator Role statements name shared mathematical roles; the dimensional defect in the traffic diffusivity is treated under Check 1.
- **CHECK 3 (Correspondence Vector Support):** FLAG — Vectors 1 and 2 are demonstrated in Section 3's Silo A/Silo B equations and Bridge shock-speed formulas; Vector 4 is demonstrated in Section 3's periodic node reconfiguration formulas; Vector 3 is only partially supported in Section 3's Vector 3 paragraph because the reduced parabolic traffic equation is not displayed and the asserted $D_{\rm eff}$ is dimensionally inconsistent.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The transfer direction from mature traffic-network node solvers to SMB switching is not backwards, and the HETP-inflation prediction has measurable thresholds; possible prior art is recorded as a Stage 3 watch item, not a rejection ground.

#### Stage 3 Watch Items
- Verify whether the scalar-conservation-law/Rankine-Hugoniot/Lax analogy between chromatography and traffic, including Langmuir isotherm versus fundamental diagram, already appears in kinematic-wave or hyperbolic-conservation-law textbooks/reviews.
- Check the delta-shock and Aw-Rascle/chromatography literature named in the entry for prior treatment of Vectors 1-2.
- Ask whether the Payne-Whitham reduction requires an additional velocity scale or an explicit nondimensionalization to make $c_0^2$ a true squared speed and $D_{\rm eff}$ a true diffusivity.

### Second Adversarial Review
**Reviewer:** DeepSeek DeepSeek V4 Pro
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-16

#### Results by Check
- **CHECK 1 (Equation Validity):** FAIL — Section 1 states that Silo A's "flux is closed by ... the Langmuir isotherm q(C)", but in the displayed equation `ε∂C/∂t+(1−ε)∂q(C)/∂t+εu∂C/∂x=0` the spatial flux is `εu∂C/∂x`, independent of `q(C)`; `q(C)` appears only in the accumulation term.
- **CHECK 2 (Vocabulary Matrix Coherence):** FAIL — The mapping "Langmuir isotherm q(C) ↔ Fundamental diagram / Greenshields relation Q(ρ)=ρV(ρ)" claims both "enter the flux term"; this is false for q(C), which enters the time-derivative holdup term, not the flux.
- **CHECK 3 (Correspondence Vector Support):** FLAG — Vectors 2 and 4 are equation-supported. Vector 3 is only partially demonstrated: both diffusively corrected equations are shown, but the Payne–Whitham Chapman–Enskog reduction to `D_eff ∝ τ c_0^2` is asserted without derivation or sign/stability check.
- **CHECK 4 (Transfer and Falsifiability):** FLAG — Asymmetry and falsifiable prediction are adequately specified; however, prior art in the scalar-hyperbolic/delta-shock literature is already named in the entry's own `validation_status` (Sun 2013; Zhang 2016; Shao & Huang) and should be probed at Stage 3.

#### Stage 3 Watch Items
- Whether the Langmuir isotherm ↔ fundamental diagram mapping can be repaired as an accumulation-side vs flux-side nonlinearity without invalidating Vector 1.
- Novelty against the delta-shock literature already cited in the entry: Sun 2013, Zhang 2016, Shao & Huang.
- The sign/stability of the Payne–Whitham `D_eff ∝ τ c_0^2` reduction and whether it genuinely matches the ED parabolic regularization.
- The applicability of traffic static-topology node-Riemann solvers to SMB's periodically rotating port-role node, which the entry's `primary_failure_risk` explicitly flags as unverified.

### Third Adversarial Review
**Reviewer:** Google Gemini 3.1 Pro
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-16

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — The PDE formulations, characteristic speeds, Rankine-Hugoniot conditions, and diffusive regularization models correctly match their respective physical domains and support the structural correspondence claimed.
- **CHECK 2 (Vocabulary Matrix Coherence):** FAIL — For the mapping `Self-sharpening front / "proportionate pattern" (favorable vs. unfavorable isotherm) ↔ Traffic shockwave / rarefaction (acceleration) fan`, the entry claims `"Both are constant states separated by a discontinuity satisfying the Rankine-Hugoniot jump condition $\sigma = [F(u_L)-F(u_R)]/(u_L-u_R)$ and admissible only under the Lax entropy inequality; both arise from crossing characteristics under genuine nonlinearity of the same constitutive closure named above."` This is mathematically false: while this correctly describes shocks/self-sharpening fronts, rarefaction fans (and proportionate patterns) are continuous similarity solutions that arise from *diverging* characteristics, not discontinuities. 
- **CHECK 3 (Correspondence Vector Support):** PASS — All four correspondence vectors listed in the YAML (`langmuir_isotherm_fundamental_diagram_constitutive_closure`, `rankine_hugoniot_lax_entropy_shock_construction`, `van_deemter_payne_whitham_diffusive_regularization`, `periodic_node_reconfiguration_boundary_condition`) are successfully demonstrated in Sections 3 and 4 with explicit equations and operator identities.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The methodological transfer from macroscopic traffic node-solvers to SMB port-switching is asymmetric and well-justified. The falsifiable prediction provides specific, measurable, and comparative bounds for numerical HETP inflation ($\rho_H$).

#### Stage 3 Watch Items
* The pairing of chromatography and traffic flow equations under the LWR/kinematic-wave framework may already be a canonical textbook example in general conservation law literature (e.g., Rhee, Aris, & Amundson's foundational texts on first-order PDEs). 
* Verify if the proposed demand-supply 'node-Riemann-solver' formulation for SMB switching is genuinely novel or if standard finite-volume interface treatments in existing modern chromatography simulations are mathematically equivalent.

### Fourth Adversarial Review
**Reviewer:** Xiaomi MiMo V2.5 Pro
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-16

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — All five displayed equations (chromatography mass balance, LWR conservation law, Rankine-Hugoniot conditions for both, ED model, Payne-Whitham model, and Daganzo demand/supply) are correctly attributed to their stated domains, belong to the same PDE class on each side of each pairing, and support the structural correspondences claimed in Section 1.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All four vocabulary mappings pair objects of compatible mathematical type (scalar constitutive closures ↔ scalar constitutive closures, discontinuity solutions ↔ discontinuity solutions, diffusivity coefficients ↔ diffusivity coefficients, periodic boundary-condition schedules ↔ periodic boundary-condition schedules), and each Operator Role explanation names a specific shared mathematical structure rather than relying on hedged similarity assertions.
- **CHECK 3 (Correspondence Vector Support):** PASS — All four listed vectors are demonstrated in Section 3 with equations: Vector 1 by the mass-balance PDEs and constitutive closures on both sides, Vector 2 by the explicit Rankine-Hugoniot formulas and Lax entropy discussion, Vector 3 by the ED and Payne-Whitham equations with Chapman-Enskog reduction argument, and Vector 4 by the Daganzo demand/supply formulas and the SMB role-reassignment formula.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The transfer direction (traffic → SMB) is genuinely asymmetric: traffic engineering possesses the mature network-junction toolkit (Daganzo/Lebacque node solvers, Coclite–Garavello–Piccoli well-posedness, CTM) while SMB chromatography lacks an equivalent periodically-forced node-Riemann-solver formalism for the switching event. The falsifiable prediction specifies measurable quantities (apparent-HETP inflation ratio ρ_H), a grid resolution (N = 100), a physical parameter range (Pe_phys ≥ 1000), concrete numerical thresholds (ρ_H ≤ 1.25 target, ρ_H < 3 / ρ_H > 1.5 falsification boundaries), and named baseline and proposed methods — this is a genuine testable prediction, not a template non-prediction. Prior art advisory: the entry's self-identified delta-shock literature (Sun 2013, Zhang 2016, Shao & Huang on Aw-Rascle) is a significant bibliometric concern for novelty that Stage 3 must investigate.

#### Stage 3 Watch Items
- The delta-shock / singular-solution literature the entry self-identifies (Sun 2013 in Appl. Math. Lett.; Zhang 2016 in ZAMP; Shao & Huang on Aw-Rascle) independently treats chromatography equations and traffic models under the same mathematical machinery. Stage 3 must determine whether this work already subsumes Vectors 1–2, and whether it touches the network-node level (Vector 4) at all.
- Whether published dynamic SMB simulators treat the van Deemter diffusivity D_L as truly constant or use density/position-dependent variants, which affects the precision of the operator-level claim that both sides share "the same parabolic regularization."
- Whether any SMB literature has independently imported conservation-law junction or network-flow solvers (e.g., from process-systems engineering groups working on multi-column switching networks), which would weaken the novelty of Vector 4's proposed transfer.

I'll perform targeted searches to inform my review, particularly to verify the mathematical claims and assess prior-art recognition for Check 4(c).
Based on my verification searches and careful line-by-line mathematical audit of the entry, I have confirmed the equations, characteristic-speed derivations, Rankine-Hugoniot formulas, Lax entropy statements, dimensional analysis, and modified-equation numerics are all internally consistent. The only reviewable concern is a prior-art recognition under Check 4(c).

### Fifth Adversarial Review
**Reviewer:** Claude Sonnet 4.5
**Protocol:** v2.0
**Verdict:** FLAG
**Review Date:** 2026-08-17

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Both silos are genuinely scalar first-order quasilinear hyperbolic conservation laws (chromatography mass balance ε∂C/∂t+(1−ε)∂q/∂t+εu∂C/∂x=0; LWR ∂ρ/∂t+∂Q(ρ)/∂x=0), and both diffusive regularizations are parabolic (ED model εD_L∂²C/∂x²; Payne-Whitham Chapman-Enskog reduction to ∂/∂x[D_eff(ρ)∂ρ/∂x] with D_eff∝τc_0²(ρ), dimensionally length²/time). The chromatography characteristic speed εu/(ε+(1−ε)q'(C)) and Rankine-Hugoniot speed εu/(ε+(1−ε)[q(C_L)−q(C_R)]/(C_L−C_R)) were re-derived from the displayed conservation law and are correct; the traffic RH σ=[Q(ρ_L)−Q(ρ_R)]/(ρ_L−ρ_R) and the Lax statement "characteristic speed ahead of the shock < shock speed < characteristic speed behind it" (i.e., f'(u_R)<σ<f'(u_L)) are standard and correctly stated. No equation-class mismatch, no misattributed equation.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All four mappings pair objects of compatible type: concave saturating constitutive closure ↔ concave saturating constitutive closure (q(C), Q(ρ) both genuinely concave); shock/rarefaction solution ↔ shock/rarefaction solution; diffusion coefficient ↔ diffusion coefficient; periodic node-flux reallocation rule ↔ periodic node-flux reallocation rule. No spatial-domain↔time-point, rate↔position, or dimensional↔dimensionless category errors. The Operator Role entries name shared structure (scalar quasilinear PDE ∂u/∂t+∂F(u)/∂x=0; RH jump σ=[F(u_L)−F(u_R)]/(u_L−u_R); parabolic term ∂/∂x[D∂u/∂x]; time-periodic node schedule s_j(t)=s_j(t mod P)) rather than relying on hedged analogy.
- **CHECK 3 (Correspondence Vector Support):** PASS — All four listed vectors are demonstrated in the body, not merely named. Vector 1 (langmuir_isotherm_fundamental_diagram) is established in §2 and §3 via both constitutive functions and their characteristic speeds. Vector 2 (rankine_hugoniot_lax_entropy) is established in §3 "Bridge" with both RH formulas written explicitly and the Lax admissibility test stated. Vector 3 (van_deemter_payne_whitham) is established in §3 "Vector 3" with the ED model equation, the Payne-Whitham second-order system, and the Chapman-Enskog small-τ reduction yielding D_eff(ρ)∝τc_0²(ρ). Vector 4 (periodic_node_reconfiguration) is established in §3 "Vector 4" with the SMB role-reassignment formula, the Daganzo/Lebacque demand-supply solver, and the periodic schedule ξ_i(t)=ξ_i(t mod T_cycle). No vector is left speculative or undemonstrated.
- **CHECK 4 (Transfer and Falsifiability):** FLAG — Asymmetry (4a) is narrowly but specifically argued and defensible: traffic possesses the mature network-node demand/supply Riemann-solver formalism and general-junction well-posedness theory, whereas SMB chromatography is mature at single-column equilibrium theory and steady-periodic triangle theory but lacks a transient switching-event node-Riemann-solver formalism; the direction (traffic→SMB) is not backwards. Falsifiability (4b) is strong: the prediction names a concrete measurable quantity (apparent-HETP inflation ratio ρ_H=H_sim/H_phys), specific regime (Pe_phys≥1000, N=100, reduced plate heights h∈[2,5]), a quantitative modified-equation estimate (D_num≈uΔx/2, Pe_num≈2N≈200, ρ_H≥5), a target (ρ_H≤1.25 under 3rd-order WENO/node-solver), and explicit disconfirmation gates (upwind ρ_H<3, or WENO not closing to ρ_H≤1.5) — this is a genuine prediction, not a template non-prediction. Prior art (4c, advisory only): the chromatography↔traffic operator-level correspondence is an instance of Whitham's canonical kinematic-wave framework (Linear and Nonlinear Waves, 1974), which unifies traffic flow, flood waves, and the adsorption/chromatography conservation-law family under the same scalar hyperbolic conservation-law / Rankine-Hugoniot / Lax-entropy machinery; the entry's own validation_status concedes the generic operator-level claim is "not itself unclaimed territory." Recorded as advisory — not grounds for rejection.

#### Stage 3 Watch Items
- **Prior art (advisory):** Confirm whether the chromatography↔traffic pairing is explicitly named as an interdisciplinary analogy in Whitham (1974, Linear and Nonlinear Waves), LeVeque (Finite Volume Methods for Hyperbolic Problems), or Dafermos (Hyperbolic Conservation Laws in Continuum Physics), beyond the generic "both are scalar conservation laws" pedagogy. LeVeque uses traffic flow as the canonical scalar-law example, and chromatography/adsorption equilibrium theory (Rhee-Aris-Amundson, 1970, Phil. Trans. R. Soc.) sits in the same conservation-law tradition.
- **Delta-shock literature overlap (entry self-identified):** Verify Sun (2013, Appl. Math. Lett. 26(6):631–637), Zhang (2016, ZAMP 67), and Shao & Huang on Aw-Rascle delta-shocks exist and assess whether their independent treatment of "the chromatography equations" and traffic models under common singular-solution machinery — without cross-citation — bears on Vectors 1–2 novelty as the entry's own primary_failure_risk asserts.
- **Vector 4 transfer feasibility — convex-vs-concave flux curvature:** In the conserved variable U=εC+(1−ε)q(C), the chromatography flux F(U)=εuC(U) is convex (F''(U)>0, since the characteristic speed εu/(ε+(1−ε)q'(C)) increases with C), whereas the traffic flux Q(ρ)=ρV(ρ) is concave (Q''(ρ)<0). The entry acknowledges the monotonicity sign differs but characterizes it as "a physical labeling difference, not a mathematical one." Probe whether importing traffic's concave-flux demand/supply node-Riemann-solver into a convex-flux SMB system requires curvature-specific adaptation (Riemann-solver shock/rarefaction branches are swapped under opposite flux curvature) that the entry's transfer design does not address.
- **Vector 4 topology:** Confirm whether SMB's rotating column-role assignment role(k,t)=role₀((k−⌊t/t_s⌋) mod N_col) is genuinely reducible to a fixed-topology node with time-varying control (the traffic formalism's setting), or whether the periodic topology reconfiguration itself — not merely the flow-split at a static junction — requires an extension the traffic literature has not developed. This is the entry's claimed novel content and its own stated primary_failure_risk.
- **Falsifiable prediction underpinning:** Verify arXiv:2405.09328 exists and provides a single-column characteristic-based WENO scheme for the chromatography ED model as claimed; confirm whether industrial dynamic SMB simulators already employ flux-limited/Godunov-type schemes that would narrow the claimed numerical-diffusion gap (Pe_num≈2N≈200, ρ_H≥5) on which the falsification thresholds (ρ_H≤1.25 target; ≤1.5 falsification gate; upwind ρ_H<3 disconfirmation) rest.

### Sixth Adversarial Review
**Reviewer:** OpenAI GPT-5.6 Luna
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-16

#### Results by Check
* **CHECK 1 (Equation Validity):** FAIL — The Payne–Whitham reduction is mathematically inconsistent as stated: the entry defines $c_0^2=-\rho V'(\rho)$ but then treats it as having units of velocity squared, so the claimed $D_{\rm eff}\propto\tau c_0^2$ dimensional argument does not follow; the displayed model also does not by itself establish that proportionality.
* **CHECK 2 (Vocabulary Matrix Coherence):** FAIL — The mapping “**Langmuir isotherm $q(C)$ ↔ Fundamental diagram / Greenshields relation $Q(\rho)=\rho V(\rho)$**” is a category error because $q(C)$ enters the chromatography accumulation/storage term, whereas $Q(\rho)$ is the traffic flux; the claim that both are “entering the flux term” is therefore false.
* **CHECK 3 (Correspondence Vector Support):** FAIL — Vector 1 is not demonstrated as the claimed flux-closure correspondence because $q(C)$ is not the chromatography flux; Vector 3 is also unsupported because the claimed Chapman–Enskog result $D_{\rm eff}\propto\tau c_0^2$ is asserted rather than derived and rests on the inconsistent $c_0^2$ definition. Vector 2 has an explicit Rankine–Hugoniot construction on both sides, while Vector 4 supplies node demand/supply equations on the traffic side and an SMB role-reassignment formula but does not establish the asserted mathematical identity of the two node problems.
* **CHECK 4 (Transfer and Falsifiability):** PASS — The proposed transfer direction is presented as asymmetric within the entry's stated scope, and the prediction specifies measurable numerical thresholds and a concrete falsification criterion; however, the numerical HETP estimate should be checked because the displayed numerical diffusivity would add to, rather than simply replace, the physical diffusivity.

#### Stage 3 Watch Items
* Probe the entry's own cited chromatography/traffic singular-solution overlap (Sun (2013), Zhang (2016), and Shao & Huang) for prior-art implications.
* Check whether the proposed SMB switching event is genuinely a topology-reconfiguring node problem rather than a fixed-topology node with periodic control.
* Verify the quantitative numerical-diffusion-to-HETP calculation underlying the claimed $\rho_H$ thresholds.

### Seventh Adversarial Review
**Reviewer:** Microsoft Copilot 1.2
**Protocol:** v2.0  
**Verdict:** PASS  
**Review Date:** 2026-08-16

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — The Silo A mass-balance and characteristic-speed formulas and the Silo B LWR equations are both first-order scalar hyperbolic conservation laws; the quoted Rankine–Hugoniot expressions are algebraically consistent with the stated conserved variables and fluxes (e.g., the chromatography conserved variable \(w=\varepsilon C+(1-\varepsilon)q(C)\) yields the stated \(\sigma_{\rm chrom}\) formula).
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — Each paired mapping in Section 2 maps objects of the same mathematical type (scalar constitutive closure ↔ scalar constitutive closure; discontinuity/shock ↔ discontinuity/shock; emergent diffusivity ↔ emergent diffusivity; time-periodic boundary-role reassignment ↔ time-periodic node control), and the Operator Role entries specify shared mathematical structure rather than hedged analogy.
- **CHECK 3 (Correspondence Vector Support):** PASS — All four YAML-listed vectors are demonstrated in the body with equations or derivations:  
  - **langmuir_isotherm_fundamental_diagram_constitutive_closure** — shown by the Silo A PDE and Silo B LWR flux and the discussion of characteristic speeds (Section 3, Silo A and Silo B).  
  - **rankine_hugoniot_lax_entropy_shock_construction** — shown by the Rankine–Hugoniot formulas and Lax admissibility statement in the Bridge subsection.  
  - **van_deemter_payne_whitham_diffusive_regularization** — shown by the ED model with \(\varepsilon D_L\partial_{xx}C\) and the PW model with small-\(\tau\) Chapman–Enskog reduction to an effective diffusivity.  
  - **periodic_node_reconfiguration_boundary_condition** — shown by the SMB role-reassignment formula and the node demand/supply equations with periodic signal control. Each vector is supported by explicit equations or a clear small-parameter reduction argument in the body.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The transfer direction (Traffic → SMB) is argued as asymmetric with concrete rationale; the entry provides a specific, measurable falsifiable prediction with numerical thresholds and pass/fail criteria (e.g., \(Pe_{\\rm phys}\\ge1000\), \(N=100\), baseline and WENO target \(\\rho_H\) bounds), satisfying the falsifiability requirement. Prior-art overlap is noted in the entry itself (advisory for Stage 3).

#### Stage 3 Watch Items
- Verify the cited prior-art references (Sun 2013; Zhang 2016; Shao & Huang) for overlap with the claimed operator-level correspondences and whether they already treat the rotating-topology or node-reconfiguration cases.
- Check the realism of the numerical-falsification parameter choices and whether the modified-equation estimate for baseline numerical diffusivity (\(D_{\rm num}\approx u\Delta x/2\)) and the resulting \(\\rho_H\) ratios are representative of industrial SMB simulators.
- Confirm the feasibility of extending the single-column WENO scheme (arXiv:2405.09328) to the periodically-switched multi-column case via a node-Riemann-solver reformulation and whether any prior implementations exist.
- Inspect whether any literature applies demand/supply node solvers to networks with rotating or reconfiguring boundary-role assignments in chromatography or related process-engineering contexts.

### Eighth Adversarial Review
**Reviewer:** xAI Grok 4.5 Fast
**Protocol:** v2.0
**Verdict:** FLAG
**Review Date:** 2026-08-16

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — The chromatography mass-balance (with Langmuir closure and characteristic speed), LWR equation (with Greenshields flux and characteristic speed), Rankine–Hugoniot expressions, equilibrium-dispersive parabolic correction, and Payne–Whitham reduction to effective diffusivity are all correctly stated for their domains and belong to matching equation classes (scalar quasilinear hyperbolic conservation laws plus Chapman–Enskog parabolic regularizations).
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — Each paired token is of compatible mathematical type (constitutive scalar closures, entropy-admissible discontinuities, emergent diffusivities, time-periodic node flux reallocations) and the Operator Role statements name the shared structure rather than merely asserting analogy.
- **CHECK 3 (Correspondence Vector Support):** PASS — All four listed vectors are demonstrated by explicit equations or operator identities in Sections 1–3 (constitutive closures and RH/Lax in the Bridge; diffusive regularizations under Vector 3; periodic node reconfiguration under Vector 4).
- **CHECK 4 (Transfer and Falsifiability):** FLAG — Transfer direction is genuinely asymmetric (mature traffic network-node solvers versus the acknowledged gap in transient SMB switching formalisms) and the numerical prediction supplies concrete, measurable thresholds on \(\rho_H\) at fixed \(N\) and \(Pe_{\rm phys}\); however the core operator pairing is a canonical interdisciplinary analogy already appearing in hyperbolic-conservation-law textbooks and the pure-math delta-shock literature.

#### Stage 3 Watch Items
- Canonical status of the scalar hyperbolic conservation law with concave constitutive closure (Langmuir isotherm versus fundamental diagram) already treated jointly under singular-solution machinery in the pure-math literature (Sun 2013; Zhang 2016; Shao & Huang) without cross-citation.
- Whether the claimed Vector-4 transfer (fixed-topology demand–supply node solvers applied to periodically rotating SMB column roles) has any prior appearance in the SMB or traffic-network literature, given the topology-reconfiguration subtlety noted by the entry itself.

### Ninth Adversarial Review
**Reviewer:** Meta Muse Spark 1.1
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-16

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Both Silo A $\varepsilon C_t+(1-\varepsilon)q(C)_t+\varepsilon u C_x=0$ with characteristic speed $\varepsilon u/(\varepsilon+(1-\varepsilon)q'(C))$ and Silo B $\rho_t+Q(\rho)_x=0$ with $Q'(\rho)$ are genuine scalar first-order hyperbolic conservation laws with concave saturating closures; Rankine-Hugoniot $\sigma_{\rm chrom}=\varepsilon u/[\varepsilon+(1-\varepsilon)(q_L-q_R)/(C_L-C_R)]$ and $\sigma_{\rm traffic}=(Q_L-Q_R)/(\rho_L-\rho_R)$, ED parabolic regularization $\varepsilon D_L C_{xx}$, and Payne-Whitham system with Chapman-Enskog reduction $D_{\rm eff}\propto\tau c_0^2$ are correctly attributed and share the same operator class, with explicit acknowledgment that monotonicity sign differs but operator identity does not.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All four pairs are type-compatible: constitutive closure ↔ constitutive closure (scalar function of scalar density, derivatives set characteristic speed), shock/rarefaction ↔ shock/rarefaction (both RH jump + Lax entropy), diffusivity $D_L$ ↔ $D_{\rm eff}$ (both parabolic regularization coefficients from small-parameter reduction of two-variable kinetics), and periodic schedule $s_j(t)=s_j(t\bmod P)$ ↔ periodic signal phase $\xi_i(t)=\xi_i(t\bmod T_{\rm cycle})$ (both time-periodic node flux reallocation requiring Riemann/demand-supply solver), with no spatial-domain-to-time-point or field-to-global-constraint category errors and no hedged-only operator roles.
- **CHECK 3 (Correspondence Vector Support):** PASS — All four listed vectors are demonstrated in body: langmuir_isotherm_fundamental_diagram_constitutive_closure via Langmuir $q(C)=q_sKC/(1+KC)$ and Greenshields $Q(\rho)=\rho v_f(1-\rho/\rho_{\max})$ and characteristic speeds (Section 3 Silo A/B); rankine_hugoniot_lax_entropy_shock_construction via explicit $\sigma_{\rm chrom},\sigma_{\rm traffic}$ and Lax inequality in Bridge paragraph; van_deemter_payne_whitham_diffusive_regularization via ED equation with $H=A+B/u+Cu$ and Payne-Whitham second-order system plus Chapman-Enskog reduction and dimensional check; periodic_node_reconfiguration_boundary_condition via $\text{role}(k,t)=\text{role}_0((k-\lfloor t/t_s\rfloor)\bmod N_{\rm col})$, demand $q_a=Q_a(\min\{k_{a,c},k_a\})$ / supply $s_a=Q_a(\max\{k_{a,c},k_a\})$, and signal cycle $\xi_i(t\bmod T_{\rm cycle})$.
- **CHECK 4 (Transfer and Falsifiability):** PASS — Asymmetry is genuine: traffic's mature network-junction/demand-supply/Godunov (Cell Transmission Model) toolkit for periodically-forced nodes is transferred to SMB's gap in transient switching-node handling, not the reverse, and entry explicitly acknowledges chromatography's maturity in single-column and steady-periodic triangle theory. Falsifiability is specific and measurable: at $Pe_{\rm phys}\ge1000$, $N=100$, predicts upwind baseline $\rho_H=H_{\rm sim}/H_{\rm phys}\ge5$ (with $Pe_{\rm num}=2N$) versus WENO+node-solver $\rho_H\le1.25$, with falsification thresholds $\rho_H<3$ for baseline or failure to reach $\rho_H\le1.5$ for WENO; this is not the template non-prediction. No canonical textbook pairing requiring prior-art FLAG identified; the general concave-flux overlap is textbook-standard but Vector 4 is not.

#### Stage 3 Watch Items
- Probe novelty narrowly: generic scalar hyperbolic structure (Vectors 1-2) is textbook (Whitham Linear and Nonlinear Waves; Rhee-Aris-Amundson; Lighthill-Whitham-Richards) and has separate delta-shock treatments (Sun 2013; Zhang 2016; Shao & Huang Aw-Rascle) noted in entry's own search strings and validation_status primary_failure_risk — confirm defensible novelty rests on Vector 4 traffic demand-supply node formalism applied to SMB rotating-topology switching, not on Vectors 1-2 alone.
- Verify Vector 4 mapping assumption: entry maps SMB's rotating column-role assignment to fixed-topology traffic node with time-varying control — check against cases where network topology itself reconfigures versus flow-split at static junction, and whether traffic well-posedness results (Coclite et al. 2005; Herty et al. 2009) need extension.