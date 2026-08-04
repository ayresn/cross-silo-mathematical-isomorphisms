---
sid_metadata:
  entry_id: "SID-053"
  schema_version: "1.0-production"
  maturity_stage: "candidate"
provenance:
  company: "Anthropic"
  model_family: "Claude"
  model_version: "Opus 5"
  generation_timestamp: "2026-08-03"
  prompt_type: "unsupervised-structural-isomorphism-discovery"
isomorphism_metadata:
  domain_a: "computational-lithography-proximity-effect-correction"
  domain_b: "laser-powder-bed-fusion-scan-path-design"
  structural_family: "thresholded-greens-kernel-inverse-design"
  triple_correspondence_vectors:
    - "governing_integral_operator"
    - "boundary_conditions"
    - "dimensionless_similarity_parameters"
    - "instability_mechanism"
    - "numerical_solution_family"
discovery_rationale:
  why_not_obvious: "historically_isolated_communities / distinct_disciplinary_language / incompatible_ontologies (wave-optical and electron-scattering imaging theory vs. Stefan-type phase-change thermodynamics)"
prior_discovery_metrics:
  # NOTE: All scores below are model-generated self-assessments produced at generation time.
  # They reflect the generating model's internal pattern-matching confidence, not externally
  # validated measurements. They should be used as triage-ranking signals for human reviewers
  # deciding which entries to prioritize for Stage 2 bibliometric validation — not as evidence
  # that the isomorphism is real or novel.
  structural_isomorphism_score: 8.6
  vocabulary_divergence_score: 9.1
  expected_methodological_transfer_score: 8.8
  community_separation_score: 8.9
  representation_mismatch_score: 6.4
  expected_transfer_effort: "medium"
  novelty_prior:
    estimate: 7.2
    uncertainty: "±1.6"
relationship_type: "candidate_structural_isomorphism"
validation_status:
  operator_equivalence_confidence: "high"
  constitutive_equivalence_confidence: "medium"
  primary_failure_risk: "constitutive_law_mismatch — the thermal kernel is shift-invariant and linear only under constant-property, quasi-steady conditions; temperature-dependent conductivity, latent heat, Marangoni recirculation, and the abrupt absorptivity change at keyhole onset all break superposition, which is the load-bearing assumption of the entire correction machinery"
  bibliometric_validation: "pending"
---

# INTERDISCIPLINARY STRUCTURAL MAPPING: ENTRY 053

## 1. CROSS-SILO SYSTEM DEFINITION

*   **Silo A (Field 1):** Computational lithography — specifically electron-beam proximity effect correction (PEC) and inverse lithography technology (ILT), where a written dose field is deliberately non-uniform so that the blurred latent energy image crosses the resist development threshold exactly on the target contour, despite long-range backscatter coupling between features that are geometrically far apart.
*   **Silo B (Field 2):** Laser powder bed fusion (LPBF) scan-path and process-parameter design, where a delivered laser energy field must drive the peak temperature across the melting isotherm exactly on the intended part contour, despite inter-hatch and inter-layer heat accumulation coupling regions of the cross-section that are geometrically far apart.
*   **Mathematical Isomorphism:** Both systems are the *same* forward map — a non-negative control density acted on by a compact, shift-invariant, two-scale Gaussian Green's kernel and then cut by a hard level set — so that their **governing integral operators** coincide term-by-term (short-range forward-scatter Gaussian ↔ melt-pool-scale diffusion Gaussian; long-range backscatter pedestal ↔ part-scale heat accumulation pedestal), their **boundary conditions** coincide (the manufactured object is an implicitly defined isocontour of the smoothed field, subject to a non-negative, rule-constrained admissible control set), their **dimensionless similarity parameters** coincide (the implicit-function-theorem edge-placement sensitivity group and the resolution ratio of feature size to kernel width), their **instability mechanism** coincides (surface-tension-driven breakup of slender threshold-defined lines), and their **numerical solution family** coincides (sigmoid-relaxed adjoint gradient descent on a level-set-parameterized control field).

## 2. DIAGNOSTIC VOCABULARY MATRIX

*   **Backscatter proximity effect / pattern-density loading** ↔ **Inter-hatch and inter-layer heat accumulation ("thermal history effect")**
    *   *Operator Role:* Both are the long-range, low-amplitude tail of the shift-invariant kernel — the dense off-diagonal blocks of the same convolution matrix. Each makes the field at a point a functional of the *pattern density averaged over a radius β* rather than of the local control value, which is precisely why per-feature parameter tables fail identically in both fields.
*   **Mask Error Enhancement Factor (MEEF)** ↔ *(no established LPBF term; proposed* **thermal MEEF** *)*
    *   *Operator Role:* Identical implicit-function-theorem object. Differentiating the level-set condition `F(x) = θ` gives edge displacement `δx = −(∂F/∂u · δu)/|∇F|` evaluated on the contour. In litho this is the ratio of field-to-mask gain over image gradient; in LPBF it is the ratio of temperature-to-energy gain over the thermal gradient. Same derivation, same amplification pathology.
*   **Normalized Image Log-Slope (NILS)** ↔ **Melt-pool boundary thermal gradient G (K·mm⁻¹)**
    *   *Operator Role:* Both are the normalized magnitude of the normal derivative of the smoothed field at the threshold isocontour, and both set the noise-to-edge-placement transfer gain. Note the asymmetry this exposes: LPBF already *measures* G routinely, but uses it exclusively for G–R solidification-microstructure maps, never as a geometric-fidelity budget term.
*   **Bossung curves / dose–focus process window** ↔ **Power–velocity (P–V) processing map**
    *   *Operator Role:* Both are the level-set family of critical dimension over a two-parameter control plane, and the usable window in both is constructed by the identical common-overlap operation on CD-tolerance bands (depth-of-focus ↔ usable P–V area).
*   **GHOST background-equalization exposure / sub-resolution assist feature** ↔ *(proposed)* **Defocused sub-fusion complementary preheat pass**
    *   *Operator Role:* An auxiliary, strictly sub-threshold control placed on the *complement* of the target support, whose only function is to flatten the long-range pedestal so that the short-range kernel alone determines contour placement. Because both control fields are non-negativity-constrained, this complement-exposure construction — not negative-amplitude assist features — is the admissible pedestal-cancellation operator in both domains.
*   **High-aspect-ratio resist line collapse** ↔ **Balling / Plateau–Rayleigh melt-track breakup**
    *   *Operator Role:* Both are capillary instabilities of a slender line whose cross-section is defined by the threshold contour and whose base wets a substrate; both linearize to the same dispersion relation with the same wetting-angle-modified critical wavelength, and in both fields the instability sets the true resolution floor *below* the one implied by the kernel width.

## 3. CORE MATHEMATICAL PARALLELISM

Silo A models patterning as a linear energy-deposition convolution followed by a hard threshold. In electron-beam lithography the point exposure distribution is the canonical double Gaussian — a narrow forward-scatter core of width `α` plus a broad backscatter pedestal of width `β` carrying energy fraction `η`:

```math
\psi(r)\;=\;\frac{1}{\pi\,(1+\eta)}\left[\frac{1}{\alpha^{2}}\,e^{-r^{2}/\alpha^{2}}\;+\;\frac{\eta}{\beta^{2}}\,e^{-r^{2}/\beta^{2}}\right]
```

The latent image and the printed pattern are then

```math
E(\mathbf{x})=(\psi * D)(\mathbf{x}),\qquad \mathcal{P}[D]=\{\mathbf{x}\;:\;E(\mathbf{x})\ \ge\ E_{\mathrm{th}}\},
```

and the industrial inverse problem (PEC, generalized to ILT) is the sigmoid-relaxed, regularized, adjoint-differentiated program

```math
\min_{D\,\in\,\mathcal{A}}\;\Big\|\,\sigma_\kappa\!\big(\psi * D-E_{\mathrm{th}}\big)-\chi_{T}\Big\|_{2}^{2}\;+\;\lambda\,R[D],
\qquad \mathcal{A}=\{D\ge 0\}\cap\{\text{rule checks}\}.
```

Silo B models fusion as a moving-source heat conduction problem with a phase-change threshold. In the quasi-steady frame of a source translating at speed `v`,

```math
\rho c_p\!\left(\frac{\partial T}{\partial t}-v\,\frac{\partial T}{\partial \xi}\right)=\nabla\!\cdot\!\big(k\,\nabla T\big)+q(\mathbf{x},t),
```

whose Rosenthal–Eagar–Tsai Green's-function solution is a convolution of the deposited power density against a Gaussian heat kernel,

```math
T(\mathbf{x},t)-T_{0}=\int_{0}^{t}\!\!\int_{\Omega} G(\mathbf{x}-\mathbf{x}',t-t')\,q(\mathbf{x}',t')\,d^{3}x'\,dt',
\qquad
G=\frac{\exp\!\big[-|\mathbf{x}-\mathbf{x}'|^{2}/4\alpha_{\mathrm{th}}(t-t')\big]}{\rho c_p\,\big[4\pi\alpha_{\mathrm{th}}(t-t')\big]^{3/2}},
```

with the fused solid defined by the peak-temperature level set `\mathcal{F}=\{\mathbf{x}:\max_t T \ge T_m\}`. The structural payoff is that reducing this to the build plane — integrating the 3D kernel over the fast intra-track timescale and separately over the slow inter-layer timescale — yields an effective planar kernel that is *literally the same functional form* as `\psi`:

```math
\Psi_{\rm th}(r)\;\simeq\;\frac{A_{\rm eff}}{\pi\,(1+\eta_{\rm th})}\left[\frac{1}{\alpha_{\rm mp}^{2}}\,e^{-r^{2}/\alpha_{\rm mp}^{2}}\;+\;\frac{\eta_{\rm th}}{\beta_{\rm part}^{2}}\,e^{-r^{2}/\beta_{\rm part}^{2}}\right],
\qquad
\mathcal{F}=\{\mathbf{x}:(\Psi_{\rm th}*q_{\rm areal})(\mathbf{x})\ \ge\ T_m-T_0\},
```

where `α_mp ≈ √(4α_th τ_dwell)` is the melt-pool-scale diffusion length and `β_part` is the inter-layer accumulation length. The two forward maps therefore factor identically as `\mathcal{A}\to(\text{compact low-pass smoothing})\to(\text{Heaviside level set})\to(\text{shape manifold})`. In latent-space terms the achievable-geometry manifolds are the images of two non-negative control cones under the *same* rank-deficient compact operator composed with the *same* non-convex threshold: both inherit an identical null space (spatial frequencies beyond the kernel cutoff are unrecoverable regardless of control effort), an identical non-convexity structure (the Heaviside makes both problems multi-modal and forces the same sigmoid homotopy `κ→∞` continuation), and an identical correctability boundary set by control non-negativity rather than by kernel width. The natural dimensionless coordinates on both manifolds are the same two groups:

```math
k_1^{\rm opt}=\frac{\mathrm{CD}\cdot \mathrm{NA}}{\lambda}\ \ \longleftrightarrow\ \ k_1^{\rm th}=\frac{\mathrm{CD}}{\sqrt{4\alpha_{\rm th}\tau_{\rm dwell}}},
\qquad
\mathrm{MEEF}=\frac{\partial F/\partial u}{|\nabla F|}\bigg|_{F=\theta}\ \ (\text{shared definition}).
```

## 4. ASYMMETRIC METHODOLOGICAL TRANSFER & SCIENTIFIC HYPOTHESIS

*   **Preferred Transfer Direction:** Computational Lithography (PEC / ILT) → Laser Powder Bed Fusion Scan-Path Design

*   **Asymmetric Maturity Rationale:** Semiconductor lithography has spent roughly three decades and enormous capital driving this exact operator to production maturity: full-chip model-based OPC and inverse solvers routinely optimize control fields of order 10¹¹ pixels on dedicated accelerator farms; kernels are calibrated against Monte Carlo scattering simulation and metrology; MEEF and NILS are first-class terms in a formal edge-placement-error budget; optical rule checking verifies the corrected control field across the full dose–focus process window; and stochastic (shot-noise) edge roughness is modeled as a variance propagated through the same linearized operator. LPBF occupies the pre-1990 rule-based end of the same technology curve: contour compensation is typically a *single scalar beam offset* applied uniformly — the direct analogue of a 1980s bias table — and geometry-dependent effects are handled by per-feature-class parameter sets (contour, hatch, downskin) established through expensive per-geometry design-of-experiments campaigns. LPBF possesses no model-based correction of the control field, no sensitivity metric linking geometry to dimensional-error variance, and no verification step analogous to ORC. Critically, the *hard* part of the mature toolkit — the kernel calibration infrastructure, the adjoint machinery, the sigmoid homotopy, the rule-constrained projection, the process-window verification loop — is domain-agnostic once the kernel is re-fit, which is why expected transfer effort is medium rather than high.

*   **Target Bottleneck Mitigation:** *Hypothesis.* The persistent LPBF bottleneck of per-geometry process qualification — the requirement to re-run parameter DOEs whenever part geometry changes, because the "correct" laser power for a given feature depends on the rest of the cross-section — is not an irreducible material or machine-noise phenomenon but the exact signature of an uncorrected long-range kernel pedestal. It should therefore be removable by the same operator-level correction that removed it in lithography: fitting `Ψ_th` for a given alloy/machine, then solving the constrained deconvolution `Ψ_th * q = T_m − T_0` on the target contour to produce a spatially varying areal-energy field, should collapse the family of geometry-specific parameter sets into a single calibrated kernel plus a solver.

*   **Falsifiable Prediction:**
    1.  **Single-scalar collapse of optimal energy (primary).** The correct linear energy density for any contour segment is predicted to be a function of exactly one geometric scalar — the `β_part`-radius-weighted local solid fraction `φ` of the surrounding cross-section — via `E_{\rm req}(φ)=E_{\rm th}\big/\!\left(\tfrac12+\eta_{\rm th}\,φ\right)`. Concretely: fabricate a benchmark artifact containing thin walls, cylinders, and overhangs at systematically varied *local density* but *identical local feature width*, and the measured optimum energies must collapse onto this one-parameter curve. Current LPBF practice predicts no such collapse, holding instead that optimum energy is set by feature class and width; a collapse with `R² > 0.9` across feature classes would falsify the prevailing account, and a failure to collapse while the kernel fit is independently validated would falsify this mapping.
    2.  **MEEF-limited uncorrectability.** Contour-error *variance* is predicted to scale as `σ_x² ∝ MEEF_th² · σ_E²`, so a log–log plot of measured contour-error standard deviation against the computed thermal MEEF across a benchmark artifact must have slope 1. This contradicts the current implicit assumption that dimensional scatter is a roughly geometry-independent machine/powder noise floor, and it implies a class of features that *no* scan strategy can correct — a claim with no counterpart in present LPBF literature.
    3.  **GHOST-analogue pedestal flattening.** A defocused, strictly sub-melting complementary pass over the non-part region at areal dose `E_{\rm ghost}=η_{\rm th}E_{\rm th}/(1+η_{\rm th})` should reduce the *spread* of geometry-optimal power across the benchmark artifact by more than half, at fixed density and fixed contour tolerance. Conventional AM reasoning predicts a defocused non-fusing pass mainly perturbs residual stress and offers no dimensional-fidelity benefit.

## 5. RELEVANT ACADEMIC SEARCH STRINGS FOR VERIFICATION

*   `"proximity effect correction" AND "double Gaussian point spread function" AND "mask error enhancement factor"`
*   `"laser powder bed fusion" AND ("Eagar-Tsai" OR "Rosenthal solution") AND "contour offset"`
*   `("inverse lithography" OR "optical proximity correction") AND ("additive manufacturing" OR "powder bed fusion") AND ("dose modulation" OR "scan path optimization")`
*   `"balling instability" AND "Plateau-Rayleigh" AND "pattern collapse" AND "aspect ratio criterion"`