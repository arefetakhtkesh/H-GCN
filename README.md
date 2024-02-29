# H-GCN
## Description
This is the repository for the IJCAI-19 paper [Hierarchical Graph Convolutional Networks for Semi-supervised Node Classiﬁcation](https://arxiv.org/pdf/1902.06667.pdf).

## Requirements

- Tensorflow (1.9.0)
- networkx

## Usage

You can conduct node classification experiments on citation network (WebKB, Citeseer or Pubmed) with the following commands:

```bash
python train.py --dataset webkb --epochs 60 --early_stopping 1000 --coarsen_level 4 --dropout 0.85 --weight_decay 7e-4 --hidden 32 --node_wgt_embed_dim 8 --seed1 156 --seed2 136
```

```bash
python train.py --dataset citeseer --epochs 200 --early_stopping 60 --coarsen_level 4 --dropout 0.85 --weight_decay 7e-4 --hidden 30 --node_wgt_embed_dim 15 --seed1 156 --seed2 156
```

```bash
python train.py --dataset pubmed --epochs 250 --early_stopping 1000 --coarsen_level 4 --dropout 0.85 --weight_decay 7e-4 --hidden 30 --node_wgt_embed_dim 8 --seed1 156 --seed2 136
```