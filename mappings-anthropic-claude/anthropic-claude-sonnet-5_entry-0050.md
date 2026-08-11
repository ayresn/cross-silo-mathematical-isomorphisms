---
sid_metadata:
  entry_id: "SID-0050"
  schema_version: "2.0-production"
  maturity_stage: "candidate"
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