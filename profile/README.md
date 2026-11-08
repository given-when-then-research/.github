# GivenWhenLab

**GivenWhenThen (GWT)** is a research dataset of **2,289 Behavior-Driven Development (BDD) test scenarios** built from **1,720 selected open-source GitHub projects**. It links each scenario's Gherkin specification to the code implementing its steps and the system code used by those implementations.

[![Dataset DOI](https://zenodo.org/badge/DOI/10.5282/zenodo.17517697.svg)](https://doi.org/10.5282/zenodo.17517697)
[![Paper at MSR 2026](https://img.shields.io/badge/Paper-MSR%202026-316A9A)](https://doi.org/10.1145/3793302.3793308)



[Dataset and replication package on Zenodo](https://zenodo.org/records/17573782) · [MSR 2026 paper](https://doi.org/10.1145/3793302.3793308)

## What's in the dataset?

Each record in `GivenWhenThen.json` links three artifacts:

| Artifact | What it contains |
| --- | --- |
| Feature file | The BDD scenario as written in Gherkin |
| Step definition file | The code that implements the scenario's steps |
| System code files | The application source files used by the step definitions |

These links support empirical studies of BDD, research on test automation, and the training and evaluation of AI models for software testing.

## How we built GWT

<img width="2280" height="482" alt="Image" src="https://github.com/user-attachments/assets/378c4ae1-21a0-4099-98c3-0daa0c1bae11" />


1. **[Projects Discovery](https://github.com/given-when-then-research/projects-discovery)**  
   Mine GitHub for projects using Cucumber and BDD, identifying **4,327 candidate repositories**.

2. **[Projects Selection](https://github.com/given-when-then-research/projects-selection)**  
   Clone and filter candidate repositories, retaining projects with valid English-language `.feature` files and an official Cucumber dependency. This stage selected **1,720 projects**.

3. **[Step Definitions Extraction Heuristic](https://github.com/given-when-then-research/step-definitions-extraction-heuristic)**  
   Apply **Exploration** and **Exploitation** heuristics to link Gherkin steps to their corresponding step definitions (glue code).

4. **[Integration and Refinement](https://github.com/given-when-then-research/integration-and-refinement)**  
   Compare, validate, clean, and consolidate heuristic outputs into a unified set of scenario-to-step-definition mappings.

5. **[System Code Detection](https://github.com/given-when-then-research/system-code-detection)**  
   Identify relevant application source files used by the step definitions and assemble the final dataset of **2,289 BDD scenarios**.

The [Zenodo replication package](https://zenodo.org/records/17573782) provides the final dataset, intermediate outputs, heuristic validation samples, and source code archives for the pipeline stages.

## Citation

If you use GWT in your research, please cite the paper.

```bibtex
@inproceedings{givenwhenthendatasetmsr,
  author    = {J{\'u}nior, Luciano Belo de Alc{\^a}ntara and Montandon, Jo{\~a}o Eduardo},
  title     = {{GivenWhenThen}: A Dataset of {BDD} Test Scenarios Mined from Open Source Projects},
  booktitle = {Proceedings of the 23rd International Conference on Mining Software Repositories},
  series    = {MSR '26},
  year      = {2026},
  pages     = {595--599},
  numpages  = {5},
  publisher = {Association for Computing Machinery},
  address   = {New York, NY, USA},
  location  = {Rio de Janeiro, Brazil},
  isbn      = {9798400724749},
  doi       = {10.1145/3793302.3793308},
  url       = {https://doi.org/10.1145/3793302.3793308}
}
```

**Dataset DOI** · [`10.5282/zenodo.17517697`](https://zenodo.org/records/17573782)
