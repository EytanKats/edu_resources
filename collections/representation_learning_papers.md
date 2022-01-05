 
#### Self-supervised learning
- [Mean Shift for Self-Supervised Learning](#small_blue_diamond-mean-shift-for-self-supervised-learning)   
:star:  
_May 2021, ICCV_
- [Bootstrap Your Own latent: A New Approach to Self-Supervised Learning](#small_blue_diamond-bootstrap-your-own-latent-a-new-approach-to-self-supervised-learning)   
:star: :star: :star: :star:  
_Jun 2020, NeurIPS_
- [Improved Baselines with Momentum Contrastive Learning](#small_blue_diamond-improved-baselines-with-momentum-contrastive-learning)  
:star: :star: :star: :star:  
_Mar 2020, ArXiv_
- [A Simple Framework for Contrastive Learning of Visual Representations](#small_blue_diamond-a-simple-framework-for-contrastive-learning-of-visual-representations)  
:star: :star: :star: :star: :star:  
_Feb 2020, ICML_
- [Momentum Contrast for Unsupervised Visual Representation Learning](#small_blue_diamond-momentum-contrast-for-unsupervised-visual-representation-learning)  
:star: :star: :star: :star: :star:  
_Nov 2019, CVPR_ 

#### Semi-supervised learning
- [Meta Pseudo Labels](#small_blue_diamond-meta-pseudo-labels)  
:star: :star:  
_Mar 2020, CVPR_
- [FixMatch: Simplifying Semi-Supervised Learning with Consistency and Confidence](#small_blue_diamond-fixmatch-simplifying-semi-supervised-learning-with-consistency-and-confidence)  
:star: :star: :star: :star:  
_Jan 2020, NeurIPS_
- [S4L: Self-Supervised Semi-Supervised Learning](#small_blue_diamond-s4l-self-supervised-semi-supervised-learning)  
:star: :star: :star:  
_May 2019, ICCV_

## Self-supervised learning  

### :small_blue_diamond: Mean Shift for Self-Supervised Learning
[[ArXiv](https://arxiv.org/abs/2105.07269)]
[[GitHub](https://github.com/UMBCvision/MSF)]

_Soroush Abbasi Koohpayegani, Ajinkya Tejankar and Hamed Pirsiavash_  
_May 2021, ICCV_

- Similar to [BYOL](https://arxiv.org/abs/2006.07733), MSF method maintains two encoders (target and online).
- The online encoder is updated with gradient descent while the target encoder is the moving average of the online encoder.
- Two different augmentations of an image are fed to these two encoders.
- The target embedding is added to the memory bank.
- The online embedding of the image is pushed to be close to the average of nearest neighbors of the target embedding from the memory bank (obviously target embedding itself will be the first nearest neighbor).
- Nearest neighbors act as a proxy for strong augmentations of the query image, so the requirement for engineering strong augmentations can be relaxed.
- MSF method using only one nearest neighbor is identical to [BYOL](https://arxiv.org/abs/2006.07733).


### :small_blue_diamond: Bootstrap Your Own latent: A New Approach to Self-Supervised Learning
[[ArXiv](https://arxiv.org/abs/2006.07733)]
[[GitHub](https://github.com/deepmind/deepmind-research/tree/master/byol)]

_Jean-Bastien Grill, Florian Strub, Florent Altch'e, Corentin Tallec, Pierre H. Richemond, Elena Buchatskaya,
Carl Doersch, Bernardo Avila Pires, Zhaohan Daniel Guo, Mohammad Gheshlaghi Azar, Bilal Piot, Koray Kavukcuoglu, Rémi Munos and Michal Valko_  
_Jun 2020, NeurIPS_

- BYOL uses two neural networks to learn: the online and target networks.
- The online network is comprised of three stages: an encoder, a projector and a predictor.
- The target network is comprised of two stages: an encoder and a projector.
- The parameters of target network are an exponential moving average of the online parameters.
- Mean squared loss is applied between the normalized online predictions and normalized target projections
that corresponds to two different augmentations of the same image.

### :small_blue_diamond: Improved Baselines with Momentum Contrastive Learning
[[ArXiv](https://arxiv.org/abs/2003.04297)]
[[GitHub](https://github.com/facebookresearch/moco)]

_Xinlei Chen, Haoqi Fan, Ross B. Girshick and Kaiming He_  
_Mar 2020, ArXiv_

- Two design improvements used in [SimCLR](https://arxiv.org/abs/2002.05709)
applied to [MoCo](https://arxiv.org/abs/1911.05722) framework:
  - MLP projection head.
  - Stronger data augmentation.

### :small_blue_diamond: A Simple Framework for Contrastive Learning of Visual Representations
[[ArXiv](https://arxiv.org/abs/2002.05709)]
[[GitHub](https://github.com/google-research/simclr)]

_Ting Chen, Simon Kornblith, Mohammad Norouzi and Geoffrey Hinton_  
_Feb 2020, ICML_

- An encoder network is trained using a contrastive loss.
- The contrastive loss calculated based on samples in current minibatch only, without sampling negative examples explicitly:
  - A data augmentation module transforms any given data example randomly resulting in two correlated views of the same example.
  - A neural network base encoder extracts representation vectors from augmented data examples.
  - A small neural network projection head maps representations to the space where contrastive loss is applied.
  - Two correlated views of the same example considered as a positive pair while other augmented examples within a minibatch treated as negative examples.

### :small_blue_diamond: Momentum Contrast for Unsupervised Visual Representation Learning
[[ArXiv](https://arxiv.org/abs/1911.05722)]
[[GitHub](https://github.com/facebookresearch/moco)]  

_Kaiming He, Haoqi Fan, Yuxin Wu, Saining Xie and Ross B. Girshick_   
_Nov 2019, CVPR_  

- Momentum Contrast (MoCo) trains a visual representation encoder by matching an encoded query to a dictionary of encoded keys using contrastive loss.  
- A query and a key are considered as a positive pair if they originated from the same image under random data augmentation.  
- The encoded keys are sampled from the dictionary. The dictionary is built as a queue, with the current mini-batch enqueued and the oldest mini-batch dequeued.  
- The keys are encoded by a slowly progressing encoder, driven by a momentum update with the query encoder.

## Semi-supervised learning

### :small_blue_diamond: Meta Pseudo Labels
[[ArXiv](https://arxiv.org/abs/2003.10580)]
[[GitHub](https://github.com/google-research/google-research/tree/master/meta_pseudo_labels)]

_Hieu Pham, Qizhe Xie, Zihang Dai and Quoc V. Le_  
_Mar 2020, CVPR_

- MPL trains the student model to minimize the cross-entropy loss on unlabeled data where the pseudo target is produced by the teacher model.
- The teacher model is trained along with the student model based on the performance of the student on labeled data.
- The teacher’s training is augmented with a supervised learning objective and a semi-supervised learning objective.
  - For the supervised objective, the teacher is trained on labeled data.
  - For the semi-supervised objective, the teacher is trained on unlabeled data using the UDA objective.

### :small_blue_diamond: FixMatch: Simplifying Semi-Supervised Learning with Consistency and Confidence
[[ArXiv](https://arxiv.org/abs/2001.07685)]
[[GitHub](https://github.com/google-research/fixmatch)]

_Kihyuk Sohn, David Berthelot, Chun-Liang Li, Zizhao Zhang, Nicholas Carlini, Ekin Dogus Cubuk, Alexey Kurakin, Han Zhang and Colin Raffel_  
_Jan 2020, NeurIPS_ 

- The loss function for FixMatch consists of two cross-entropy loss terms: supervised and unsupervised.
- The supervised loss is the standard cross-entropy loss applied on weakly augmented labeled examples.
- The unsupervised cross-entropy loss encourages a prediction on a strongly augmented version of the unlabeled example match its' pseudo-label.
- The pseudo-label computed from the model prediction on a weakly augmented version of the unlabeled example: when the model assigns a probability to any class which is above a threshold, the prediction is converted to an one-hot pseudo-label.

### :small_blue_diamond: S4L: Self-Supervised Semi-Supervised Learning
[[ArXiv](https://arxiv.org/abs/1905.03670)]
[[GitHub](https://github.com/google-research/s4l)]

_Xiaohua Zhai, Avital Oliver, Alexander Kolesnikov and Lucas Beyer_  
_May 2019, ICCV_

- The learning objective of the S4L method consists of two terms: supervised and unsupervised.
- The supervised loss is the standard cross-entropy loss applied on labeled examples.
- The unsupervised loss is the task specific loss applied on unlabeled examples:
  - Crossentropy loss for [rotation prediction](https://arxiv.org/abs/1803.07728) task.
  - [Batch hard triplet loss with soft margin](https://arxiv.org/abs/1703.07737) for [exemplar](https://arxiv.org/abs/1406.6909) task.
