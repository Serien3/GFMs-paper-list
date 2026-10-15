## Preface

本仓库记录关于 GFM (Genomic Foundation Models) 的文章。看过的文章会至少用一句话概括内容，有些还会有 notes (多数为 AI 写作的)。只有标题的就是还没看过的，只是先存档到这里。

⭐ 表示已做笔记

### Update

# GFM

1. ⭐ [ICML-2026]dnaHNet: A Scalable and Hierarchical Foundation Model for Genomic Sequence Learning [[paper]](https://openreview.net/forum?id=6pN2KNCspk)    分词不该是模型之外的预处理，而该是模型内部一个逐位置、可微、严格因果的决策——边界概率由相邻表示的余弦相似度给出，边界处的编码器状态充当"记忆检查点"，主网络只在这些检查点上推理（R=6 时注意力成本降 36×），解码器在检查点之间用自己的循环状态补齐碱基级细节，全程靠 NLL 加一个锚定压缩率的 ratio loss 端到端训练。在这套 H-Net 原装机制上，dnaHNet 真正的增量是把 DNA 配方调通（α 从 0.03 降到 ~0.01、编解码器容量 15%→30%、两级压缩比 (3,2)）并用 100+ 模型的 scaling sweep 证明：同预算下 perplexity 随 FLOPs 下降更快（指数 0.06 对 SH2 的0.04），10⁶ nt 推理少 3.89× FLOPs，零样本 VEP 和基因必需性都压过同语料自训的 SH2；最漂亮的是学出来的边界自己拼出了密码子周期性和 SD 基序、启动子这类功能结构，说明预测压力加计算预算能让分层表示自发涌现。但记住三条边界：架构和洞见是 H-Net 的，本文是把它在基因组上验证和驯服；"SOTA" 是 matched-budget 相对自训基线的，从未对比 Evo 2 官方 checkpoint；FLOPs 优势只在 10⁶ nt 以内成立，per-token 成本 c₁ + c₂·L/R² 终将越过线性架构。
2. [ICML-2026]Predicting evolutionary rate as a pretraining task improves genome language model representations [[paper]](https://openreview.net/forum?id=FOIP4Blm4F)
3. [ICLR-2026]Learnable Tokenization for DNA Foundational Models [[paper]](https://openreview.net/forum?id=1kpkaJKDXW)    这篇论文的可迁移原则是：当信息密度在输入上不均匀时，把压缩边界交给任务损失去训练，分词就会自动变成信息密度图——DNACHUNKER 的分词因此无监督地复现了启动子/外显子/重复区的功能注释。它的技术增量是把 H-Net 的动态 chunking 装进双向 MLM 的必经手术：cross-attention 内容路由替代插值上采样，mask 强制边界防止路由器退化，二者缺一移植必死。工程价值已证（156M 对 1.2B 的基准胜出、对 InDel 的鲁棒性），但"learnable 分词带来下游收益"缺少同架构固定块对照，因果链未闭环，且 α/λ 等关键超参数未公开，复现需要自己补实验。
4. [arXiv-2025]MergeDNA: Context-aware Genome Modeling with Dynamic Tokenization through Token Merging [[paper]](https://arxiv.org/abs/2511.14806)

