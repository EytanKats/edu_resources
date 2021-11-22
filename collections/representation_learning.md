[Papers:](#papers)  
:small_orange_diamond:[self-supervised learning](#self-supervised-learning)  
:small_orange_diamond:[semi-supervised learning](#self-supervised-learning)


## Papers

### Self-supervised learning  

:small_blue_diamond: __Momentum Contrast for Unsupervised Visual Representation Learning__
[[ArXiv](https://arxiv.org/abs/1911.05722)]
[[GitHub](https://github.com/facebookresearch/moco)]  

_Kaiming He, Haoqi Fan, Yuxin Wu, Saining Xie and Ross B. Girshick_   
_CVPR 2020_  

Momentum Contrast (MoCo) trains visual representation encoder by matching encoded query to encoded keys using contrastive loss.
Encoded keys are sampled from dictionary. Dictionary is built as a queue, with current mini-batch enqueued and oldest mini-batch dequeued.
Keys are encoded by slowly progressing encoder, driven by momentum update with query encoder.

### Semi-supervised learning
