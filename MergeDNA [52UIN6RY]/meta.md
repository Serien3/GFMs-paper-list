---
key: 52UIN6RY
version: 2
itemType: preprint
title: 'MergeDNA: Context-aware Genome Modeling with Dynamic Tokenization through Token Merging'
abstractNote: 'Modeling genomic sequences faces two unsolved challenges: the information density varies widely across different regions, while there is no clearly defined minimum vocabulary unit. Relying on either four primitive bases or independently designed DNA tokenizers, existing approaches with naive masked language modeling pre-training often fail to adapt to the varying complexities of genomic sequences. Leveraging Token Merging techniques, this paper introduces a hierarchical architecture that jointly optimizes a dynamic genomic tokenizer and latent Transformers with context-aware pre-training tasks. As for network structures, the tokenization module automatically chunks adjacent bases into words by stacking multiple layers of the differentiable token merging blocks with local-window constraints, then a Latent Encoder captures the global context of these merged words by full-attention blocks. Symmetrically employing a Latent Decoder and a Local Decoder, MergeDNA learns with two
  pre-training tasks: Merged Token Reconstruction simultaneously trains the dynamic tokenization module and adaptively filters important tokens, while Adaptive Masked Token Modeling learns to predict these filtered tokens to capture informative contents. Extensive experiments show that MergeDNA achieves superior performance on three popular DNA benchmarks and several multi-omics tasks with fine-tuning or zero-shot evaluation, outperforming typical tokenization methods and large-scale DNA foundation models.'
date: '2025-11-17'
shortTitle: MergeDNA
libraryCatalog: arXiv.org
url: http://arxiv.org/abs/2511.14806
accessDate: '2026-09-29T06:05:03Z'
extra: arXiv:2511.14806 [q-bio.GN]
DOI: 10.48550/arXiv.2511.14806
repository: arXiv
archiveID: arXiv:2511.14806
creators:
- Siyuan Li
- Kai Yu
- Anna Wang
- Zicheng Liu
- Chang Yu
- Jingbo Zhou
- Qirong Yang
- Yucheng Guo
- Xiaoming Zhang
- Stan Z. Li
zoteroTags:
- Computer Science - Artificial Intelligence
- Computer Science - Machine Learning
- Quantitative Biology - Genomics
collections:
- 6K4MW3BR
relations: {}
dateAdded: '2026-09-29T06:05:03Z'
dateModified: '2026-09-29T06:05:04Z'
---
