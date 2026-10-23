# YOLO11n AOD4 v6 — airborne-object detector

[![Hugging Face](https://img.shields.io/badge/Hugging%20Face-model%20card-ffcc4d)](https://huggingface.co/Seemorgh/yolo11n-aod4-v6)

A **reviewed archival release** of a recovered Ultralytics YOLO11n checkpoint for four airborne-object classes: **airplane, bird, drone, and helicopter**. The checkpoint, original model card, license text, provenance notes, and sanitized notebooks are mirrored under [`release/`](release/).

**This is a historical training artifact, not a field-validated, operational, or safety-certified detector.** The checkpoint is a PyTorch serialized file; load it only in a trusted environment. No raw dataset, original application, live inference system, or private training materials are included.

## Contents

- [`release/best.pt`](release/best.pt) — recovered checkpoint (stored with Git LFS; about 5.5 MB)
- [`release/README.md`](release/README.md) — original Hugging Face model card, preserved byte-for-byte
- [`release/notebooks/01_train_export.ipynb`](release/notebooks/01_train_export.ipynb) — sanitized training and export notebook
- [`release/notebooks/02_eval_tiling_range.ipynb`](release/notebooks/02_eval_tiling_range.ipynb) — exploratory draft without verified execution results
- [`release/NOTEBOOK_REVIEW.md`](release/NOTEBOOK_REVIEW.md) — notebook editing and limitations
- [`release/provenance.json`](release/provenance.json) and [`release/SHA256SUMS`](release/SHA256SUMS) — provenance and release-file checksums
- [`LICENSE`](LICENSE) — preserved GNU AGPL v3 license text

From the repository root, run `cd release && shasum -a 256 -c SHA256SUMS` on macOS (or `sha256sum -c SHA256SUMS` on Linux) to verify the mirrored files after Git LFS download. The checksum for `release/README.md` is retained because that original file is not edited.

## Historically recorded validation results

The reviewed notebook records **mAP50 0.96518** and **mAP50–95 0.66663** on **4,514 validation images** with four-class aggregate results. These figures are historical records, **not** independently reproduced results or drone-only precision, recall, test performance, field reliability, or mobile inference verification.

## Sources, attribution and caveats

- **Canonical model release:** [Hugging Face — Seemorgh/yolo11n-aod4-v6](https://huggingface.co/Seemorgh/yolo11n-aod4-v6)
- **Reviewed release snapshot:** [Hugging Face commit](https://huggingface.co/Seemorgh/yolo11n-aod4-v6/tree/692377dc55f682cbe5fe17fc5944514574ca9b08)
- **Training documentation:** [drone-detection-showcase](https://github.com/Seemorghdev/drone-detection-showcase/blob/main/docs/training-report.md)
- **Dataset attribution:** Airborne Object Detection, *Airborne-Object-Detection-4-AOD4*, version 6, [Roboflow Universe](https://universe.roboflow.com/airborne-object-detection/airborne-object-detection-4-aod4/dataset/6), which declares CC BY 4.0. Dataset images are not redistributed here.

The model release preserves the checkpoint's **AGPL-3.0** designation; the dataset's **CC BY 4.0** declaration is separate. The license notices and historical source review do not independently certify redistribution compliance, original training provenance, exact checkpoint-to-Core-ML equivalence, or on-device inference. The original application remains private.

This GitHub mirror preserves the reviewed public Hugging Face release without importing any Hugging Face repository history. No new experiments or evaluations are implied.
