# Evidence gating in retrieval-augmented question answering

Reproducibility materials for **Training Context Construction and Calibration for Evidence Gating in Retrieval Augmented Question Answering**, by Zhe Yang, Jiazhe Wu, Yu Wang, and Chen Yan.

The study compares four training context constructions and independent threshold calibration for evidence gating. These archives preserve the scored HotpotQA experiments, controlled comparisons, external public-label validation on NoMIRACL and SQuAD 2.0, and figure inputs.

| Archive | Contents |
| --- | --- |
| [Supplemental Data S2](archives/Supplemental_Data_S2.zip) | Frozen retrieval inputs and groups, gate scores, shared reader outputs, external validation labels and scores, benchmark source URLs and hashes, and numerical reproduction code |
| [Supplemental Data S3](archives/Supplemental_Data_S3.zip) | Training inputs and context-construction protocols, checkpoint-selection code, historical prediction caches, and analytical figure sources |
| [Supplemental Data S4](archives/Supplemental_Data_S4.zip) | Figure scripts and source values, editable slides, and the recorded HotpotQA dialogue example |

The archives correspond byte-for-byte to Supplemental Data S2–S4. [Archive checksums](SHA256SUMS) identify the exact files. Each archive contains a README and a manifest for its members. See [source and license information](DATA_SOURCES.md) for upstream attribution and reuse conditions.

## Recompute the reported statistics

Use Python 3.10 or later. Run the following from the repository root:

```text
python -m zipfile -e archives/Supplemental_Data_S2.zip .
python -m zipfile -e archives/Supplemental_Data_S3.zip .
python -m zipfile -e archives/Supplemental_Data_S4.zip .
python -m pip install -r Supplemental_Data_S2/requirements.txt
python Supplemental_Data_S2/reproduce_statistics.py
python Supplemental_Data_S3/reproduce_historical_metrics.py
```

The numerical checks run on saved predictions and do not need a GPU or model weights. The S2 entry point checks the main retrieval evaluation and all four external contrasts; the S3 entry point verifies the historical controlled comparisons. See the README files inside S3 and S4 for retraining and regenerating figures. Reconstructing the full model inputs or refitting adapters requires the original upstream benchmark downloads and model revisions identified in those archives.

## Citation

Use [CITATION.cff](CITATION.cff) for repository citation metadata. The benchmark articles and original download locations are listed in [DATA_SOURCES.md](DATA_SOURCES.md).
