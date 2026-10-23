---
language: en
license: agpl-3.0
tags:
- ultralytics
- yolov11
- object-detection
- airborne-objects
pipeline_tag: object-detection
library_name: ultralytics
---
# YOLO11n airborne-object detector — AOD4 v6

Recovered four-class checkpoint: airplane, bird, drone, helicopter. Architecture: Ultralytics YOLO11n; checkpoint version metadata: 8.4.87. This is a historical training artifact, not a field-validated detector.

## Historical results

The retained training notebook records 50 completed epochs and subsequent Core ML export. Its later validation output reports **mAP50 0.9651819355211275** and **mAP50–95 0.66663031065507**, over 4,514 images and 6,369 instances. The checkpoint separately stores mAP50 0.96511 and mAP50–95 0.66650. These records are preserved separately; no new evaluation was performed.

All metrics are four-class aggregate box-detection validation results. They do not establish drone-specific accuracy, held-out test performance, mobile inference success, or field reliability.

## Provenance and limitations

The documentary review reports agreement between all 200 stored epoch metrics and the notebook's 50 training rows within printed rounding precision. This supports same-run origin. No original cloud-to-local checksum receipt was found. The release checksum identifies the recovered bytes only. Exact checkpoint-to-Core-ML equivalence and successful device inference remain unverified.

## Dataset attribution

Airborne Object Detection, *Airborne-Object-Detection-4-AOD4*, version 6, Roboflow Universe. Dataset page declares [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/): https://universe.roboflow.com/airborne-object-detection/airborne-object-detection-4-aod4/dataset/6 . No dataset images are included.

## License and notices

The checkpoint embeds an AGPL-3.0 notice; this release preserves that designation and includes the GNU AGPL v3 text. Framework source: https://github.com/ultralytics/ultralytics/tree/v8.4.87 . No Enterprise agreement or Apache-2.0 relicensing permission was established. Dataset licensing is separate. These notices do not certify redistribution compliance.

## Contents and handling

`best.pt` is the unchanged recovered PyTorch checkpoint. PyTorch checkpoint formats may contain serialized executable objects; use only in a trusted environment. Sanitized training and exploratory evaluation notebooks are included under `notebooks/`; see `NOTEBOOK_REVIEW.md` for edits and limitations. No credentials, dataset, Core ML asset, or operational integration is included. Static string inspection found no credential-like match in checkpoint metadata; it retains generic training paths. No model loading, inference, training, conversion, or evaluation was performed for packaging.

Documentation: https://github.com/Seemorghdev/drone-detection-showcase/blob/main/docs/training-report.md
Portfolio: https://mehridian.tech/projects/small-object-reference#recorded-training-results

## Reviewed notebooks

- [Training and Core ML export](notebooks/01_train_export.ipynb): sanitized code with a labeled summary of historical outputs; original raw outputs excluded.
- [Exploratory evaluation draft](notebooks/02_eval_tiling_range.ipynb): no retained execution evidence. Image-level counts are not precision/recall or false-positive measurements; increased prediction frequency does not validate tiling.
- [Review and sanitization notes](NOTEBOOK_REVIEW.md). Neither notebook was executed for this release.
