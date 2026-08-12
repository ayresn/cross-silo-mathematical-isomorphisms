---
sid_metadata:
  entry_id: "SID-0052"
  schema_version: "2.0-production"
  maturity_stage: "candidate"
provenance:
  company: "Anthropic"
  model_family: "Claude"
  model_version: "Opus 5"
  generation_timestamp: "2026-08-12"
  prompt_type: "unsupervised-structural-isomorphism-discovery"
isomorphism_metadata:
  domain_a: "elastohydrodynamic-lubrication-and-rough-surface-contact-tribology"
  domain_b: "subglacial-hydrology-and-hard-bed-glacier-sliding"
  structural_family: "free-boundary-complementarity-with-nonlocal-half-space-compliance"
  triple_correspondence_vectors:
    - "poiseuille_cubic_mobility_reynolds_operator"
    - "half_space_dirichlet_to_neumann_multiplier_elastic_viscous_correspondence"
    - "reynolds_swift_stieber_signorini_complementarity_pair"
    - "mixed_lubrication_load_partition_effective_pressure_identity"
    - "westergaard_complete_contact_similarity_group"
discovery_rationale:
  why_not_obvious: "distinct_disciplinary_language / historically_isolated_communities / eleven_order_of_magnitude_separation_in_characteristic_timescale"
prior_discovery_metrics:
  structural_isomorphism_score: 8.6
  vocabulary_divergence_score: 9.1
  expected_methodological_transfer_score: 8.4
  community_separation_score: 9.3
  representation_mismatch_score: 6.2
  expected_transfer_effort: "medium"
  novelty_prior:
    estimate: 6.8
    uncertainty: "±1.6"
relationship_type: "candidate_structural_isomorphism"
validation_status:
  operator_equivalence_confidence: "high"
  constitutive_equivalence_confidence: "medium"
  primary_failure_risk: "glen_law_nonlinearity_and_regelation_channel_absent_from_the_elastic_kernel"
  bibliometric_validation: "pending"
---

# INTERDISCIPLINARY STRUCTURAL MAPPING: ENTRY 0052

## 1. CROSS-SILO SYSTEM DEFINITION

*   **Silo A (Field 1):** Elastohydrodynamic and mixed lubrication in machine-element tribology — a pressurised liquid film separating two elastically deforming counterfaces, in which the film ruptures into sub-ambient cavities behind the contact and the applied load is partitioned between fluid film and solid asperity contact.
*   **Silo B (Field 2):** Hard-bed glacier sliding and subglacial drainage — temperate ice sliding over rock at a water-pressurised interface, in which the ice separates from the lee of bed bumps to form water-filled cavities, and the ice overburden is partitioned between the water film and the ice–bed contact patches.
*   **Mathematical Isomorphism:** Both systems are governed by the same degenerate thin-film operator $\nabla\!\cdot\!\big(\tfrac{h^{3}}{12\mu}\nabla p\big)$ closed by (i) a half-space Dirichlet-to-Neumann multiplier linear in $|k|$, (ii) a pointwise complementarity condition between gap and normal traction (Reynolds–Swift–Stieber on one side, Signorini on the other), and (iii) an integral load-partition identity; in the linear-viscous limit — or under a linearised Glen rheology, for bed slopes $k\Delta \ll 1$ and wavelengths above Nye's regelation-controlling wavelength — the two closures coincide *exactly* under the substitution $E^{*}\to 4\eta_{\rm eff}u_b|k|$, and the correspondence stops precisely where regelation opens a second compliance channel that has no counterpart in the elastic kernel.

## 2. DIAGNOSTIC VOCABULARY MATRIX

*   **Poiseuille film mobility $h^{3}/12\eta_L$** ↔ **Laminar sheet conductivity $h^{3}/12\mu_w$**
    *   *Operator Role:* Both are the identical scalar mobility coefficient (type: $[\mathrm{m}^{3}\,\mathrm{Pa}^{-1}\mathrm{s}^{-1}]$ per unit width) multiplying the gradient inside the degenerate elliptic operator $\nabla\!\cdot\!\big(\tfrac{h^{3}}{12\mu}\nabla p\big)$; no transformation is required because $\eta_L$ and $\mu_w$ are both dynamic viscosities of the interfacial liquid, and $h$ is the mean local gap in both.
*   **Reduced modulus $E^{*}$** ↔ **Linearised Glen effective viscosity $\eta_{\rm eff}$ at sliding speed $u_b$**
    *   *Operator Role:* Both are the coefficient of $|k|$ in the half-space Dirichlet-to-Neumann map for the normal traction: $\hat\sigma_{zz}=\tfrac{1}{2}E^{*}|k|\hat u_z$ (elastic) and $\hat\sigma_{zz}=2\eta_{\rm eff}|k|\hat w$ (Stokes). Types differ — $E^{*}$ is $[\mathrm{Pa}]$, $\eta_{\rm eff}$ is $[\mathrm{Pa\,s}]$ — and are reconciled by the steady-sliding kinematic closure $\hat w = i k u_b \hat u_z$, giving the explicit dimensional bridge $E^{*} = 4\eta_{\rm eff}u_b|k|$, equivalently $G^{*}=\eta_{\rm eff}u_b|k|$ for incompressible media.
*   **Cavitation pressure $p_{\rm cav}$ with the Reynolds–Swift–Stieber rupture condition** ↔ **Subglacial water pressure $p_w$ at cavity-roof separation**
    *   *Operator Role:* Both are the lower obstacle (type: scalar field, $[\mathrm{Pa}]$) defining the admissible cone in the same variational inequality, $K=\{q:\,q\ge p_{\rm cav}\}$ and $K=\{\sigma:\,\sigma\ge p_w\}$, and both enforce the identical free-boundary regularity $p=p_{\rm obstacle},\ \partial p/\partial n=0$ at the rupture front.
*   **Elrod–Adams fractional film content $\theta$** ↔ **Ice–bed contact indicator $\chi$, with contact fraction $f=\langle\chi\rangle$**
    *   *Operator Role:* Both are the $[0,1]$-valued dimensionless dual variable of the linear complementarity problem, satisfying pointwise $(1-\theta)(p-p_{\rm cav})=0$ and $(1-\chi)(\sigma_{n}-p_{w})=0$ respectively; $\theta$ and $\chi$ have identical mathematical type (bounded measurable indicator/relaxed indicator).
*   **Asperity load share $W_c/W$ in mixed lubrication** ↔ **Effective pressure $N=\bar\sigma_n-p_w$**
    *   *Operator Role:* Both are the integral load-partition constraint that closes the free-boundary problem — in EHL it fixes the rigid-body approach $h_0$, in glaciology it fixes the cavity-size scale. Types differ ($W_c/W$ dimensionless, $N$ in $[\mathrm{Pa}]$) and are reconciled by $W_c/W=N/\bar\sigma_n$, i.e. $N$ is the contact-borne share of the mean normal traction $\bar\sigma_n$ (ice overburden).
*   **Westergaard complete-contact pressure $p^{*}=\pi E^{*}\Delta/\lambda$** ↔ **Cavitation-suppression effective pressure $N^{*}$**
    *   *Operator Role:* Both are the single dimensionless similarity group of the partial-contact problem, $\Pi=\bar p/p^{*}$ and $\Pi=N/N^{*}$, and both enter as the argument of the same closed-form contact-fraction function $f=(2/\pi)\arcsin\sqrt{\Pi}$; $\Delta$ is the roughness/bed amplitude and $\lambda$ its wavelength in both.

## 3. CORE MATHEMATICAL PARALLELISM

**Silo A.** Tribology models a lubricated line contact by coupling three objects. The film pressure $p(x)$ obeys the steady incompressible Reynolds equation, in which a cubic Poiseuille mobility balances the Couette wedge term at entrainment speed $u_m$:

```math
\frac{\mathrm{d}}{\mathrm{d}x}\!\left(\frac{h^{3}}{12\eta_{L}}\,\frac{\mathrm{d}p}{\mathrm{d}x}\right)=u_{m}\,\frac{\mathrm{d}h}{\mathrm{d}x}
```

The gap $h(x)$ is not prescribed: it responds *nonlocally* to the pressure through the plane-strain elastic half-space kernel,

```math
h(x)=h_{0}+\frac{x^{2}}{2R}-\frac{2}{\pi E^{*}}\int_{\Omega}p(x')\,\ln|x-x'|\,\mathrm{d}x',
\qquad \frac{1}{E^{*}}=\frac{1-\nu_{1}^{2}}{E_{1}}+\frac{1-\nu_{2}^{2}}{E_{2}}
```

whose Fourier symbol is the Dirichlet-to-Neumann multiplier

```math
\hat p(k)=\tfrac{1}{2}E^{*}\,|k|\,\hat u_{z}(k).
```

Film rupture is handled by the mass-conserving Elrod–Adams complementarity system in $(p,\theta)$, equivalent to a variational inequality on the cone $K=\{q\in H^{1}:q\ge p_{\rm cav}\}$:

```math
\frac{\partial}{\partial x}\!\left(\frac{h^{3}}{12\eta_{L}}\frac{\partial p}{\partial x}\right)=u_m\frac{\partial(\theta h)}{\partial x},
\qquad p\ge p_{\rm cav},\quad 0\le\theta\le 1,\quad (1-\theta)\,(p-p_{\rm cav})=0,
```

```math
\int_{\Omega}\!\Big[\frac{h^{3}}{12\eta_{L}}\nabla p\cdot\nabla (q-p)-u_m h\,\partial_x (q-p)\Big]\mathrm{d}x\;\ge\;0
\qquad\forall\,q\in K .
```

In mixed lubrication the problem is closed by the load-partition identity, with $p_c\ge 0$ supported on the contact set $\{\chi=1\}$:

```math
\int_{\Omega}\big[\theta\,p+\chi\,p_{c}\big]\,\mathrm{d}x=W,\qquad \frac{W_{c}}{W}=\frac{1}{W}\int_{\Omega}\chi\,p_{c}\,\mathrm{d}x .
```

Finally, for a rigid sinusoid $z=\Delta\cos(2\pi x/\lambda)$ pressed on the half-space, Westergaard's solution gives the contact half-width $a$ per period in closed form:

```math
\frac{\bar p}{p^{*}}=\sin^{2}\!\Big(\frac{\pi a}{\lambda}\Big),\qquad p^{*}=\frac{\pi E^{*}\Delta}{\lambda}
\;\;\Longrightarrow\;\;
f\equiv\frac{2a}{\lambda}=\frac{2}{\pi}\arcsin\sqrt{\bar p/p^{*}} .
```

**Silo B.** Glaciology models the subglacial water sheet with an equation its own community writes independently (Creyts & Schoof; Hewitt; Werder *et al.*'s GlaDS). Mass conservation for sheet thickness $h$ with melt supply $\dot m$, laminar flux, and hydraulic potential $\phi=p_w+\rho_w g z_b$:

```math
\frac{\partial h}{\partial t}+\nabla\!\cdot\!\mathbf{q}=\frac{\dot m}{\rho_{w}},\qquad
\mathbf{q}=-\frac{h^{3}}{12\mu_{w}}\nabla\phi,
```

closed — and this is the surrogate the transfer targets — by a *local, algebraic* opening–closure pair with two tuned constants $h_r,l_r$:

```math
\left.\frac{\partial h}{\partial t}\right|_{\rm mech}=u_{b}\,\frac{h_{r}-h}{l_{r}}\;-\;\frac{2A}{n^{n}}\,h\,N^{n},
\qquad N=\bar\sigma_{n}-p_{w}.
```

Separately, the small-scale glaciological cavity problem (Fowler; Schoof; Gagliardini *et al.*) is posed as a Stokes free-boundary problem with a Signorini condition on the gap $g$ between ice sole and bed, and Glen's law as the constitutive relation:

```math
\nabla\!\cdot\!\boldsymbol{\sigma}=0,\quad \boldsymbol{\sigma}=-p\mathbf{I}+2\eta_{\rm eff}\dot{\boldsymbol{\varepsilon}},\quad
\eta_{\rm eff}=\tfrac{1}{2}A^{-1/n}\dot\varepsilon_{e}^{(1-n)/n},
```

```math
g\ge 0,\qquad \sigma_{n}-p_{w}\ge 0,\qquad g\,(\sigma_{n}-p_{w})=0,
\qquad \bar\sigma_{n}-p_{w}=N .
```

Linearising the Stokes problem about a flat sole with a biharmonic stream function $\psi=(A_{k}+B_{k}z)e^{-|k|z}$ and imposing decay gives $B_k=|k|A_k$ (identically for either perturbed no-slip or perturbed free-slip tangential conditions), whence the viscous half-space Dirichlet-to-Neumann multiplier:

```math
\hat\sigma_{zz}(k)=2\eta_{\rm eff}\,|k|\,\hat w(k).
```

**The bridge.** Comparing the two multipliers term by term identifies the compliance operators. Steady sliding at $u_b$ over a stationary bed advects the ice sole, so $\partial_t\to u_b\partial_x$ and $\hat w=iku_b\hat u_z$; substituting,

```math
\hat\sigma_{zz}=2\eta_{\rm eff}|k|\,(u_{b}|k|\,\hat u_{z})
\;\;\equiv\;\;
\tfrac{1}{2}E^{*}|k|\,\hat u_{z}
\qquad\Longleftrightarrow\qquad
\boxed{\;E^{*}=4\,\eta_{\rm eff}\,u_{b}\,|k|\;}
```

which is dimensionally consistent ($\mathrm{Pa}=\mathrm{Pa\,s}\cdot\mathrm{m\,s^{-1}}\cdot\mathrm{m^{-1}}$) and reduces, for incompressible media where $E^{*}=4G^{*}$, to the elementary correspondence $G^{*}\leftrightarrow\eta_{\rm eff}u_b|k|$. Under this single substitution the four remaining structures map without further transformation: the mobility $h^{3}/12\eta_L\leftrightarrow h^{3}/12\mu_w$ is already identical; the Elrod–Adams pair $(p\ge p_{\rm cav},\,0\le\theta\le1,\,(1-\theta)(p-p_{\rm cav})=0)$ is the Signorini pair $(\sigma_n\ge p_w,\,0\le\chi\le1,\,(1-\chi)(\sigma_n-p_w)=0)$ with $\theta\leftrightarrow\chi$ and $p_{\rm cav}\leftrightarrow p_w$; and the load-partition identity $\int[\theta p+\chi p_c]=W$ becomes $\langle\chi\,\sigma_c\rangle=N$, i.e. *the glaciological effective pressure is the asperity load share of mixed lubrication*.

Propagating the substitution through Westergaard's complete-contact pressure yields a target-side quantity with no glaciological precedent in closed form:

```math
N^{*}=\frac{\pi E^{*}\Delta}{\lambda}\Big|_{E^{*}=4\eta_{\rm eff}u_{b}k}
=2\eta_{\rm eff}u_{b}k^{2}\Delta=\frac{8\pi^{2}\eta_{\rm eff}u_{b}\Delta}{\lambda^{2}},
```

and, inserting Glen's law with the dominant strain-rate invariant $\dot\varepsilon_{e}\simeq u_{b}k^{2}\Delta$ (this is the one $O(1)$ modelling choice in the entry),

```math
N^{*}=A^{-1/n}\big(u_{b}k^{2}\Delta\big)^{1/n}
=\left(\frac{4\pi^{2}u_{b}\Delta}{A\lambda^{2}}\right)^{1/n},
\qquad
f=\frac{2}{\pi}\arcsin\sqrt{N/N^{*}} .
```

The correspondence extends exactly as far as the linear multiplier is valid and stops in three identifiable places, all target-side: (i) $n\ne1$ makes $\eta_{\rm eff}$ state-dependent, so $N^{*}$ inherits an $O(1)$ prefactor ambiguity while the *shape* $f(N/N^{*})$ does not; (ii) $k\Delta\lesssim 1$ is required for the half-space linearisation; (iii) below Nye's controlling wavelength (order $10^{-1}\,\mathrm{m}$) regelation supplies a compliance channel with no elastic counterpart, and the mapping fails there outright rather than degrading.

## 4. ASYMMETRIC METHODOLOGICAL TRANSFER & SCIENTIFIC HYPOTHESIS

*   **Preferred Transfer Direction:** Elastohydrodynamic / mixed-lubrication tribology → Subglacial hydrology and hard-bed sliding laws
*   **Asymmetric Maturity Rationale:** Tribology has spent five decades building solvers for precisely this operator — Reynolds mobility plus $|k|$-multiplier plus complementarity. Specifically: multilevel multi-integration (Brandt–Lubrecht) reducing the dense half-space kernel to $O(N\log N)$ inside full-multigrid cycles with mesh-independent convergence at near-rigid loads; mass-conserving cavitation algorithms (Elrod–Adams, Kumar–Booker) and monolithic Fischer–Burmeister Newton–Schur complementarity solvers with quadratic convergence; and spectral rough-surface contact methods that ingest a measured surface power spectrum directly rather than a single amplitude. Glaciology is genuinely mature elsewhere and this must be stated plainly: nonlinear Stokes and higher-order ice-flow solvers, adjoint inversion for basal traction, mesh adaptivity, and ensemble UQ (Elmer/Ice, ISSM, ISMIP6) are all first-rate, and full-Stokes cavity simulation on real three-dimensional bed patches is an established capability. The narrow missing capability is a *reduced* formulation cheap enough to embed in a drainage model: operational subglacial hydrology replaces the nonlocal contact problem with the local algebraic opening term $u_b(h_r-h)/l_r$, which makes cavity size a purely pointwise function of $N$, introduces two unmeasurable constants $(h_r,l_r)$, and structurally cannot accept a bed roughness spectrum.
*   **Target Bottleneck Mitigation:** Replacing $u_b(h_r-h)/l_r$ with the Fourier multiplier $\hat\sigma_{zz}=2\eta_{\rm eff}|k|\hat w$ evaluated by multilevel multi-integration, and solving the resulting sheet–cavity system as a single Fischer–Burmeister complementarity problem, yields a cavity closure with **zero tuned parameters** whose only input is the measured bed power spectrum $C(k)$. The testable hypothesis: the $(h_r,l_r)$ pair currently absorbs the second moment of $C(k)$, so a spectral half-space closure will reproduce calibrated GlaDS behaviour on smooth synthetic beds while diverging systematically — and correctly — on beds with realistic short-wavelength content, because $N^{*}\propto \Delta/\lambda^{2}$ weights short wavelengths that a single $(h_r,l_r)$ pair cannot represent.
*   **Falsifiable Prediction:** In a cryogenic ring-shear apparatus with temperate ice sliding at $u_b=100\ \mathrm{m\,a^{-1}}$ on a sinusoidal hard bed of $\lambda=0.50\ \mathrm{m}$, $\Delta=0.025\ \mathrm{m}$ ($n=3$, $A=2.4\times10^{-24}\,\mathrm{Pa^{-3}s^{-1}}$), the entry's mathematics gives $N^{*}=(4\pi^{2}u_b\Delta/A\lambda^{2})^{1/3}=1.74\ \mathrm{MPa}$ and hence steady ice–bed contact fractions $f=0.22$ at $N=0.2\ \mathrm{MPa}$, $f=0.36$ at $N=0.5\ \mathrm{MPa}$, and $f=0.55$ at $N=1.0\ \mathrm{MPa}$. The named baseline is the SHMIP-standard local closure (GlaDS, Werder *et al.* 2013, with the benchmark values $h_r=0.1\ \mathrm{m}$, $l_r=2\ \mathrm{m}$), which for the same parameters gives $h/h_r=0.986$ at $N=0.5\ \mathrm{MPa}$ and $0.899$ at $N=1.0\ \mathrm{MPa}$ — an essentially fully-cavitated bed, an absolute discrepancy of $\approx0.35$ in $f$ at $N=0.5\ \mathrm{MPa}$, and the wrong sign of curvature. The transferred law must fit measured $f$ (from direct contact-area imaging or from the pressure-independent component of drag) with RMS error $\le0.05$ over $0.1\le N/N^{*}\le0.9$ using $N^{*}$ as the *single* fitted scale, with the fitted $N^{*}$ within a factor of two of the a-priori $1.74\ \mathrm{MPa}$ (the tolerance is set by the $\dot\varepsilon_e\simeq u_bk^{2}\Delta$ linearisation, not chosen freely). **Falsified if** measured $f$ is better fitted by a straight line in $N/N^{*}$ than by $\tfrac{2}{\pi}\arcsin\sqrt{N/N^{*}}$, or if the fitted $N^{*}$ departs from the a-priori value by more than a factor of two, or if $f$ measured at fixed rms bed slope fails to scale as $\lambda^{-1}$ across a wavelength sweep at $\lambda>0.3\ \mathrm{m}$.

## 5. RELEVANT ACADEMIC SEARCH STRINGS FOR VERIFICATION

*   `"Elrod-Adams" AND "mass-conserving cavitation" AND "multilevel multi-integration" AND "mixed lubrication load sharing"`
*   `"subglacial cavity" AND "Signorini condition" AND "effective pressure" AND ("sheet thickness parameterisation" OR "opening rate" OR "GlaDS")`
*   `("Westergaard" OR "complete contact pressure") AND ("glacier sliding" OR "subglacial cavity") AND "half-space compliance"`  *(deliberate falsification attempt: returns the specific claimed pairing if already published)*
*   `"rough surface contact mechanics" AND "glacier bed roughness spectrum" AND "real contact area fraction" AND ("Persson theory" OR "boundary element")`  *(second falsification attempt, aimed at the spectral-closure claim rather than the sinusoidal one)*
*   `"elastic-viscous correspondence" AND "Dirichlet-to-Neumann" AND "Reynolds equation" AND ("cavitation" OR "film rupture") AND ice`