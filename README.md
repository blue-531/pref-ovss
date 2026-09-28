# Preference-Guided Adaptation for Open-Vocabulary Semantic Segmentation via Prompt Disagreement

**NeurIPS 2026**

[Hyun-Kurl Jang](https://blue-531.github.io/), [Jihun Kim](https://jihun1998.github.io/), Kuk-Jin Yoon

KAIST

[Project page](https://blue-531.github.io/pref-ovss/) · Paper (coming soon)

> [!NOTE]
> **Code coming soon.** We are preparing the code release for this repository. Watch or star it to get notified.

![Method overview](assets/method.png)

## Overview

Open-vocabulary semantic segmentation (OVSS) models degrade in specialized domains such as medical
imaging, remote sensing and industrial inspection, where dense pixel-level masks for adaptation are
costly and require expert knowledge. We adapt OVSS models with **binary preferences** instead of masks.

Different prompt templates produce systematically different segmentations of the same image, which we
call *prompt disagreement*. We use it as a built-in source of preference supervision:

1. **Preference query mining.** Run the model with K = 14 prompt templates, localize the region where
   the templates disagree most (cross-prompt entropy), and pick the template pair that disagrees most
   inside it.
2. **Region-Localized Preference Optimization (RLPO).** A single binary answer ("which prediction is
   closer to the intended class in this region?") drives a DPO-style update on region-level scores.
3. **Consistency regularization.** Keeps predictions outside the queried region stable.

On the MESS benchmark the method improves SAN and CAT-Seg (CLIP ViT-B/16 and ViT-L/14) without any
pixel-level annotation, e.g. +10.6 mean mIoU for CAT-Seg ViT-L/14, and remains effective under noisy
preferences.

## Code release

The release will include adaptation code for the CAT-Seg and SAN backbones, the MESS dataset
registry, and scripts to reproduce the main results.

## Citation

```bibtex
@inproceedings{jang2026preference,
  title     = {Preference-Guided Adaptation for Open-Vocabulary
               Semantic Segmentation via Prompt Disagreement},
  author    = {Jang, Hyun-Kurl and Kim, Jihun and Yoon, Kuk-Jin},
  booktitle = {Advances in Neural Information Processing Systems (NeurIPS)},
  year      = {2026}
}
```
