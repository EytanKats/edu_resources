 
#### Self-supervised learning
- [Momentum Contrast for Unsupervised Visual Representation Learning](#small_blue_diamond-momentum-contrast-for-unsupervised-visual-representation-learning)
- [A Simple Framework for Contrastive Learning of Visual Representations](#small_blue_diamond-a-simple-framework-for-contrastive-learning-of-visual-representations)

#### Semi-supervised learning
- [FixMatch: Simplifying Semi-Supervised Learning with Consistency and Confidence](#small_blue_diamond-fixmatch-simplifying-semi-supervised-learning-with-consistency-and-confidence)

## Self-supervised learning  

### :small_blue_diamond: Momentum Contrast for Unsupervised Visual Representation Learning
[[ArXiv](https://arxiv.org/abs/1911.05722)]
[[GitHub](https://github.com/facebookresearch/moco)]  

_Kaiming He, Haoqi Fan, Yuxin Wu, Saining Xie and Ross B. Girshick_   
_CVPR 2020_  

- Momentum Contrast (MoCo) trains a visual representation encoder by matching an encoded query to a dictionary of encoded keys using contrastive loss.  
- A query and a key are considered as a positive pair if they originated from the same image under random data augmentation.  
- The encoded keys are sampled from the dictionary. The Dictionary is built as a queue, with the current mini-batch enqueued and the oldest mini-batch dequeued.  
- The keys are encoded by a slowly progressing encoder, driven by a momentum update with the query encoder.

### :small_blue_diamond: A Simple Framework for Contrastive Learning of Visual Representations
[[ArXiv](https://arxiv.org/abs/2002.05709)]
[[GitHub](https://github.com/google-research/simclr)]

_Ting Chen, Simon Kornblith, Mohammad Norouzi and Geoffrey Hinton_  
_ICML 2020_

- An encoder network is trained using a contrastive loss.
- The contrastive loss calculated based on samples in current minibatch only, without sampling negative examples explicitly:
  - A data augmentation module transforms any given data example randomly resulting in two correlated views of the same example.
  - A neural network base encoder extracts representation vectors from augmented data examples.
  - A small neural network projection head maps representations to the space where contrastive loss is applied.
  - Two correlated views of the same example considered as a positive pair while other augmented examples within a minibatch treated as negative examples.

## Semi-supervised learning

### :small_blue_diamond: FixMatch: Simplifying Semi-Supervised Learning with Consistency and Confidence
[[ArXiv](https://arxiv.org/abs/2001.07685)]
[[GitHub](https://github.com/google-research/fixmatch)]

_Kihyuk Sohn, David Berthelot, Chun-Liang Li, Zizhao Zhang, Nicholas Carlini, Ekin Dogus Cubuk, Alexey Kurakin, Han Zhang and Colin Raffel._  
_NeurIPS 2020_  

- The loss function for FixMatch consists of two cross-entropy loss terms: supervised and unsupervised.
- The supervised loss is the standard cross-entropy loss applied on weakly augmented labeled examples.
- The unsupervised cross-entropy loss encourages a prediction on a strongly augmented version of the unlabeled example match its' pseudo-label.
- The pseudo-label computed from the model prediction on a weakly augmented version of the unlabeled example: when the model assigns a probability to any class which is above a threshold, the prediction is converted to an one-hot pseudo-label.
