# Speculative-decoding joint-training report

Public HTML version of the audited Korean research report on gradient
interference in bidirectional joint training of independent pretrained AR
target and drafter models.

The HTML report includes seven audited experiment figures generated from the
versioned analysis CSVs: target-NLL mitigation, gradient diagnostics,
exploratory HellaSwag, quality-versus-acceptance, cross-swap sensitivity, the
full five-task downstream macro, and task/pretrained-reference heterogeneity.
Detailed numeric tables remain available in collapsible sections beneath the
figures.

In the locked full five-task panel, naive bidirectional target updates reduced
the same-seed downstream macro in 19/21 training seeds and all five pair means;
the norm cap recovered part, but not all, of that loss.

Read the report at <https://bluear7878.github.io/specdec-joint-report/>.
