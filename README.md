<div align="center">
  <h2>
    <a href="https://github.com/Zhixin-L/PrefDiag-Bench">
      PrefDiag-Bench: Diagnosing Personalization Failures in Mobile GUI Agents
    </a>
  </h2>
</div>

<p align="center">
  <a href="https://scholar.google.com/citations?user=dSQdVooAAAAJ">Zhixin Lin</a><sup>1,2</sup>,
  <a href="https://faculty.sdu.edu.cn/xudongliang/zh_CN/index.htm">Dongliang Xu</a><sup>1,*</sup>,
  <a href="https://github.com/LJungang">Jungang Li</a><sup>3,4</sup>,
  <a href="https://shidongpan.github.io/">Shidong Pan</a><sup>5</sup>,<br>
  <a href="https://yorkeyao.cc/">Liang Liu</a><sup>2,&dagger;</sup>,
  <a href="https://yorkeyao.cc/">Jun Feng</a><sup>6</sup>,
  <a href="https://yorkeyao.cc/">Jing Li</a><sup>7</sup>,
  <a href="https://yorkeyao.cc/">Yanbin Sun</a><sup>8</sup>,
  <a href="https://yorkeyao.cc/">Yue Yao</a><sup>1,*</sup>
</p>

<p align="center">
  <sup>1</sup> Shandong University &nbsp; <sup>2</sup> VIVO AI Lab &nbsp;
  <sup>3</sup> HKUST (GZ) &nbsp; <sup>4</sup> HKUST<br>
  <sup>5</sup> Independent Research &nbsp;
  <sup>6</sup> Institute of Automation, Chinese Academy of Sciences<br>
  <sup>7</sup> University of Technology Sydney &nbsp; <sup>8</sup> Guangzhou University
</p>

<p align="center">
  <em><sup>&dagger;</sup> Project lead &nbsp; <sup>*</sup> Corresponding authors</em>
</p>

<p align="center">
  <b>Paper:</b> arXiv link forthcoming &nbsp; | &nbsp;
  <b>Code &amp; Data:</b> will be released &nbsp; | &nbsp;
  <b>Project Page:</b> planned
</p>

## TODO

- [ ] Add the arXiv paper link.
- [ ] Release end-to-end tasks, user profiles, and behavioral memory logs.
- [ ] Release diagnostic probes and reference annotations.
- [ ] Release evaluation code and reproduction instructions.
- [ ] Launch the project page.

The code and dataset will be released in this repository. The overview and paper figures are available below.

## Overview

A personalized GUI agent needs to complete a task while respecting the user's preferences throughout execution. For the same request, a preference may change the desired item, impose a budget, prioritize one candidate, require a comparison, or call for confirmation before acting.

**PrefDiag-Bench** evaluates two complementary questions:

1. **How** does a preference change the agent's execution requirements?
2. **When** should that preference become active in the current task and GUI state?

The benchmark pairs **end-to-end mobile GUI tasks** with **stage-wise diagnostic probes**. This pairing connects task outcomes with the capabilities needed to apply preferences, from interpreting user history to choosing an operation.

<p align="center">
  <img src="assets/overview.png" width="960" alt="PrefDiag-Bench: five ways preferences change GUI execution and the state-dependent timing of confirmation">
</p>

## Benchmark

![E2E Tasks](https://img.shields.io/badge/E2E_tasks-318-7952B3?style=flat-square)
![Diagnostic Probes](https://img.shields.io/badge/Diagnostic_probes-1%2C664-367C8D?style=flat-square)
![Preference Types](https://img.shields.io/badge/Preference_types-5-52667A?style=flat-square)

| Task Families | End-to-End Tasks | Diagnostic Probes | Preference Atoms | Evaluated Systems |
|:---:|:---:|:---:|:---:|:---:|
| **53** | **318** | **1,664** | **260** | **11** |

Each task family contains **one Basic task and five personalized variants**, giving 53 Basic and 265 personalized tasks. Tasks span seven application domains: communication, office, commerce, navigation, system settings, information retrieval, and social media.

### Five Preference Types

| Type | What Changes | Example Requirement |
|:---|:---|:---|
| **Outcome** | The desired result or final choice | Choose the user's usual sugar and ice options. |
| **Constraint** | Conditions that a valid choice or action must satisfy | Keep a purchase within the user's budget. |
| **Ranking** | Priorities among valid candidates | Prefer an official store when suitable options are available. |
| **Process** | The procedure used to complete the task | Compare prices across apps before purchasing. |
| **Interaction** | Whether, when, and how to communicate with the user | Request confirmation before adding an item to the cart. |

### Two Forms of User Context

- **Explicit User Profiles** state the user's preferences directly.
- **Behavioral Memory Logs** convey preferences through synthetic historical records, including supporting evidence and distracting context.

The two context forms are evaluated with the same task requirements, initialization, and success checker. End-to-end success requires satisfying the task goal and all applicable preference requirements.

<p align="center">
  <img src="assets/construction.png" width="960" alt="Construction of paired user contexts and task-linked diagnostic probes">
</p>

## Diagnostic Probes

P1-P5 examine five capabilities across information processing, contextual reasoning, and action formulation. Probe questions are evaluated independently, with reference prerequisites supplied where needed.

| Probe | Stage | Diagnostic Question |
|:---:|:---|:---|
| **P1** | Memory Induction | Can the agent recover a user preference from behavioral logs? |
| **P2** | Evidence Selection | Can it identify the historical records supporting a given preference? |
| **P3** | Relevance Selection | Can it identify which preference applies to the current task? |
| **P4** | Trigger Recognition | Can it recognize whether the current state triggers the preference? |
| **P5** | Operation Mapping | Can it select an appropriate operation once the preference is active? |

For task-level diagnostic scoring, all associated questions at a probe stage must be answered correctly. The task and diagnostic results can then be compared for the same task-preference pair.

## Citation

```bibtex
@misc{lin2026prefdiagbench,
  title  = {Diagnosing Personalization Failures in Mobile GUI Agents},
  author = {Lin, Zhixin and Xu, Dongliang and Li, Jungang and
            Pan, Shidong and Liu, Liang and Feng, Jun and
            Li, Jing and Sun, Yanbin and Yao, Yue},
  year   = {2026},
  note   = {Preprint}
}
```

The citation will be updated with the arXiv identifier after publication.

## Contact

For questions about the benchmark or its release, please open a [GitHub issue](https://github.com/Zhixin-L/PrefDiag-Bench/issues).
