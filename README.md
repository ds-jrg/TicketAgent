## Introduction

High-quality tickets are essential for software development, serving as a means of knowledge transfer between product owners and developers. Poorly written tickets create additional work and increase development costs. Creating tickets is time-consuming, and product owners often lack insight into the codebase, resulting in descriptions that may not reflect existing implementations. Large language models (LLMs) excel at processing natural language and possess strong programming knowledge, making them promising tools for automating ticket generation. However, research on LLM-based ticket generation remains limited. Recent work has shown that combining LLMs with code graphs improves querying of large codebases, which may benefit ticket generation. We propose TicketAgent, a repository-aware workflow for automated software ticket generation that combines LLM-based ticket writing with code-graph-based code localization and project-specific domain knowledge. We evaluate TicketAgent alongside two baselines: an LLM-only workflow and a retrieval-augmented generation (RAG) workflow. Across automated and human evaluations, providing LLMs with additional information sources consistently improves ticket quality. In particular, structured access to the source code via code-based querying yields the largest improvements, outperforming both the LLM-only and RAG baselines.

This repository contains the following files:

- summarize_prompt.txt -> This prompt was used to generate inputs notes for ticket generation out of the existing corpus of tickets
- system_prompt_base_llm.txt -> This prompt was used for the ticket generation with the base-llm.
- system_prompt_rag.txt -> This prompt was used for the ticket generation with the llm+rag.
- prompts_agent.txt -> These prompts were used for the two agents and for interaction with the LocAgent tool by TicketAgent.
- system_prompt_llm_judge.txt -> The system prompt given to both llm judges for pair-wise evaluation.

## Citing This Work

Note: Our paper is accepted for publication at the 35th ACM International Conference on Information and Knowledge Management (CIKM 2026), and will appear in the conference proceedings. You can cite the work using the following BibTeX entry:

```bibtex
@inproceedings{ticketagent2026,
  title={Automated Software Ticket Generation Using Large Language Models and Code Graphs},
  author={Timo Maximilian Sieger and Stefan Heindorf},
  year={2026},
  booktitle={Proceedings of the 35th ACM International Conference on Information and Knowledge Management (CIKM '26)},
  pages={1--5},
  publisher={ACM},
  address={New York, NY, USA},
  doi={10.1145/3799682.3839849}
}
```
