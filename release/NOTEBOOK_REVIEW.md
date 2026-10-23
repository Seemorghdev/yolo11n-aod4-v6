# Notebook review — 22 October 2026

Reviewed both original notebooks as JSON without executing cells or loading the model. Published copies are edited derivatives, not byte-identical original evidence.

## Training/export

The original has saved execution counts and outputs, including a preliminary 3-epoch run, a completed separate 50-epoch run, copied artifact listings and a successful Core ML export message. These remain historical records. Original outputs are excluded to remove raw logs, embedded arrays, private storage identifiers and incidental environment details. A labeled markdown summary preserves the material historical findings. Credential validity or revocation was not tested.

The dependency install was unpinned and environment-specific. Dataset access, environment setup, and file paths require user configuration. No claim of one-click reproduction is made.

## Evaluation draft

Every original code cell has null execution count and no outputs. There are two implemented steps despite the old three-step title; no physical-range estimator. Step 1 buckets the largest annotated box and counts any aerial prediction in the image, without IoU matching or ground-truth class filtering. Step 2 counts frames with aerial predictions on the first candidate clip, without reading annotations. Neither provides validated precision, recall, false-positive rates, a detection floor, or evidence that tiling improves accuracy. Bird predictions are not inherently false positives. The notebooks now state these limits and remove the original unsupported success claims.

## Sanitization and scope

Removed the credential literal, raw outputs, execution counts and original metadata. Replaced cloud/device paths and the unverified external archive locator; corrected contextual comments and metric labels. Retained training settings and exploratory logic. No training, inference, conversion, downloads of evaluation datasets or evaluation was performed.

The root AGPL-3.0 release notice applies to these notebook copies. Dataset CC BY 4.0 attribution is separate and does not certify all underlying rights. No Apache-2.0 relicensing or Enterprise agreement was established. See the root model card and linked documentary report for provenance qualifications.
