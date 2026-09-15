# Meeting 3 Report — Dataset Tasks and Further Dataset Exploration

**Date:** 2026-09-16  
**Meeting:** 3  
**Main Goal:** Identify the tasks supported by the datasets collected in Meeting 2 and continue collecting new datasets covering Audio Question Answering and other audio-related tasks.

## 1. Meeting Objective

This week's work has two parts:

1. Revisit the datasets collected during Meeting 2 and identify the machine learning or research task associated with each dataset.
2. Search for additional datasets covering Audio Question Answering and other audio-related tasks, such as temporal reasoning and speech emotion recognition.

Dataset collection is still ongoing, so this is a working report.

## 2. Previous Datasets — Updated With Tasks

The following table preserves the datasets collected during Meeting 2 and adds the task or tasks supported by each dataset.

| Name | Type | Task(s) | Language | Size | Audio Available? | Questions Available? | Answers Available? | Link |
|---|---|---|---|---|---|---|---|---|
| dcase2025-audio-qa | Audio Question Answering | Audio Question Answering (AQA) / Audio Reasoning | English | 15,571 samples | Yes | Yes | Yes (multiple choice) | [Click](https://huggingface.co/datasets/gijs/dcase2025-audio-qa) |
| trivia_qa_audio_score | Audio Question Answering | Spoken / Audio Question Answering | English | 1,000 samples | Yes | Yes | Yes | [Click](https://huggingface.co/datasets/chiyuanhsiao/trivia_qa-audio-score) |
| Merged Arabic Corpus of Isolated Words | Arabic Speech Recognition | Isolated-Word Speech Recognition / Speech Classification | Arabic | 1,000 files | Yes | No | No | [Click](https://www.kaggle.com/datasets/mohamedanwarvic/merged-arabic-corpus-of-isolated-words) |
| Quran Ayat Speech to Text | Arabic Speech-to-Text | Automatic Speech Recognition (ASR) / Speech-to-Text | Arabic | ~232K files | Yes | No | No | [Click](https://www.kaggle.com/datasets/bigguyubuntu/quran-ayat-speech-to-text/data) |
| Arabic Language Comprehension | Text QA / Reading Comprehension | Reading Comprehension / Text Question Answering | Arabic | 702 samples | No | Yes | Yes | [Click](https://www.kaggle.com/datasets/thedevastator/unlocking-arabic-language-comprehension-with-the?select=validation.csv) |
| Shifaa Arabic Mental Health Consultations | Text QA / Dialogue | Question Answering / Text Classification | Arabic | 2,256 samples | No | Yes | Yes | [Click](https://www.kaggle.com/datasets/ahmedseleem/shifaa-arabic-mental-health-consultations) |
| Spoken-SQuAD | Spoken Question Answering | Spoken Question Answering (SQA) / Spoken Reading Comprehension | English | ~37K train + ~5.3K test QA pairs | Yes | Yes | Yes | [Click](https://github.com/Chia-Hsuan-Lee/Spoken-SQuAD) |
| NMSQA | Textless / Fully Spoken Question Answering | Textless Spoken Question Answering / ASR | English | Large-scale SQuAD-derived dataset | Yes | Yes — spoken questions | Yes | [Click](https://huggingface.co/datasets/voidful/NMSQA) |
| SLUE-SQA-5 | Spoken Question Answering | Spoken Question Answering (SQA) | English | Questions from 5 major QA datasets | Yes | Yes — spoken questions | Yes | [Click](https://huggingface.co/datasets/asapp/slue-phase-2) |
| HeySQuAD Human | Spoken Question Answering | Spoken Question Answering / ASR-Robust QA | English | 76,148 samples | Yes — human speech | Yes | Yes | [Click](https://huggingface.co/datasets/yijingwu/HeySQuAD_human) |
| HeySQuAD Machine | Spoken Question Answering | Spoken Question Answering / ASR-Robust QA | English | 98,163 samples | Yes — synthetic speech | Yes | Yes | [Click](https://huggingface.co/datasets/yijingwu/HeySQuAD_machine) |
| LibriSQA | Open-ended Spoken Question Answering | Spoken Question Answering / ASR / Multiple-Choice QA | English | ~107K SQA pairs | Yes — LibriSpeech audio | Yes | Yes | [Click](https://huggingface.co/datasets/ZihanZhao/LibriSQA) |
| WebQuestions | Open-domain Question Answering | Open-Domain / Factoid Question Answering | English | ~5.8K questions | No | Yes | Yes | [Click](https://github.com/brmson/dataset-factoid-webquestions) |
| CuratedTREC | Factoid Question Answering | Factoid Question Answering | English | ~2K questions | No | Yes | Yes | [Click](https://github.com/brmson/dataset-factoid-curated) |

## 3. Newly Discovered Datasets

The following datasets were discovered after Meeting 2 and are intentionally kept separate from the previous datasets.

| # | Dataset | Type | Task(s) | Language | Size | Audio? | Questions? | Answers? | Notes | Download |
|---|---|---|---|---|---|---|---|---|---|---|
| 1 | Clotho-AQA | Audio Question Answering | Audio Question Answering (AQA) | English | 1,991 audio files; 35,838 QA pairs | Yes | Yes | Yes | Questions are about the content/events occurring in general audio recordings. | [Download](https://zenodo.org/records/6473207) |
| 2 | AQUA-Bench | Audio QA Benchmark | Audio Question Unanswerability Assessment (AAD / IASD / IAQD) | English | — | Yes | Yes | Yes | It tests whether the model realizes when a question cannot be answered from the audio. | [Link](https://kuan2jiu99.github.io/AQUA-Bench-demo/) |
| 3 | Diagnostic Audio Question Answering (DAQA) | Diagnostic Audio Question Answering | Audio Question Answering (AQA) / Temporal Reasoning | English | 100,000 audio sequences; approximately 599K questions | Yes | Yes | Yes | Designed to test temporal reasoning about sequences of natural sound events. Questions and answers are programmatically generated. | [Download/code](https://github.com/facebookresearch/daqa) |
| 4 | Ryerson Audio-Visual Database of Emotional Speech and Song (RAVDESS) | Emotional Speech & Song | Speech Emotion Recognition (SER) | English | 7,356 files | Yes | No | No | Speech recordings are labeled with emotions such as happy, sad, angry, fearful, disgust, surprised, calm, and neutral. | [Download](https://zenodo.org/records/1188976) |
| 5 | Berlin Database of Emotional Speech (Emo-DB) | Emotional Speech | Speech Emotion Recognition (SER) | German | approximately 500 recordings | Yes | No | No | Emotional speech labeled with anger, boredom, disgust, fear/anxiety, happiness, sadness, and neutral. | [Official dataset](http://emodb.bilderbar.info/) |

## 4. Task Categories Identified So Far

| Task | Simple Description |
|---|---|
| Automatic Speech Recognition (ASR) | Speech audio → text |
| Speech / Isolated-Word Classification | Speech audio → word/class |
| Audio Question Answering (AQA) | Audio + question → answer |
| Spoken Question Answering (SQA) | Spoken question/context → answer |
| Spoken Reading Comprehension | Spoken passage → answer to a question |
| Audio Temporal Reasoning | Reason about the order/timing of sound events |
| Audio Question Unanswerability Assessment | Determine whether a question can actually be answered from the provided audio |
| Speech Emotion Recognition (SER) | Speech audio → emotion label |
| Text QA / Reading Comprehension | Text/context + question → answer |
| Open-Domain / Factoid QA | Question → factual answer |

## 5. Current Progress

- **Previous datasets:** 14
- **New datasets collected this week so far:** 5
- **Total datasets reviewed:** 19

The new datasets are intentionally kept separate from the previous datasets. Dataset collection for Meeting 3 is still ongoing, and we are exploring multiple audio-related tasks instead of limiting the search to Audio Question Answering. No final dataset has been selected yet.
