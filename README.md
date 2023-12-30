# Awesome-NeurIPS-2023 : Observations and Interesting Papers from the Neural Information Processing Conference
#### _[<img src="images/back_button_2.png" width="25" height="25">Back to TOC](https://github.com/xsankar/Awesome-Awesome-LLM)_
| [About Me](https://www.linkedin.com/in/ksankar) | [Blog](https://ksankar.medium.com) |
| :- | :- |
> |***As of 11.30.23, I am working hard to build the repos - takes time to review and curate. Appreciate your patience ... Thanks ...***|
> | :- |
> 
---
| [Now](#now) | [Interesting](#interesting) | [Towards AGI](#towards-agi) | [Planning](#planning) | [Reasoning](reasoning) | [Alignment](alignment) | [Rl](rl) |
| :- | :- | :- | :- | :- | :- | :- |
|  |  |  |  |  |  |  |
[Prompting](#prompting) | [SLM](#slm) | [Training Efficiency](#training-efficiency) | [Fine Tuning/RAG](#fine-tuning-rag) | [Datasets](#datasets) | [Benchmarks](#benchmarks) | [Attack Mitigation](#attack-mitigation) |
| :-: | :-: | :-: | :-: | :-: | :-: | :-: |
|  |  |  |  |  |  |  |
---
### Metrics & Benchmarks by Topic (See [LLM Evaluation Topics for a quick intro](#llm-evaluation-topics))

| [Dialogue Kinetics](#dialogue-kinetics) | [Bias](#bias) | [Toxicity](#toxicity) | [Robustness](#robustness) | [Factuality](#factuality) | [Hallucination](#hallucination) | [Accuracy](#accuracy) | [Alignment](#alignment) |
| :- | :- | :- | :- |:- |:- |:- | :- |
---
| [World Knowledge](#world-knowledge) | [Commonsense Reasoning](#commonsense-reasoning) | [Language Understanding](#language-understanding) | [Symbolic Problem Solving](#symbolic-problem-solving) | [Reading Comprehension](#reading-comprehension) | [Programming](programming) |
| :- | :- | :- | :- |:- |:- |
***
### LLM Evaluation Concepts
![OpenAI](./images/NPS-v07-p26.png)
***
![OpenAI](./images/LLMSec_P28.jpeg)
***
![OpenAI](./images/NPS-v07-p29.png)
***
![OpenAI](./images/LLMSec_P25.jpeg)
***
![OpenAI](./images/NPS-v07-p31.png)
***
| [Survey & Analytical Paper Collection](#survey--analytical-papers) | [Guardrail Platforms](#guardrail-platforms) | [Multi Benchmark Frameworks](#multi-benchmark-frameworks) | [Metrics & Benchmarks by Topic](#metrics--benchmarks-by-topic) | [Datasets](#datasets) | [Data Leakage](#data-leakage) | [Other Repos](#other-repos) |
| :-: | :-: | :-: | :-: | :-: | :-: | :-: |
***
## Survey & Analytical Papers 
[<img src="images/back_button_2.png" width="25" height="25">Top](#back-to-toc)
| Year | Title | Notes | 
| -: | :- | :- |
| | Survey Papers | |
| 11.2023 | [A Survey on Hallucination in Large Language Models: Principles, Taxonomy, Challenges, and Open Questions](https://github.com/LuckyyySTA/Awesome-LLM-hallucination) | |
| 10.2023 | [Cataloguing LLM Evaluations](https://aiverifyfoundation.sg/downloads/Cataloguing_LLM_Evaluations.pdf) | from [AI verify Foundation SIngapore](https://aiverifyfoundation.sg/) |
| 10.2023 | [Evaluating Large Language Models: A Comprehensive Survey](https://arxiv.org/abs/2310.19736) | |
| 7.2023 | [A Survey on Evaluation of Large Language Models](https://arxiv.org/abs/2307.03109) | |
| | Analytical Papers | |
| 06.2023 | [DecodingTrust: A Comprehensive Assessment of Trustworthiness in GPT Models](https://arxiv.org/abs/2306.11698) | |
| 11.2022 | [Holistic Evaluation of Language Models](https://arxiv.org/abs/2211.09110) |  |
| 11.2021 | [A Systematic Investigation of Commonsense Knowledge in Large Language Models](https://arxiv.org/abs/2111.00607) | EMNLP/Dubai 2022 | 
***
## Guardrail Platforms
[<img src="images/back_button_2.png" width="25" height="25">Top](#back-to-toc)
| Type | Title | Notes | 
| -: | :- | :- |
| Evaluation Guardrail | [Trulens](https://www.trulens.org/) | By TruEra. Truthfulness, Question answering relevance, Harmful or toxic language, User sentiment, Language mismatch, Response verbosity, LLM Augmentation | 
| Prompt Injection | [Rebuff](https://guthub.com/protectai/rebuff) | By Protect AI. Open source – self hardening prompt injection detector | 
| PII Scrubber | [LLM Gateway](https://github.com/wealthsimple/llm-gateway) | Tracks data sent and received from these providers in a postgres database and runs PII scrubbing heuristics prior to sending | 
| PII Scrubber | [Azure Presidio](https://microsoft.github.io/presidio/) | Micro$oft | 
| Guardrails.ai | [Guardrail](https://github.com/guardrails-ai/guardrails)| [Nvidia nemo + Guardrails](https://arize.com/blog-course/guardrails-what-are-they-and-how-can-you-use-nemo-and-guardrails-ai-to-safeguard-llms/) | 
| Guardrail | [Nvidia Nemo Framework](https://developer.nvidia.com/nemo) | Monitoring communication in both directions, Topical guardrails, Safety guardrails (response), Security guardrails (malicious code) |
| Guardrail for aws bedrock | [Bedrock Guardrails](https://aws.amazon.com/bedrock/guardrails/) | |
| Evaluation | Quotient AI | Stealth as of 12.27.23 |
***
## Multi Metric Evaluation Frameworks 
[<img src="images/back_button_2.png" width="25" height="25">Top](#back-to-toc)
>
| Year | Title | Notes | 
| :- | :- | :- |
| 2023 | [MosaicML Eval Gauntlet](https://www.mosaicml.com/llm-evaluation) | Good eval framework. Encompasses 34 different benchmarks, organized into 6 broad categories of competency that we expect good foundation models to have. Their categorization is very useful - I am borrowing some of their ideas ! |
| 2023 | [OpenCompass](https://github.com/open-compass/opencompass) | Extensive dataset support, good dataset list |
| 2023 | [GAIA: A benchmark for General AI Assistants](https://huggingface.co/papers/2311.12983) | Hugginface questions |
| | [Language Model Evaluation Harness - EleutherAI](https://github.com/EleutherAI/lm-evaluation-harnes) | 200+ subtasks / evaluation settings implemented |
| | [Alpaca Eval](https://github.com/tatsu-lab/alpaca_eval) | An Automatic Evaluator for Instruction-following Language Models |
| 11.2023| [IFEval](https://arxiv.org/abs/2311.07911) | 25 types of verifiable instructions and constructed around 500 prompts |
| | [Giskard](https://huggingface.co/blog/JMJM/giskard-llm-testing-and-debugging-hf) | Multiple vulnerabilities |
| | https://github.com/FastEval/FastEval | |
***
