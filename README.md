# A Pedagogical Introduction to the Architecture of Claude for Research Administrators

This repository contains the source and compiled PDF for the paper *A Pedagogical Introduction to the Architecture of Claude for Research Administrators* by Duncan A. Brown (Office of Research, Syracuse University).

## Read the paper

**[Read the paper (PDF)](https://github.com/duncan-brown/claude-architecture-paper/blob/main/A_Pedagogical_Introduction_to_the_Architecture_of_Claude.pdf)**

## What this is

Large language models such as Claude are increasingly used in research administration for data analysis, document generation, and institutional research, yet their internal architecture is poorly understood by most of the professionals who rely on them. That gap leads to misplaced trust in some outputs and unnecessary skepticism toward others.

This paper is a scaffolded, non-technical introduction to how Claude actually works, aimed at research administrators and other professionals who use these tools but do not have a machine learning background. It builds up from a concrete analogy between Claude's runtime and a traditional Python program, then progressively introduces the context window, chat persistence, projects, skills, connectors and the Model Context Protocol, the sandboxed execution environment, the orchestration harness, the research tool, and finally the tokenizer and transformer architecture. Each section builds on the vocabulary of the one before it, and the paper is designed so that a reader can stop at whatever level of detail serves their needs.

The central practical argument concerns the trustworthiness of different kinds of output: the distinction between statistical text generation and deterministic code execution. The headline principle for practitioners is straightforward: **do not trust a number that the model produced in prose.** An appendix provides a case study of a production skill used for sponsored research budget development at Syracuse University.

## Origin

The paper began as an answer to a question from Brett Padgett, Senior Vice President and Chief Financial Officer at Syracuse University, about how Claude skills work. What started as an explanatory diagram grew into a full architectural treatment.

## Repository contents

| File | Description |
|------|-------------|
| `A_Pedagogical_Introduction_to_the_Architecture_of_Claude.pdf` | Compiled PDF build of the paper |
| `main.tex` | LaTeX source |
| `references.bib` | Bibliography (BibTeX) |
| `fig_stack.pdf` | Figure: traditional software stack analogy |
| `fig_architecture.pdf` | Figure: execution environment and connectors |
| `fig_context_growth.pdf` | Figure: context window growth |
| `fig_skill.pdf` | Figure: anatomy of a skill |
| `fig_skill_lifecycle.pdf` | Figure: skill lifecycle |
| `fig_agent_loop.pdf` | Figure: the agent loop |
| `fig_transformer.pdf` | Figure: transformer architecture |
| `fig_research.pdf` | Figure: multi-agent research tool architecture |

## Building from source

The paper is written in LaTeX and uses a separate BibTeX bibliography. To compile locally:

```bash
pdflatex main.tex
bibtex main
pdflatex main.tex
pdflatex main.tex
```

All figure PDFs referenced by `main.tex` are included in the repository, so no figure regeneration step is required to build the document.

## Citation

If you reference this work, please cite:

> D. A. Brown, *A Pedagogical Introduction to the Architecture of Claude for Research Administrators* (2026).

## Author

Duncan A. Brown
Office of Research, Syracuse University
Syracuse, NY 13244

## License

This work is licensed under a [Creative Commons Attribution 4.0 International License (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/). You are free to share and adapt the material for any purpose, including commercially, provided you give appropriate credit.
