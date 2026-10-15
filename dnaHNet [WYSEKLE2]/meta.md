---
key: WYSEKLE2
version: 4
itemType: conferencePaper
title: 'dnaHNet: A Scalable and Hierarchical Foundation Model for Genomic Sequence Learning'
abstractNote: Genomic foundation models have the potential to decode DNA syntax, yet face a fundamental tradeoff. Standard subword tokenizers fragment biologically meaningful motifs such as codons and regulatory elements, while nucleotide-level models preserve biological coherence but incur prohibitive computational costs for long contexts. We introduce dnaHNet, a state-of-the-art tokenizer-free autoregressive model that segments and models genomic sequences end to end. Using a differentiable dynamic chunking mechanism, dnaHNet compresses raw nucleotides into latent tokens adaptively, balancing compression with predictive accuracy. Pretrained on prokaryotic genomes, dnaHNet outperforms leading architectures including StripedHyena2 in scaling and efficiency. This recursive chunking yields quadratic FLOP reductions, enabling $>3 \times$ inference speedup over Transformers. On zero-shot tasks, dnaHNet achieves superior performance in predicting protein variant fitness and gene essentiality,
  while automatically discovering hierarchical biological structures without supervision. These results establish dnaHNet as a scalable, interpretable framework for next-generation genomic modeling.
date: 2026/06/24
language: en
shortTitle: dnaHNet
libraryCatalog: openreview.net
url: https://openreview.net/forum?id=6pN2KNCspk
accessDate: '2026-09-30T00:10:31Z'
conferenceName: Forty-third International Conference on Machine Learning
creators:
- Arnav Shah
- Junzhe Li
- Parsa Idehpour
- Adibvafa Fallahpour
- Brandon Wang
- Sukjun Hwang
- Bo Wang
- Patrick D. Hsu
- Hani Goodarzi
- Albert Gu
zoteroTags: []
collections:
- 6K4MW3BR
relations: {}
dateAdded: '2026-09-30T00:10:31Z'
dateModified: '2026-09-30T00:10:31Z'
---
