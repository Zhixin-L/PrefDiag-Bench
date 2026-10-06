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
  📑 <a href="https://arxiv.org/"><b>Paper</b></a> &nbsp; | &nbsp;
  🏠 <a href="https://github.com/Zhixin-L/PrefDiag-Bench"><b>Project Page</b></a> &nbsp; | &nbsp;
  🤗 <a href="https://huggingface.co/datasets"><b>Dataset</b></a>
</p>

<p align="center">
  If you find this work useful, please consider starring ⭐ the repository to support our research.
</p>

<p align="center">
  <em>Code and data will be released. Resource links are placeholders until publication.</em>
</p>

## 📖 PrefDiag-Bench Overview

Personalized GUI agents must not only complete tasks, but also adapt their decisions and execution to individual preferences. **PrefDiag-Bench** evaluates this ability through **318 mobile GUI tasks** across seven application domains and **1,664 diagnostic probes**.

Each task family pairs a Basic task with five personalized variants: **Outcome, Constraint, Ranking, Process, and Interaction**. User context is provided as either **explicit user profiles** or **behavioral memory logs**.

The **P1-P5 probes** examine memory induction, evidence selection, relevance selection, trigger recognition, and operation mapping, connecting preference understanding to task execution.

<p align="center">
  <img src="assets/overview.png" width="960" alt="PrefDiag-Bench: five ways preferences change GUI execution and the state-dependent timing of confirmation">
</p>

## 📑 Citation

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

## ✉️ Contact

For questions about the benchmark or its release, please open a [GitHub issue](https://github.com/Zhixin-L/PrefDiag-Bench/issues).
