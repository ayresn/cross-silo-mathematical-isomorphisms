---
sid_metadata:
  entry_id: "SID-0053"
  schema_version: "2.0-production"
  maturity_stage: "candidate"
provenance:
  company: "Anthropic"
  model_family: "Claude"
  model_version: "Opus 5"
  generation_timestamp: "2026-08-12"
  prompt_type: "unsupervised-structural-isomorphism-discovery"
isomorphism_metadata:
  domain_a: "applied-superconductivity-magnet-quench-protection"
  domain_b: "clinical-neurophysiology-cortical-spreading-depolarization"
  structural_family: "bistable-semilinear-parabolic-ignition-fronts"
  triple_correspondence_vectors:
    - "shared_bistable_parabolic_operator_with_unit_restoring_slope_after_affine_nondimensionalization"
    - "maxwell_equal_area_stall_condition_minimum_propagating_current_vs_sd_abort_threshold"
    - "unstable_stationary_nucleus_first_integral_mpz_vs_critical_initiation_half_length"
    - "shared_L2_gradient_flow_lyapunov_functional_and_mountain_pass_content_mqe_vs_threshold_kcl_moles"
    - "generation_to_clearance_capacity_ratio_with_unit_threshold_stekly_number_vs_pump_reserve"
    - "diffusion_free_core_path_independent_dose_integral_miits_vs_depolarization_duration"
discovery_rationale:
  why_not_obvious: "incompatible_ontologies / historically_isolated_communities / structure_visible_only_after_nondimensionalization"
prior_discovery_metrics:
  structural_isomorphism_score: 8.6
  vocabulary_divergence_score: 9.4
  expected_methodological_transfer_score: 7.8
  community_separation_score: 9.6
  representation_mismatch_score: 6.8
  expected_transfer_effort: "medium"
  novelty_prior:
    estimate: 7.4
    uncertainty: "±1.3"
relationship_type: "candidate_structural_isomorphism"
validation_status:
  operator_equivalence_confidence: "high"
  constitutive_equivalence_confidence: "medium"
  primary_failure_risk: "source_term_nonautonomy — the Silo B source depends on slow variables (ATP availability, [Na⁺]ᵢ, glutamate, cell swelling) that are frozen in the single-field reduction; the bistable reduction is valid only on the fast ionic timescale"
  bibliometric_validation: "pending"
---

# INTERDISCIPLINARY STRUCTURAL MAPPING: ENTRY 0053

## 1. CROSS-SILO SYSTEM DEFINITION

*   **Silo A (Field 1):** Applied superconductivity — magnet stability and quench protection engineering. A localized thermal disturbance in a composite superconductor either decays back to the cryogenic operating point or ignites a self-sustaining normal zone that propagates along the conductor at the normal-zone propagation velocity.
*   **Silo B (Field 2):** Clinical and experimental neurophysiology — cortical spreading depolarization (SD) in injured cortex. A focal ionic disturbance either is reabsorbed by Na⁺/K⁺-ATPase clearance and astrocytic buffering or ignites a self-sustaining depolarized zone that propagates across cortex at 1.5–7 mm min⁻¹.
*   **Mathematical Isomorphism:** Under the affine rescalings $u=(T-T_{op})/(T_c-T_{op})$ and $w=(K-K_{rest})/(K_r-K_{rest})$ followed by division by each system's linear restoring slope at its own rest state, the Wilson normal-zone equation and the Grafstein–Tuckwell–Miura extracellular-potassium equation become the *same* semilinear bistable parabolic operator $\tau\partial_t u=\lambda^{2}\partial_x^{2}u+\hat g(u)$ with $\hat g(0)=0,\ \hat g'(0)=-1$, so that their traveling-front solvability relation, Maxwell equal-area stall condition, unstable stationary nucleus and its first integral, $L^2$-gradient-flow Lyapunov functional and mountain-pass content, and unit-threshold generation-to-clearance capacity ratio coincide term by term — exactly for the operator and its stationary and traveling-wave structure, only in the flux-factorized diffusion-free core limit for the dose integral, and not at all at the level of constitutive source form (piecewise-quadratic current sharing versus Hill-type release and pump) or slow-variable coupling.

## 2. DIAGNOSTIC VOCABULARY MATRIX

*   **Current-sharing temperature $T_{cs}$** ↔ **SD initiation threshold $[\mathrm{K^+}]_{e,\theta}$**
    *   *Operator Role:* Both are the interior unstable zero $\theta$ of the shared source, $\hat g(\theta)=0$, $\hat g'(\theta)>0$, separating the two basins of $\tau\partial_t u=\lambda^2\partial_x^2u+\hat g(u)$. $T_{cs}$ is a real scalar in K; $[\mathrm{K^+}]_{e,\theta}$ is a real scalar in mol m⁻³. The affine maps $u=(T-T_{op})/(T_c-T_{op})$ and $w=(K-K_{rest})/(K_r-K_{rest})$ carry both to the same dimensionless $\theta\in(0,u_+)$, giving $\theta_A=1-I/I_{c0}$ and $\theta_B=(K_\theta-K_{rest})/(K_r-K_{rest})$.
*   **Stekly cryostability parameter $\alpha_S$** ↔ **Pump-reserve ratio $\Pi$**
    *   *Operator Role:* Both are the dimensionless ratio (peak generation capacity)/(clearance capacity at the reference excursion) multiplying the generation term in the nondimensional source; both are dimensionless reals whose unit crossing marks loss of the self-sustaining upper state. $\alpha_S=\rho_m J_m^2A_m/(hP(T_c-T_{op}))$; $\Pi=(j_0+j_r)/j_p$.
*   **Minimum propagating zone half-length $\ell_{MPZ}$** ↔ **Critical initiation half-length $\ell^{*}$**
    *   *Operator Role:* Both are the half-width of the unstable stationary solution $U_c$ of $\lambda^2U''+\hat g(U)=0$, obtained from the identical first integral $\tfrac{\lambda^2}{2}U'^2+\hat G(U)=0$. Both are lengths in m; no rescaling needed beyond $\lambda_A=\sqrt{kA/hP}$ versus $\lambda_B=\sqrt{D_K^{*}\alpha/r}$.
*   **Minimum quench energy $E_{MQE}$** ↔ **Threshold KCl content $Q^{*}$**
    *   *Operator Role:* Both are the stored-extensive-quantity content of the same mountain-pass profile $U_c$ of the shared Lyapunov functional $F$. Types differ (J versus mol) and are reconciled by identifying the densities conjugate to the diffusing potential — i.e. the coefficients of $\partial_t$ in each PDE: $C\,(T-T_{op})\ \leftrightarrow\ \alpha\,(K-K_{rest})$, in J m⁻³ and mol m⁻³ respectively. The shared dimensionless invariant is the nucleus content $\mathcal{Q}=\lambda^{-1}\!\int U_c\,d\xi$.
*   **Minimum propagating current $I_p$ / cold-end recovery** ↔ **SD abort (stall) threshold**
    *   *Operator Role:* Both are the Maxwell equal-area condition $\int_0^{u_+}\hat g(u)\,du=0$, i.e. the vanishing of the numerator in the traveling-wave solvability relation $\tau c\int U'^2 d\xi=\int_0^{u_+}\hat g\,du$. Both are codimension-one surfaces in the respective parameter spaces $(I,h)$ and $(j_0,j_r,j_p,K_p)$.
*   **Normal-zone propagation velocity (NZPV)** ↔ **SD front velocity $v_{SD}$**
    *   *Operator Role:* Both are the eigenvalue $c$ of the same traveling-wave operator $\lambda^2U''+\tau cU'+\hat g(U)=0$ with $U(-\infty)=u_+$, $U(+\infty)=0$. Both in m s⁻¹.
*   **Quench integral (MIITs) $\Gamma_A$** ↔ **Cumulative depolarization duration $\Gamma_B$**
    *   *Operator Role:* Both are the path-independent first integral of the diffusion-free core dynamics, $\int(\text{normalized drive})\,dt=$ state function of the peak excursion. Types are reconciled by normalizing each drive to its reference value ($J_m^2\!\to\!(J_m/J_{op})^2$; ATP availability $m$ already dimensionless), after which both integrals carry units of s.

## 3. CORE MATHEMATICAL PARALLELISM

**Silo A.** A composite superconductor operating at $T_{op}$ carries transport current $I$; a mechanical or flux-jump disturbance heats a short length above the current-sharing temperature $T_{cs}$, at which current begins to commutate into the normal matrix and Joule generation switches on. Magnet engineers model the resulting one-dimensional competition between generation, axial conduction and cryogen cooling with the Wilson normal-zone equation:

```math
C\,\partial_t T \;=\; k\,\partial_x^{2}T \;+\; G(T;I)\;-\;\frac{hP}{A}\bigl(T-T_{op}\bigr),
\qquad
G(T;I)=\frac{\rho_m\,I_m(T)^{2}}{A\,A_m}
```

```math
I_m(T)=
\begin{cases}
0, & T<T_{cs}\\[4pt]
I\,\dfrac{T-T_{cs}}{T_c-T_{cs}}, & T_{cs}\le T\le T_c\\[6pt]
I, & T>T_c
\end{cases}
\qquad
T_{cs}=T_{op}+\bigl(T_c-T_{op}\bigr)\Bigl(1-\tfrac{I}{I_{c0}}\Bigr)
```

Setting $u=(T-T_{op})/(T_c-T_{op})$, $\tau_A=CA/hP$, $\lambda_A=\sqrt{kA/hP}$ and dividing through by $(hP/A)(T_c-T_{op})$:

```math
\tau_A\,\partial_t u=\lambda_A^{2}\,\partial_x^{2}u+\hat g_A(u),
\qquad
\hat g_A(u)=\alpha_S\,\varphi_A(u)-u,
\qquad
\alpha_S=\frac{\rho_m J_m^{2}A_m}{hP\,(T_c-T_{op})}
```

```math
\varphi_A(u)=
\begin{cases}
0,&u<\theta_A\\[3pt]
\Bigl(\tfrac{u-\theta_A}{1-\theta_A}\Bigr)^{2},&\theta_A\le u\le 1\\[5pt]
1,&u>1
\end{cases}
\qquad \theta_A=1-\tfrac{I}{I_{c0}}
```

Note $\hat g_A(0)=0$, $\hat g_A'(0)=-1$, and the upper root is $u_+=\alpha_S$, which is a fully resistive self-sustaining state iff $\alpha_S>1$ — the classical Stekly cryostability criterion recovered as a statement about root position.

**Silo B.** The Grafstein potassium hypothesis, formalized by Tuckwell and Miura and expressed in Nicholson's extracellular-space variables, models SD as autocatalytic K⁺ release into a tortuous extracellular volume fraction $\alpha$ opposed by Na⁺/K⁺-ATPase uptake:

```math
\partial_t K = D_K^{*}\,\partial_x^{2}K+\frac{1}{\alpha}\Bigl[J_{rel}(K)-J_{pump}(K)\Bigr],
\qquad D_K^{*}=\frac{D_K}{\lambda_t^{2}}
```

```math
J_{rel}(K)=j_0+j_r\frac{K^{2}}{K_r^{2}+K^{2}},
\qquad
J_{pump}(K)=j_p\frac{K^{2}}{K_p^{2}+K^{2}}
```

With $r\equiv\bigl(J_{pump}'-J_{rel}'\bigr)\big|_{K_{rest}}>0$, $\Delta K\equiv K_r-K_{rest}$, $w=(K-K_{rest})/\Delta K$, $\tau_B=\alpha/r$, $\lambda_B=\sqrt{D_K^{*}\alpha/r}$:

```math
\tau_B\,\partial_t w=\lambda_B^{2}\,\partial_x^{2}w+\hat g_B(w),
\qquad
\hat g_B(w)=\frac{J_{rel}-J_{pump}}{r\,\Delta K}\Big|_{K=K_{rest}+w\Delta K}
```

so that $\hat g_B(0)=0$ and $\hat g_B'(0)=-1$ by construction.

**Bridge (V1 — shared operator).** Both systems are now instances of

```math
\tau\,\partial_t u=\lambda^{2}\,\partial_x^{2}u+\hat g(u),
\qquad
\hat g(0)=\hat g(\theta)=\hat g(u_+)=0,\quad \hat g'(0)=-1,\quad \hat g'(u_+)<0,
```

with $(\tau,\lambda,\theta,u_+)=(CA/hP,\ \sqrt{kA/hP},\ 1-I/I_{c0},\ \alpha_S)$ for Silo A and $(\alpha/r,\ \sqrt{D_K^{*}\alpha/r},\ \theta_B,\ w_+)$ for Silo B. The identification is exact; only the constitutive shape of $\hat g$ between its roots differs.

**V2 — Maxwell equal-area stall condition.** Setting $u(x,t)=U(\xi)$, $\xi=x-ct$, $U(-\infty)=u_+$, $U(+\infty)=0$ gives $\lambda^2U''+\tau cU'+\hat g(U)=0$. Multiplying by $U'$ and integrating over $\mathbb{R}$ annihilates the boundary terms:

```math
\tau c\int_{-\infty}^{\infty}\!U'^{2}\,d\xi=\int_{0}^{u_+}\hat g(u)\,du
\qquad\Longrightarrow\qquad
\operatorname{sign}(c)=\operatorname{sign}\!\int_{0}^{u_+}\hat g(u)\,du .
```

*Silo A closed form.* With $u_+=\alpha_S$ and $\int_{\theta_A}^{1}\varphi_A\,du=(1-\theta_A)/3$:

```math
\int_0^{\alpha_S}\!\hat g_A\,du=\alpha_S\Bigl[\tfrac{1-\theta_A}{3}+\alpha_S-1\Bigr]-\tfrac{\alpha_S^{2}}{2}=0
\;\Longleftrightarrow\;
\alpha_S=\tfrac{4+2\theta_A}{3}.
```

Writing $i=I/I_{c0}$, $\alpha_S=\alpha_0 i^{2}$ with $\alpha_0=\rho_m I_{c0}^{2}/(A_m hP(T_c-T_{op}))$ and $\theta_A=1-i$, the minimum propagating current solves

```math
\alpha_0 i_p^{2}+\tfrac{2}{3}i_p-2=0
\qquad\Longrightarrow\qquad
i_p=\frac{-\tfrac{2}{3}+\sqrt{\tfrac{4}{9}+8\alpha_0}}{2\alpha_0},
```

which is the cold-end recovery / minimum-propagating-current criterion in closed form.

*Silo B closed form.* The same condition, written in the neurophysiologist's variables and evaluated with the Hill-2 forms above ($\Delta=K_+-K_{rest}$):

```math
\int_{K_{rest}}^{K_+}\!\bigl[J_{rel}-J_{pump}\bigr]dK
=(j_0+j_r-j_p)\Delta
-j_rK_r\Bigl[\arctan\tfrac{K}{K_r}\Bigr]_{K_{rest}}^{K_+}
+j_pK_p\Bigl[\arctan\tfrac{K}{K_p}\Bigr]_{K_{rest}}^{K_+}=0 .
```

This is the SD abort threshold: pharmacological or metabolic manipulations that drive this integral through zero reverse the sign of $v_{SD}$, exactly as reducing $I$ through $I_p$ reverses NZPV. In the step-source adiabatic limit the Silo A branch reproduces Wilson's $v=(J_m/C)\sqrt{\rho_m k/(T_t-T_{op})}$ with $T_t=(T_c+T_{cs})/2$; in the cubic reduction $\hat g=a\,u(u-\theta)(1-u)$ the Silo B branch reproduces the Nagumo speed $c=(\lambda/\tau)\sqrt{a/2}\,(1-2\theta)$.

**V3 — Unstable stationary nucleus.** Stationary solutions of $\lambda^2U''+\hat g(U)=0$ decaying to $0$ obey the first integral

```math
\tfrac{\lambda^{2}}{2}\,U'^{2}+\hat G(U)=0,\qquad \hat G(U)=\int_0^{U}\hat g(s)\,ds,
```

so the nucleus peak $u_p$ is fixed by $\hat G(u_p)=0$ — a second, *local* equal-area condition distinct from the global one in V2.

*Silo A.* Taking the step-source idealization $G=G_{max}=\rho_mJ_m^2A_m/A$ inside the zone and neglecting cooling there, $kT''=-G_{max}$ with $T(\pm\ell)=T_{op}$ gives $T(x)=T_{op}+\tfrac{G_{max}}{2k}(\ell^{2}-x^{2})$, and imposing $T(0)=T_c$:

```math
\ell_{MPZ}=\sqrt{\frac{2kA\,(T_c-T_{op})}{\rho_m J_m^{2}A_m}}
\;\xrightarrow{\;A_m/A\to1\;}\;
\Bigl[\tfrac{2k(T_c-T_{op})}{\rho_m J_m^{2}}\Bigr]^{1/2},
```

Wilson's standard MPZ estimate.

*Silo B.* The same quadrature, with the half-width measured to half-peak to avoid the logarithmic tail divergence:

```math
\ell^{*}=\lambda_B\!\int_{w_p/2}^{w_p}\frac{dw}{\sqrt{-2\hat G_B(w)}},
\qquad \hat G_B(w_p)=0,
\qquad \lambda_B=\sqrt{D_K^{*}\alpha/r}.
```

Linearization about the two stable roots gives the tail decay lengths $\lambda_-=\lambda$ and $\lambda_+=\lambda/\sqrt{|\hat g'(u_+)|}$ on both sides; write $\lambda_{tail}=\max(\lambda_-,\lambda_+)$.

**V4 — Shared Lyapunov functional and mountain-pass content.** Both PDEs are $L^2$ gradient flows. In Silo A variables (constant $k$; for temperature-dependent $C$ the flow is gradient in the $C$-weighted metric):

```math
F_A[T]=\int\Bigl[\tfrac{k}{2}(\partial_xT)^{2}-\!\int_{T_{op}}^{T}\!\Bigl(G(s;I)-\tfrac{hP}{A}(s-T_{op})\Bigr)ds\Bigr]dx,
\qquad C\,\partial_tT=-\frac{\delta F_A}{\delta T}.
```

In Silo B variables:

```math
F_B[K]=\int\Bigl[\tfrac{D_K^{*}\alpha}{2}(\partial_xK)^{2}-\!\int_{K_{rest}}^{K}\!\bigl(J_{rel}(s)-J_{pump}(s)\bigr)ds\Bigr]dx,
\qquad \alpha\,\partial_tK=-\frac{\delta F_B}{\delta K}.
```

In both cases $dF/dt=-\!\int\!\rho_{\!*}(\partial_t\cdot)^{2}dx\le0$ with $\rho_{\!*}\in\{C,\alpha\}$, so $U_c$ is the mountain-pass saddle separating the rest basin from the propagating branch. The *operationally measured* threshold in each field is not $\Delta F$ but the stored-quantity content of $U_c$ — the enthalpy and the ion content respectively:

```math
E_{MQE}=A\!\int\!\Bigl[\int_{T_{op}}^{U_c(x)}\!C\,dT\Bigr]dx
\qquad\longleftrightarrow\qquad
Q^{*}=\alpha\!\int\bigl(K_c(x)-K_{rest}\bigr)\,dV,
```

$Q^{*}$ being precisely the threshold number of moles of KCl in a focal microinjection. The two integrands are the densities conjugate to the diffusing potential in each PDE, which is what makes the type reconciliation $C(T-T_{op})\leftrightarrow\alpha(K-K_{rest})$ forced rather than chosen.

**V5 — Generation-to-clearance capacity ratio, unit threshold.** In Silo A, $\alpha_S=\rho_mJ_m^{2}A_m/(hP(T_c-T_{op}))$ is exactly the nondimensional upper root $u_+$, and $\alpha_S\le1$ places that root below the normal transition: no self-sustaining resistive zone. In Silo B, since $J_{rel}-J_{pump}\to j_0+j_r-j_p$ as $K\to\infty$, the upper root exists iff

```math
\Pi\equiv\frac{j_0+j_r}{j_p}>1 .
```

Both parameters are (peak generation capacity)/(clearance capacity at the reference excursion), both have threshold exactly unity in their own nondimensionalization, and both control the sign of the V2 integral. **Where the correspondence stops:** Silo A's removal term is linear (Newton cooling), so the upper root always exists and $\alpha_S=1$ marks its *position*; Silo B's removal saturates, so $\Pi=1$ marks its *existence*. The dimensionless statement "no self-sustaining upper state below unity" is shared; the mechanism producing it is not.

**V6 — Diffusion-free core dose integral (holds only under flux factorization).** At the core of a fully developed zone, diffusion is negligible and the local balance is a separable ODE on both sides.

*Silo A:* $C(T)\,dT/dt=\rho_m(T)J_m(t)^{2}$, hence

```math
\Gamma_A=\int_0^{t_f}\!\Bigl(\tfrac{J_m(t)}{J_{op}}\Bigr)^{2}dt
=\frac{1}{J_{op}^{2}}\int_{T_{op}}^{T_{hot}}\frac{C(T)}{\rho_m(T)}\,dT ,
```

the MIITs / quench-integral hot-spot criterion: a path-independent state function of the peak temperature.

*Silo B:* under the pump-limited factorization $\alpha\,dK/dt=-m(t)\,J_{pump}(K)$, with $m(t)\in[0,1]$ the ATP availability,

```math
\Gamma_B=\int_0^{t_f}\!m(t)\,dt=\alpha\!\int_{K_{rest}}^{K_{hi}}\frac{dK}{J_{pump}(K)} ,
```

so the clinically recorded depolarization duration is likewise a path-independent state function of the peak ionic excursion. The correspondence requires the flux to factorize into (time-dependent drive) × (function of state) on both sides; it fails where $m$ itself depends on $K$.

## 4. ASYMMETRIC METHODOLOGICAL TRANSFER & SCIENTIFIC HYPOTHESIS

*   **Preferred Transfer Direction:** Applied superconductivity / magnet quench protection → experimental and clinical cortical spreading depolarization.

*   **Asymmetric Maturity Rationale:** For this exact operator class, superconductivity has built, over roughly sixty years, an *instrumented metrology and protection-decision* stack on top of the bistable ignition PDE: Wilson–Dresner MPZ/MQE theory; the calibrated heater-pulse protocol that measures minimum quench energy as a two-dimensional map over pulse energy and pulse duration on instrumented short samples; the Stekly and cold-end-recovery criteria used as quantitative design rules rather than descriptions; the MIITs hot-spot integral tied to a hard design limit; and detection architectures specified as threshold voltage plus validation window with an explicitly budgeted false-trigger rate. The SD field is genuinely mature elsewhere — multi-ion biophysical models with explicit Na⁺/K⁺/Cl⁻/glutamate dynamics and cell swelling (Kager–Wadman–Somjen, Hübel–Ullah), bifurcation analysis of SD wave models, and standardized clinical ECoG detection of DC shifts under COSBID recommendations — and it is *not* less sophisticated at PDE analysis, which is the shared asset here, not the transferable one. The narrow, specific capability it lacks: no calibrated stimulus-energy threshold metrology (an $E_{MQE}$-equivalent energy–duration map), no tissue-calibrated $\Gamma_B$ converting recorded depolarization duration into a predicted peak local excursion, and consequently no protection-decision architecture with a quantified false-positive budget. SD "threshold" is still reported as a preparation-specific KCl volume or stimulation charge.

*   **Target Bottleneck Mitigation:** Hypothesis — the operational bottleneck in SD research and neurocritical monitoring is that propagate-versus-abort cannot presently be predicted for a given focal depolarization in a given cortex, because the threshold is treated as a fixed injected volume rather than as the mountain-pass content $Q^{*}$ of a nucleus whose size depends on how close the tissue sits to the equal-area stall condition. Importing the MQE energy–duration ladder protocol (V4), the equal-area stall criterion (V2) and the $\Gamma$ dose integral (V6) replaces that fixed volume with a two-parameter criterion in $(\lambda_{tail},v_{SD})$, both independently measurable at the bedside or bench from the K⁺ front profile and the propagation delay between adjacent electrodes.

*   **Falsifiable Prediction:** In urethane-anesthetized rat neocortex with an open cranial window, K⁺-selective microelectrode plus intrinsic-optical-signal imaging, and SD induced by focal KCl microinjection through a calibrated micropipette of controlled radius, grade $v_{SD}$ over at least a 4-fold range (nominally 6 → 1.5 mm min⁻¹) across ≥5 conditions by superfusion with graded low-dose ouabain or graded hypoxia. Near the stall condition the critical nucleus is two interacting fronts whose stationarity requires $\tau c=B\,e^{-L^{*}/\lambda_{tail}}$, so $L^{*}=\lambda_{tail}\ln\!\bigl(B/\tau c\bigr)$ and, independent of the unknown prefactor, $L^{*}(v_1)-L^{*}(v_2)=\lambda_{tail}\ln(v_2/v_1)$. **Prediction:** the minimum initiation half-length regressed on $\ln(1/v_{SD})$ is linear with $R^{2}\ge0.9$ and slope equal, within 25%, to $\lambda_{tail}$ measured independently from the exponential leading edge of the $[\mathrm{K^+}]_e$ front; a 4-fold speed reduction must raise $L^{*}$ by $\lambda_{tail}\ln4=1.386\,\lambda_{tail}$, i.e. 0.28–0.83 mm for the reported $\lambda_{tail}\approx0.2$–0.6 mm. The named baseline it must beat is the speed-independent fixed-critical-volume (fixed threshold charge) criterion in standard use for SD induction, which predicts slope zero. **Falsified if** the regression slope is statistically indistinguishable from zero, or differs from the independently measured $\lambda_{tail}$ by more than 25%, or if $L^{*}$ varies with $v_{SD}$ non-logarithmically (e.g. as a power law) over the tested range. **Corollary, conditional on the cubic reduction $\hat g=a\,u(u-\theta)(1-u)$ only:** stall ($c=0$) occurs at $\int_0^1\hat g=0\Leftrightarrow\theta=1/2$, predicting that SD aborts when the measured threshold $[\mathrm{K^+}]_{e,\theta}$ reaches the midpoint of the rest-to-plateau excursion — 29–31 mM for $K_{rest}=3$ mM and a 55–60 mM plateau. Falsified if abort is observed with $\theta$ outside 0.40–0.60 in tissue where the source is verified single-field and cubic-like.

## 5. RELEVANT ACADEMIC SEARCH STRINGS FOR VERIFICATION

*   `"minimum propagating zone" AND "minimum quench energy" AND ("cold end recovery" OR "minimum propagating current") AND "equal area"`
*   `"spreading depolarization" AND ("Tuckwell-Miura" OR "extracellular potassium reaction-diffusion") AND ("critical nucleus" OR "threshold initiation volume") AND "front velocity"`
*   `("spreading depolarization" OR "spreading depression") AND ("quench propagation" OR "normal zone propagation" OR "minimum quench energy" OR "Stekly")` — deliberate self-falsification of the pairing claim
*   `("MIITs" OR "quench integral" OR "hot spot temperature") AND ("depolarization duration" OR "cumulative depolarization" OR "neurocritical care")` — self-falsification of the V6 transfer claim
*   `"critical nucleus" AND "logarithmic" AND "front interaction" AND "bistable reaction-diffusion" AND ("spreading depolarization" OR "cortical")` — tests whether the predicted log law has already been applied target-side