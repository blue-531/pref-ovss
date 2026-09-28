# Preference-Guided Adaptation for Open-Vocabulary Semantic Segmentation via Prompt Disagreement

<p align="center">
  <a href="https://blue-531.github.io/">Hyun-Kurl Jang</a>,
  <a href="https://jihun1998.github.io/">Jihun Kim</a> and
  Kuk-Jin Yoon
  <br>
  KAIST
  <br>
  <b>NeurIPS 2026</b>
</p>

<div align="center">
  
 [![arXiv](https://img.shields.io/badge/arXiv-2405.17427-red)](https://arxiv.org/abs/2410.15674)
[![Project](https://img.shields.io/badge/project-page-green)](https://blue-531.github.io/pref-ovss/)

</div>

![teaser](assets/teaser.gif)


## 💥 News

- **[2026.09]** Our paper is accepted to **NeurIPS 2026** 🎉!
- **[2026.09]** The [project page](https://blue-531.github.io/pref-ovss/) is online.
- Code will be released soon. Stay tuned!


## Introduction

Open-vocabulary semantic segmentation (OVSS) models degrade in specialized domains such as medical
imaging, remote sensing and industrial inspection, where dense pixel-level masks for adaptation are
costly and require expert knowledge. We propose a **preference-guided adaptation** framework that
replaces dense mask supervision with **binary preferences**. Different prompt templates produce
systematically different segmentations of the same image, a phenomenon we call **prompt disagreement**,
and we repurpose it as a source of preference supervision. We mine a localized preference
query from the region where the templates disagree most, and adapt the model with
**R**egion-**L**ocalized **P**reference **O**ptimization (**RLPO**) together with a consistency
regularizer that stabilizes the prediction outside the queried region.


## Code

TBD


## Citation

TBD


## Acknowledgement

We thank [CAT-Seg](https://github.com/cvlab-kaist/CAT-Seg), [SAN](https://github.com/MendelXu/SAN)
and [MESS](https://github.com/blumenstiel/MESS) for sharing their source code.
