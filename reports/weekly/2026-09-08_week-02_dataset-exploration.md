# Meeting 2 Report — Dataset Exploration for Audio Question Answering

**Date:** 2026-09-08  
**Meeting:** 2  
**Main Goal:** Find and compare datasets that may be useful for the Audio Question Answering research project.

## 1. Meeting Objective

The main goal of Meeting 2 is to explore and identify datasets that could be used for the Audio Question Answering project.

At this stage, the objective is **not to select a final dataset**. The focus is to:

- Find available Audio Question Answering datasets.
- Compare their size, language, and structure.
- Check whether audio, questions, and answers are available.
- Identify datasets that are directly usable for Audio QA.
- Identify supporting datasets that could potentially be adapted or combined, especially for Arabic Audio QA.

## 2. Dataset Categories

The collected datasets fall into three main categories:

1. **Direct Audio Question Answering datasets** — contain audio together with questions and answers.
2. **Speech / ASR datasets** — contain audio and speech samples or transcripts, but no QA pairs.
3. **Text Question Answering datasets** — contain questions and answers but no audio; these could potentially be converted into Audio QA datasets using recordings or text-to-speech.

## 3. Dataset Comparison Table

| Name | Type | Language | Size | Audio Available? | Questions Available? | Answers Available? | Link |
|---|---|---|---|---|---|---|---|
| dcase2025-audio-qa | Audio Question Answering | English | 15,571 samples | Yes | Yes | Yes (multiple choice) | [Click](https://huggingface.co/datasets/gijs/dcase2025-audio-qa) |
| trivia_qa_audio_score | Audio Question Answering | English | 1,000 samples | Yes | Yes | Yes | [Click](https://huggingface.co/datasets/chiyuanhsiao/trivia_qa-audio-score) |
| Merged Arabic Corpus of Isolated Words | Arabic Speech Recognition | Arabic | 1,000 files | Yes | No | No | [Click](https://www.kaggle.com/datasets/mohamedanwarvic/merged-arabic-corpus-of-isolated-words) |
| Quran Ayat Speech to Text | Arabic Speech-to-Text | Arabic | ~232K files | Yes | No | No | [Click](https://www.kaggle.com/datasets/bigguyubuntu/quran-ayat-speech-to-text/data) |
| Arabic Language Comprehension | Text QA / Reading Comprehension | Arabic | 702 samples | No | Yes | Yes | [Click](https://www.kaggle.com/datasets/thedevastator/unlocking-arabic-language-comprehension-with-the?select=validation.csv) |
| Shifaa Arabic Mental Health Consultations | Text QA / Dialogue | Arabic | 2,256 samples | No | Yes | Yes | [Click](https://www.kaggle.com/datasets/ahmedseleem/shifaa-arabic-mental-health-consultations) |
| Spoken-SQuAD | Spoken Question Answering | English | ~37K train + ~5.3K test QA pairs | Yes | Yes | Yes | [Click](https://github.com/Chia-Hsuan-Lee/Spoken-SQuAD) |
| NMSQA | Textless / Fully Spoken Question Answering | English | Large-scale SQuAD-derived dataset | Yes | Yes — spoken questions | Yes | [Click](https://huggingface.co/datasets/voidful/NMSQA) |
| SLUE-SQA-5 | Spoken Question Answering | English | Questions from 5 major QA datasets | Yes | Yes — spoken questions | Yes | [Click](https://huggingface.co/datasets/asapp/slue-phase-2) |
| HeySQuAD Human | Spoken Question Answering | English | 76,148 samples | Yes — human speech | Yes | Yes | [Click](https://huggingface.co/datasets/yijingwu/HeySQuAD_human) |
| HeySQuAD Machine | Spoken Question Answering | English | 98,163 samples | Yes — synthetic speech | Yes | Yes | [Click](https://huggingface.co/datasets/yijingwu/HeySQuAD_machine) |
| LibriSQA | Open-ended Spoken Question Answering | English | ~107K SQA pairs | Yes — LibriSpeech audio | Yes | Yes | [Click](https://huggingface.co/datasets/ZihanZhao/LibriSQA) |
| WebQuestions | Open-domain Question Answering | English | ~5.8K questions | No | Yes | Yes | [Click](https://github.com/brmson/dataset-factoid-webquestions) |
| CuratedTREC | Factoid Question Answering | English | ~2K questions | No | Yes | Yes | [Click](https://github.com/brmson/dataset-factoid-curated) |

## 4. Most Relevant Audio QA Datasets

The datasets currently most relevant to the project are:

| Dataset | Why It Is Relevant |
|---|---|
| **dcase2025-audio-qa** | Direct Audio QA dataset with audio, questions, and multiple-choice answers. |
| **trivia_qa_audio_score** | Small direct Audio QA dataset that can be useful for initial experimentation. |
| **Spoken-SQuAD** | Foundational Spoken QA dataset and useful as a baseline. |
| **NMSQA** | Particularly relevant because it supports fully spoken / textless QA settings. |
| **SLUE-SQA-5** | Broader spoken QA benchmark using questions from several major QA datasets. |
| **HeySQuAD** | Provides human-spoken and machine-generated spoken questions, enabling comparison between real and synthetic speech. |
| **LibriSQA** | Large-scale spoken QA dataset suitable for modern Audio QA experiments. |

## 5. Arabic Dataset Observation

An important observation from the initial search is that many Arabic speech datasets and several Arabic text QA datasets are available, but there are far fewer datasets that directly combine:

**Arabic audio + questions + answers**

The Arabic datasets found so far mainly provide either:

- **Audio without QA pairs**, such as Quran Ayat Speech to Text and the Merged Arabic Corpus of Isolated Words; or
- **QA pairs without audio**, such as Arabic Language Comprehension and Shifaa.

This may become an important research direction later because an Arabic Audio QA dataset could potentially be created by combining an Arabic QA dataset with recorded or synthesized speech.

## 6. Current Conclusion

The dataset search shows that there are several English Audio Question Answering datasets available for experimentation.

The strongest candidates currently include:

**NMSQA, LibriSQA, SLUE-SQA-5, HeySQuAD, Spoken-SQuAD, dcase2025-audio-qa, and trivia_qa_audio_score.**

For Arabic, direct Audio QA datasets appear much more limited. Therefore, two possible directions should be investigated next:

1. **Use an existing English Audio QA benchmark** to develop and evaluate the system.
2. **Investigate creating or adapting an Arabic Audio QA dataset** by combining existing Arabic speech and QA resources.

No final dataset is selected during Meeting 2. The purpose of this meeting is to establish the available dataset landscape before deciding on the research methodology and implementation direction.
