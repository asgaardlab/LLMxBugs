# Large Language Models are Pretty Good Zero-Shot Video Game Bug Detectors

<div>

[![Website](http://img.shields.io/badge/Website-4b44ce.svg)](https://asgaardlab.github.io/LLMxBugs/)
[![arXiv](https://img.shields.io/badge/arXiv-TBA-b31b1b.svg)](https://arxiv.org/abs/)

</div>



## Abstract

Video game testing requires game-specific knowledge as well as common sense reasoning about the events in the game. While AI-driven agents can satisfy the first requirement, it is not yet possible to meet the second requirement automatically.
Therefore, video game testing often still relies on manual testing, and human testers are  required to play the game thoroughly to detect bugs. As a result, it is challenging to fully automate game testing.
In this study, we explore the possibility of leveraging the zero-shot capabilities of large language models for video game bug detection.
By formulating the bug detection problem as a question-answering task, we show that large language models can identify which event is buggy in a sequence of textual descriptions of events from a game. To this end, we introduce the `GameBugDescriptions` benchmark dataset, which consists of 167 buggy gameplay videos and a total of 334 question-answer pairs across 8 games.
We extensively evaluate the performance of six models across the OPT and InstructGPT large language model families on our benchmark dataset.
Our results show promising results for employing language models to detect video game bugs. With the proper prompting technique, we could achieve an accuracy of 70.66%, and on some video games, up to 78.94%.


## Results Summary

Summary of the results for the bug detection task [[Code](https://github.com/asgaardlab/LLMxBugs/blob/main/Overview.ipynb)].

|   | OPT-66B  | OPT-66B  | OPT-175B  | OPT-175B  | text-ada-001  | text-ada-001  | text-babbage-001  | text-babbage-001  | text-curie-001  | text-curie-001  | text-davinci-002  | text-davinci-002  |
|:---: |:---: |:---: |:---: |:---: |:---: |:---: |:---: |:---: |:---: |:---: |:---: |:---: |
| Trigger  | Descr1  | Descr2  | Descr1  | Descr2  | Descr1  | Descr2  | Descr1  | Descr2  | Descr1  | Descr2  | Descr1  | Descr2  |
| 1  | 15.57  | 23.35  | 14.97  | 32.93  | 31.14  | 22.16  | 49.1  | 29.94  | 43.11  | 27.54  | **70.66**  | **59.88**  |
| 2  | 15.57  | 31.14  | 15.57  | 32.93  | 34.13  | 19.16  | 49.1  | 31.14  | 41.32  | 29.94  | 62.87  | 58.08  |
| 3  | 48.50  | 31.74  | 13.77  | 31.14  | 16.17  | 6.59  | 49.7  | 31.74  | 41.32  | 31.14  | 52.10  | 58.68  |
| 4  | 44.31  | 31.14  | 16.17  | 31.74  | 7.78  | 2.99  | 47.9  | 30.54  | 44.91  | 32.34  | 52.69  | 55.69  |
| 5  | 26.95  | 37.13  | 13.17  | 31.14  | 27.54  | 19.16  | 47.9  | 32.93  | 36.53  | 31.74  | 50.90  | 50.90  |
| 6  | 28.14  | 29.94  | 19.16  | 31.74  | 20.96  | 8.98  | 49.1  | 31.14  | 43.11  | 29.34  | 45.51  | 50.30  |
| 7  | 22.16  | 36.53  | 13.17  | 31.14  | 23.35  | 17.96  | 49.1  | 31.74  | 39.52  | 32.93  | 43.11  | 50.30  |
