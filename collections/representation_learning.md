- [Papers:](#papers)  
  - [self-supervised learning](#self-supervised-learning)
  - [semi-supervised learning](#self-supervised-learning)


## Papers

### Self-supervised learning  

:small_blue_diamond: __Momentum Contrast for Unsupervised Visual Representation Learning__
[[ArXiv](https://arxiv.org/abs/1911.05722)]
[[GitHub](https://github.com/facebookresearch/moco)]  

_Kaiming He, Haoqi Fan, Yuxin Wu, Saining Xie and Ross B. Girshick_   
_CVPR 2020_  

- Momentum Contrast (MoCo) trains a visual representation encoder by matching an encoded query to a dictionary of encoded keys using contrastive loss.  
- A query and a key are considered as a positive pair if they originated from the same image under random data augmentation.  
- The encoded keys are sampled from the dictionary. The Dictionary is built as a queue, with the current mini-batch enqueued and the oldest mini-batch dequeued.  
- The keys are encoded by a slowly progressing encoder, driven by a momentum update with the query encoder.

### Semi-supervised learning

:small_blue_diamond: __FixMatch: Simplifying Semi-Supervised Learning with Consistency and Confidence__
[[ArXiv](https://arxiv.org/abs/2001.07685)]
[[GitHub](https://github.com/google-research/fixmatch)]

_Kihyuk Sohn, David Berthelot, Chun-Liang Li, Zizhao Zhang, Nicholas Carlini, Ekin Dogus Cubuk, Alexey Kurakin, Han Zhang and Colin Raffel._  
_NeurIPS 2020_  

- 
