# Candidate Datasets for AQA and SQA

Last checked: 2026-08-26

Do not download a dataset until its license, access conditions, storage size,
and fit to the final research question have been checked. “Real” is decomposed
into audio provenance and annotation provenance below.

| Dataset/benchmark | Primary task | Audio provenance | QA provenance | Languages | Official source | Initial caution |
|---|---|---|---|---|---|---|
| Spoken-SQuAD | Spoken-document extractive QA | TTS from SQuAD passages | Inherited text QA | English | [Official repository](https://github.com/Chia-Hsuan-Lee/Spoken-SQuAD) | Synthetic speech; text questions; large audio download |
| Clotho-AQA | Environmental AQA | Real-world Freesound/Clotho clips | Crowdsourced questions and answers | Primarily English text QA | [Zenodo record](https://zenodo.org/records/6473207) | Check Clotho/Freesound licensing per clip; restricted answer forms |
| SD-QA | Spoken dialectal QA | Human-recorded spoken prompts | Adapted QA benchmark prompts | Arabic, Bengali, English, Kiswahili, Korean | [Paper](https://aclanthology.org/2021.findings-emnlp.281/) | Verify repository access, consent, speaker metadata, and inherited labels |
| Spoken-CoQA | Spoken conversational QA | Read the paper/repository to classify precisely | Adapted from conversational QA with spoken modality | English | [Paper](https://aclanthology.org/2022.findings-naacl.91/) | Confirm current data/code availability and exact speech generation procedure |
| TurQuAse | Low-resource spoken QA | TTS plus ASR pipeline | Automatically generated QA with limited manual seed data | Turkish | [Paper](https://aclanthology.org/2022.findings-emnlp.342/) | Useful for synthetic-data research, not a natural-speech-only corpus |
| AudioBench | Broad audio-language benchmark | Mixed by component | Mixed; includes generated and human-verified material | Multiple task-dependent languages | [Paper](https://aclanthology.org/2025.naacl-long.218/) | Audit each subset separately; it is a benchmark collection, not one homogeneous dataset |
| VoxEval | End-to-end spoken knowledge QA | Speech conditions defined by benchmark | Converted/constructed knowledge QA; inspect paper | Primarily English in initial release | [Official repository](https://github.com/dreamtheater123/VoxEval) | Check synthesis and voice-condition details before calling it natural speech |
| SpokenNativQA | Everyday spoken QA | Naturally spoken | Culturally aligned QA; inspect release documentation | Multilingual | [ISCA paper](https://www.isca-archive.org/interspeech_2025/alam25_interspeech.html) | Verify license, language distribution, collection protocol, and downloadable release |

## Selection checklist

Before choosing a dataset, answer:

1. Which exact task formulation does it support?
2. Are the train/dev/test splits speaker-independent?
3. Were questions written while annotators listened to audio, or inherited from
   text?
4. Are answers acoustic facts, linguistic content, external knowledge, or a
   mixture?
5. Does the license permit the planned research and redistribution?
6. Are audio files stable, or dependent on links that may disappear?
7. What demographic, language, accent, and recording-condition coverage exists?
8. Could a text-only model exploit question/answer priors without listening?
9. Is there contamination from common pretraining corpora?
10. Can the experiment be reproduced with available compute and storage?

