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
- Optimizer-state controller validation:
  <https://bluear7878.github.io/specdec-joint-report/methods/>
- SafeMove-SD v0.2 Stage 0/1 engineering result:
  <https://bluear7878.github.io/specdec-joint-report/safemove/>
- Visually structured follow-up method proposal:
  <https://bluear7878.github.io/specdec-joint-report/ideas/>

The ideas page clearly separates completed observations from untested proposals.
Its central visual maps the observed optimizer-state and endpoint evidence to
design requirements, ranked method candidates, falsifiable hypotheses, and
stage-gated experiments.

SafeMove-SD v0.2 passed its implementation identities but was killed at the
frozen engineering gate: its emergency radius bound was active on 92–99% of
steps and exact FP32 AAL fell for all three independent target–drafter pairs.
