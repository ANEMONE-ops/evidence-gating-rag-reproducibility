# Data sources and reuse

The archives contain study-specific selections, derived input records, prediction outputs, and analysis code. Benchmarks and pretrained models retain their original terms. This repository does not apply one license to the combined archives or relicense third-party content.

| Benchmark | Use in this study | Source and attribution | Upstream terms |
| --- | --- | --- | --- |
| MuSiQue | Training and historical evaluation; selected questions and passages | [Trivedi et al., 2022](https://doi.org/10.1162/tacl_a_00475); [official release](https://github.com/StonyBrookNLP/musique#data) | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) |
| HotpotQA | Principal test, historical evaluation, and Figure 3; selected questions and passages | [Yang et al., 2018](https://doi.org/10.18653/v1/D18-1259); [official release and corpus](https://hotpotqa.github.io/) | [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) for the distributed dataset and corpus; adapted material from HotpotQA retains this license |
| IIRC | Historical evaluation | [Ferguson et al., 2020](https://doi.org/10.18653/v1/2020.emnlp-main.86); [original Allen Institute data release notice](https://github.com/allenai/allennlp-website/blob/master/iirc.html) | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) for the dataset |
| NoMIRACL | External validation; identifiers, published labels, and derived predictions | [Thakur et al., 2024](https://doi.org/10.18653/v1/2024.findings-emnlp.730); [official dataset card](https://huggingface.co/datasets/miracl/nomiracl) | [Apache-2.0](https://www.apache.org/licenses/LICENSE-2.0) per the dataset card; consult original source terms for passage text |
| SQuAD 2.0 | External validation; identifiers, published labels, and derived predictions | [Rajpurkar et al., 2018](https://doi.org/10.18653/v1/P18-2124); [official release](https://rajpurkar.github.io/SQuAD-explorer/) | [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) for original and adapted SQuAD material |

The study selects, reformats, groups, and orders benchmark inputs for retrieval and calibration. Archive READMEs and machine-readable manifests document these changes and preserve the upstream identifiers and hashes. For NoMIRACL and SQuAD 2.0, the external restoration script uses the official downloads rather than a copy of the upstream archives.

Model weights are obtained from the upstream releases at the revisions specified in S3: [Qwen2.5-1.5B-Instruct](https://huggingface.co/Qwen/Qwen2.5-1.5B-Instruct) and [BGE-small-en-v1.5](https://huggingface.co/BAAI/bge-small-en-v1.5). No pretrained weights are included in the repository.
