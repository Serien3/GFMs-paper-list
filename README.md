## Preface

本仓库记录关于 GFM (Genomic Foundation Models) 的文章。看过的文章会至少用一句话概括内容，有些还会有 notes (多数为 AI 写作的)。只有标题的就是还没看过的，只是先存档到这里。

⭐ 表示已做笔记

### Update

# GFM

1. ⭐ [ICML-2026]dnaHNet: A Scalable and Hierarchical Foundation Model for Genomic Sequence Learning [[paper]](https://openreview.net/forum?id=6pN2KNCspk)    这篇论文的可迁移原则是：当信息密度在输入上不均匀时，把压缩边界交给任务损失去训练，分词就会自动变成信息密度图——DNACHUNKER 的分词因此无监督地复现了启动子/外显子/重复区的功能注释。它的技术增量是把 H-Net 的动态 chunking 装进双向 MLM 的必经手术：cross-attention 内容路由替代插值上采样，mask 强制边界防止路由器退化，二者缺一移植必死。工程价值已证（156M 对 1.2B 的基准胜出、对 InDel 的鲁棒性），但"learnable 分词带来下游收益"缺少同架构固定块对照，因果链未闭环，且 α/λ 等关键超参数未公开，复现需要自己补实验。
2. [ICML-2026]Predicting evolutionary rate as a pretraining task improves genome language model representations [[paper]](https://openreview.net/forum?id=FOIP4Blm4F)
3. [ICLR-2026]Learnable Tokenization for DNA Foundational Models [[paper]](https://openreview.net/forum?id=1kpkaJKDXW)
4. [arXiv-2025]MergeDNA: Context-aware Genome Modeling with Dynamic Tokenization through Token Merging [[paper]](https://arxiv.org/abs/2511.14806)

