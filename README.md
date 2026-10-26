# TSquared rPPG Accuracy Statement

This is a deliberately narrow, non-clinical public performance disclosure from TSquared Medical
Devices LLC. It reports aggregate results, failed gates, and material limitations so prospective
customers can evaluate our engineering discipline. It is **not** software, a reproducible
evaluation package, a dataset, or the production implementation.

## What the evidence shows

No current row passes every predeclared commercial gate. The table deliberately shows favorable
same-dataset results beside an unfavorable external result and keeps accuracy separate from
availability.

| Evidence role | People / clips | Participant-macro MAE (95% CI) | Pooled MAE / RMSE | Reference evaluability | Candidate coverage | Max error | Gate outcome |
|---|---:|---:|---:|---:|---:|---:|---|
| Locked older-adult, subject-disjoint, same-dataset cohort | 6 / 12 | 0.30 (0.24–0.34) bpm | 0.29 / 0.43 bpm | **80.25%** | 95.27% | 2.62 bpm | **Fail:** reference evaluability |
| One-person same-dataset recovery | 1 / 2 | 0.73 (CI unavailable) bpm | 0.73 / 1.20 bpm | 100.00% | 98.78% | 5.14 bpm | **Fail:** original locked execution had a software error |
| Historical local post-development descriptive pool | 9 / 18 | 1.02 (0.69–1.39) bpm | 0.96 / 2.48 bpm | 97.35% | 95.57% | 28.10 bpm | Not an independent gate |
| Separate private external single-record test | 1 / 1 | 12.42 (CI unavailable) bpm | 12.42 / 15.19 bpm | 100.00% | 97.24% | 55.10 bpm | **Fail:** accuracy |

The six-person locked cohort completed all 12 recordings and had no error above 2.63 bpm among
accepted, reference-evaluable windows. It nevertheless failed because 78 of 395 windows had an
ambiguous contact reference under the frozen policy, leaving 76.46% end-to-end yield. Eleven of
12 videos also emitted one or two MPEG-4 decoder error lines. Those facts cannot be omitted when
quoting the low MAE.

The private external record is equally important: 26 accepted windows exceeded 20 bpm error and
four exceeded 30 bpm. This demonstrates a major domain-generalization gap. The underlying
identifiable sample is not redistributed or demonstrated; only the non-identifying failure
aggregate is disclosed. Current evidence does not support a population, production, device-class,
clinical, diagnostic, pediatric, pigmentation, or medical-use accuracy claim.

## What is disclosed

- aggregate, non-subject-level positive and negative benchmark results;
- the scope, denominators, evidence role, failed gate, and material limitations of each result;
- source attribution; and
- a clear description of what a paid feasibility or private validation engagement can deliver.

## What is intentionally not included

- production face tracking, landmark stabilization, or skin-region construction;
- metric, reporting, or disclosure-audit source code and tests;
- frame-quality and signal-quality thresholds;
- temporal filtering, uncertainty, containment, or reacquisition implementation;
- deep-model adapters, state handling, checkpoints, or model weights;
- dataset acquisition, synchronization, preprocessing, or cohort tooling;
- raw video, contact signals, subject identifiers, or window-level results;
- confidential client or TSquared product information; and
- any clinical, diagnostic, regulatory, or medical-performance claim.

Those elements are TSquared's private engineering work and are scoped through the agency after a
client's data, intended use, reference system, confidentiality needs, and acceptance criteria are
understood.

The retained private evidence package contains the exact aggregate tables, subject-clustered
interval calculation, integrity hashes, software tests, and source records used to prepare this
statement. Qualified customers may request a controlled evidence review under an appropriate
commercial scope and confidentiality agreement. The retained material is not publicly
redistributed.

## Work with TSquared

TSquared offers bounded rPPG and physiological-signal engagements through its Upwork agency:

- data, reference, synchronization, and protocol audit;
- reproducible baseline and model benchmarking;
- artifact-rejection, temporal-estimation, and failure-analysis sprint;
- sensor and algorithm verification planning; and
- private implementation under an appropriate contract and NDA when needed.

See [COMMERCIAL_ENGAGEMENT.md](COMMERCIAL_ENGAGEMENT.md). Please contact
[TSquared Medical Devices LLC on Upwork](https://www.upwork.com/agencies/2113634840967276849/)
for project work. GitHub Issues are not a substitute for an engineering engagement.

## Sources and attribution

- MCD-rPPG dataset record: https://huggingface.co/datasets/kyegorov/mcd_rppg
- MCD-rPPG paper: https://doi.org/10.1145/3746027.3758255

No third-party raw data or model binary is redistributed here.
