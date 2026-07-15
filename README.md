# Independent target–drafter interference report

Public HTML version of the Korean research report on target-update interference
when a draft-aware loss is applied to an independent pretrained AR target.

The streamlined report centers on three audited visuals:

- the new same-state AdamW `CE+aux` versus `CE-only` shadow experiment;
- the full five-task target-only downstream contrast;
- the target-quality versus exact-acceptance trade-off.

The central result is that the auxiliary term directly changes the applied
target update and Adam moments, while matched endpoint experiments show worse
target NLL in 21/21 seeds and lower downstream macro accuracy in 19/21 seeds.
The report distinguishes this repeated negative transfer from a universal or
catastrophic gradient-failure law.

Read the report at <https://bluear7878.github.io/specdec-joint-report/>.
