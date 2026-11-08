# GivenWhenLab

**GivenWhenThen (GWT)** is a dataset of **2,289 Behavior-Driven Development (BDD) test scenarios** mined from **1,720 open-source GitHub projects**. It connects each scenario's Gherkin specification to the code that implements its steps and the system code those steps use.

<img width="2280" height="482" alt="Image" src="https://github.com/user-attachments/assets/378c4ae1-21a0-4099-98c3-0daa0c1bae11" />

[![Dataset DOI](https://zenodo.org/badge/DOI/10.5282/zenodo.17517697.svg)](https://zenodo.org/records/17573782)
[![Paper at MSR 2026](https://img.shields.io/badge/Paper-MSR%202026-316A9A)](https://doi.org/10.1145/3793302.3793308)

[Dataset and replication package on Zenodo](https://zenodo.org/records/17573782) · [MSR 2026 paper](https://doi.org/10.1145/3793302.3793308) · [Project website](https://givenwhenlab.github.io/)

## What's in the dataset?

Each record in `GivenWhenThen.json` links three artifacts:

| Artifact | What it contains |
| --- | --- |
| Feature file | The BDD scenario as written in Gherkin |
| Step definition file | The code that implements the scenario's steps |
| System code files | The application source files used by the step definitions |

These links support empirical studies of BDD, research on test automation, and the training and evaluation of AI models for software testing.

## How we built GWT

<!-- Save your diagram as profile/assets/gwt-pipeline.svg, then uncomment the line below. -->
<!-- ![Five stages of the GivenWhenThen data collection pipeline](assets/gwt-pipeline.svg) -->

1. **Discover projects.** Search GitHub for repositories that declare Cucumber as a dependency and contain Gherkin feature files.
2. **Select projects.** Validate feature files, identify English-language scenarios, and confirm use of an official Cucumber library.
3. **Extract step definitions.** Use two heuristics, *Exploitation* and *Exploration*, to link feature steps to their implementations.
4. **Integrate and refine.** Combine the results into a consolidated set of feature and step definition pairs.
5. **Detect system code.** Identify the application source files used by the step definitions to complete the dataset records.

The [Zenodo package](https://zenodo.org/records/17573782) includes the final dataset, intermediate outputs, heuristic evaluation samples, and source code archives for each stage.

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
