---
sid_metadata:
  entry_id: "SID-060"
  schema_version: "1.0-production"
  maturity_stage: "candidate"
provenance:
  company: "OpenAI"
  model_family: "GPT"
  model_version: "5.4 Thinking Mini"
  generation_timestamp: "2026-08-03"
  prompt_type: "unsupervised-structural-isomorphism-discovery"
isomorphism_metadata:
  domain_a: "thermoacoustic-combustion-control"
  domain_b: "epileptiform-neural-dynamics"
  structural_family: "delay-coupled-hopf-instabilities"
  triple_correspondence_vectors:
    - "governing_differential_operator"
    - "instability_mechanism"
    - "numerical_solution_family"
discovery_rationale:
  why_not_obvious: "The two communities use incompatible ontologies—acoustic flame coupling versus cortical excitability—and are usually separated by combustion engineering, nonlinear dynamics, and clinical neurophysiology vocabularies. The shared structure only becomes visible at the operator level after reduction to delayed non-selfadjoint feedback systems. Provisional numbering placeholder (060); maintainer should verify against the live directory and renumber if needed before commit."
prior_discovery_metrics:
  structural_isomorphism_score: 8.6
  vocabulary_divergence_score: 9.1
  expected_methodological_transfer_score: 8.9
  community_separation_score: 9.4
  representation_mismatch_score: 8.7
  expected_transfer_effort: "medium"
  novelty_prior:
    estimate: 8.2
    uncertainty: "±1.1"
relationship_type: "candidate_structural_isomorphism"
validation_status:
  operator_equivalence_confidence: "very_high"
  constitutive_equivalence_confidence: "medium"
  primary_failure_risk: "incompatible_boundary_conditions"
  bibliometric_validation: "pending"
---

# INTERDISCIPLINARY STRUCTURAL MAPPING: ENTRY 060

## 1. CROSS-SILO SYSTEM DEFINITION

* **Silo A (Field 1):** Thermoacoustic combustion control of self-excited limit cycles in confined premixed combustors.
* **Silo B (Field 2):** Closed-loop epileptiform neural dynamics governing seizure onset in cortical tissue.
* **Mathematical Isomorphism:** Both systems reduce, after low-order projection, to a delayed, non-selfadjoint feedback operator whose leading complex eigenpair crosses a Hopf boundary; the same post-bifurcation branch structure is then best resolved by pseudo-arclength continuation and Floquet analysis, making the operator, instability, and numerical family correspondences jointly explicit.

## 2. DIAGNOSTIC VOCABULARY MATRIX

* **Flame transfer function** ↔ **synaptic response kernel**

  * *Operator Role:* Each token represents a frequency- and delay-dependent gain map inserted into the feedback term of a linearized evolution operator; mathematically, both act as convolutional response operators that shift the real part and phase of the dominant eigenvalue.
* **Acoustic mode growth rate** ↔ **pre-ictal growth multiplier**

  * *Operator Role:* Each quantity is the instability diagnostic extracted from the monodromy or linearized delay operator; both determine whether the trajectory remains on a stable fixed point or undergoes a Hopf transition to a stable oscillatory attractor.

## 3. CORE MATHEMATICAL PARALLELISM

Thermoacoustic combustors are modeled as coupled acoustic oscillators with delayed heat-release feedback, where the flame acts like a phase-shifting active element that can inject energy into a bounded resonator. The canonical low-order form captures the essential operator-level structure:

```math
\ddot{p}(t)+2\zeta\omega_0\dot{p}(t)+\omega_0^2p(t)=\beta\,\mathcal{Q}\!\left(p(t-\tau)\right)
```

When the delay phase and feedback gain align, the dominant acoustic mode becomes linearly unstable, a Hopf bifurcation produces a self-sustained limit cycle, and continuation methods track the branch while Floquet multipliers quantify its resilience.

Epileptiform seizure onset can be written in the same latent topology after coarse-graining cortical tissue into a delayed neural mass or field model, with synaptic recruitment playing the role of phase-lagged positive feedback. A representative reduced form is:

```math
\tau_m \dot{V}(t)=-V(t)+W\,\sigma\!\left(V(t-\tau_d)\right)+I_{\mathrm{stim}}(t)
```

Here too, sufficiently strong delayed excitation drives the leading eigenpair through the imaginary axis, generating a periodic attractor or pathological oscillation. In latent space, both curves occupy the same center-manifold geometry: a stable fixed point loses hyperbolicity, a limit cycle emerges, and the unstable manifold is best followed by the same continuation-and-multiplier machinery.

## 4. ASYMMETRIC METHODOLOGICAL TRANSFER & SCIENTIFIC HYPOTHESIS

* **Preferred Transfer Direction:** Thermoacoustic combustion control → Epileptiform neural dynamics
* **Asymmetric Maturity Rationale:** Thermoacoustics has a highly mature toolkit for identifying transfer functions, performing reduced-order model calibration, computing adjoint sensitivities, and continuing unstable branches through Hopf points under experimental feedback. Epileptiform control still relies heavily on empirical stimulation schedules, patient-specific heuristics, and less standardized operator-tracking pipelines, so importing the thermoacoustic workflow addresses a concrete analytical gap rather than merely renaming an existing method.
* **Target Bottleneck Mitigation:** If seizure precursors are fit with a delay-operator model and then analyzed using flame-style pseudo-arclength continuation plus Floquet-spectrum tracking, the model should produce a patient-specific instability boundary that can be used to schedule stimulation at phases predicted to remain below the Hopf threshold. That would replace phase-agnostic stimulation with stability-margin-aware control.
* **Falsifiable Prediction:** In a prospective benchmark, stimulation timed to the leading adjoint mode of the fitted delay operator will suppress seizure initiation more effectively than equal-energy random-phase stimulation, and the dominant Floquet multiplier should cross the unit circle before electrographic onset by a reproducible lead time. A null result would show no improvement over phase-random baselines and no predictive pre-ictal multiplier drift.

## 5. RELEVANT ACADEMIC SEARCH STRINGS FOR VERIFICATION

* `"flame transfer function" AND "pseudo-arclength continuation" AND "Floquet multipliers"`
* `"delay neural mass equation" AND "Hopf bifurcation" AND "phase response curve"`