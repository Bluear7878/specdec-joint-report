# Independent target–drafter interference report and research ideas

Public HTML version of the Korean research report on target-update interference
when a draft-aware loss is applied to an independent pretrained AR target.

The streamlined report centers on four audited visuals:

- the intervention-to-outcome motivation chain with all 21 endpoint seeds;
- the new same-state AdamW `CE+aux` versus `CE-only` shadow experiment;
- the full five-task target-only downstream contrast;
- the target-quality versus exact-acceptance trade-off.

The central result is that the auxiliary term directly changes the applied
target update and Adam moments, while matched endpoint experiments show worse
target NLL in 21/21 seeds and lower downstream macro accuracy in 19/21 seeds.
The report distinguishes this repeated negative transfer from a universal or
catastrophic gradient-failure law.

Public pages:

- Completed evidence report: <https://bluear7878.github.io/specdec-joint-report/>
- Draft-Aware QAT v0.3 target-live and v0.2 quantization report:
  <https://bluear7878.github.io/specdec-joint-report/draft-aware-qat/>
- CT-EPR v0.12 exact cross-swap evidence and prospective-method boundary:
  <https://bluear7878.github.io/specdec-joint-report/ct-epr-v012/>
- Optimizer-state controller validation:
  <https://bluear7878.github.io/specdec-joint-report/methods/>
- SafeMove-SD v0.2 Stage 0/1 engineering result:
  <https://bluear7878.github.io/specdec-joint-report/safemove/>
- ARR v0.1 shared-mass responsibility engineering result:
  <https://bluear7878.github.io/specdec-joint-report/arr/>
- Coordinate-only ARR v0.2 engineering result:
  <https://bluear7878.github.io/specdec-joint-report/coordinate-arr/>
- Visually structured follow-up method proposal:
  <https://bluear7878.github.io/specdec-joint-report/ideas/>

The ideas page clearly separates completed observations from untested proposals.
Its central visual maps the observed optimizer-state and endpoint evidence to
design requirements, ranked method candidates, falsifiable hypotheses, and
stage-gated experiments.

The Draft-Aware QAT page now leads with the completed v0.3 target-live β-dose
audit. Its frozen decision is `motivation_not_established_no_exact_gain`:
teacher-forced Hybrid-LK overlap increased at β 0.1/0.3/1.0, but FP32-eager
exact acceptance and AAL point estimates decreased at every dose. Macro target
NLL stayed inside the frozen margin while β=1 harmed WikiText-2 NLL by 0.0157,
showing domain redistribution. A post-hoc non-mutating six-way cross-swap found
positive conditional target and draft acceptance legs in 0/3 doses each. Those
legs are descriptive checkpoint effects, not causal mediation. The earlier v0.2
quantization-shock and sequential-recovery evidence remains on the same page.

SafeMove-SD v0.2 passed its implementation identities but was killed at the
frozen engineering gate: its emergency radius bound was active on 92–99% of
steps and exact FP32 AAL fell for all three independent target–drafter pairs.

ARR v0.1 reproduced the raw joint target-quality/acceptance trade-off, reduced
the raw target NLL harm by 79–104%, but was also killed: target non-inferiority,
exact-AAL, and component-Pareto gates failed on engineering seed 99. Selection
seeds 6–8 remain sealed. A post-hoc objective decomposition identifies the
dense frozen-target conditional anchor as the next mechanism to isolate; the
coordinate-only successor was therefore advanced to a separate Stage-0/1 panel.

Coordinate-only ARR v0.2 then removed that dense conditional anchor and passed
the frozen target-NLL non-inferiority, decomposition, bidirectional-path,
cross-swap, identity, and cost checks. It was nevertheless killed at engineering
seed 99 because exact AAL improved for only one of three pairs and component
Pareto support also failed. Selection seeds 6–8 remain sealed.

The v0.12 retrospective exact cross-swap screen isolates an especially useful
continuation signal. Under single-domain UCR, the conditional target checkpoint
leg was negative in 3/3 engineering pairs while the draft checkpoint leg was
positive in 3/3; WCR was mixed. The CT-EPR page makes clear that this supports
the motivation and next design, not CT-EPR efficacy.
