#### Self-supervised learning
- [Bootstrap Your Own latent: A New Approach to Self-Supervised Learning](#small_blue_diamond-bootstrap-your-own-latent-a-new-approach-to-self-supervised-learning)    
_Jun 2020, NeurIPS_
- [Improved Baselines with Momentum Contrastive Learning](#small_blue_diamond-improved-baselines-with-momentum-contrastive-learning)   
_Mar 2020, ArXiv_
- [A Simple Framework for Contrastive Learning of Visual Representations](#small_blue_diamond-a-simple-framework-for-contrastive-learning-of-visual-representations)  
_Feb 2020, ICML_
- [Momentum Contrast for Unsupervised Visual Representation Learning](#small_blue_diamond-momentum-contrast-for-unsupervised-visual-representation-learning)    
_Nov 2019, CVPR_ 

#### Semi-supervised learning
- [Meta Pseudo Labels](#small_blue_diamond-meta-pseudo-labels)  
_Mar 2020, CVPR_
- [FixMatch: Simplifying Semi-Supervised Learning with Consistency and Confidence](#small_blue_diamond-fixmatch-simplifying-semi-supervised-learning-with-consistency-and-confidence)  
_Jan 2020, NeurIPS_
- [S4L: Self-Supervised Semi-Supervised Learning](#small_blue_diamond-s4l-self-supervised-semi-supervised-learning)  
_May 2019, ICCV_  
- [Virtual Adversarial Training: A Regularization Method for Supervised and Semi-Supervised Learning](#small_blue_diamond-virtual-adversarial-training-a-regularization-method-for-supervised-and-semi-supervised-learning)  
_Apr 2017, IEEE transactions on pattern analysis and machine intelligence_  
- [Mean Teachers are Better Role Models: Weight-Averaged Consistency Targets Improve Semi-Supervised Deep Learning Results](#small_blue_diamond-mean-teachers-are-better-role-models-weight-averaged-consistency-targets-improve-semi-supervised-deep-learning-results)  
_Mar 2017, NeurIPS_  
- [Temporal Ensembling for Semi-Supervised Learning](#small_blue_diamond-temporal-ensembling-for-semi-supervised-learning)  
_Oct 2016, ICLR_  
- [Pseudo-Label: The Simple and Efficient Semi-Supervised Learning Method for Deep Neural Networks](#small_blue_diamond-pseudo-label-the-simple-and-efficient-semi-supervised-learning-method-for-deep-neural-networks)   
_Jun 2013, Workshop on Challenges in Representation Learning, ICML_  

## Self-supervised learning  

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

### :small_blue_diamond: Virtual Adversarial Training: A Regularization Method for Supervised and Semi-Supervised Learning
[[ArXiv](https://arxiv.org/abs/1704.03976)]
[[GitHub](https://github.com/takerum/vat_tf)]

_Takeru Miyato, Shin-Ichi Maeda, Masanori Koyama and Shin Ishii_  
_Apr 2017, IEEE transactions on pattern analysis and machine intelligence_  

- The proposed regularization technique is a method that trains the output distribution to be isotropically smooth around each input data point by selectively smoothing the model in its most anisotropic direction.
- The most anisotropic direction at an input data point (virtual adversarial direction) is a direction of the perturbation that can most greatly alter the output distribution in the sense of distributional divergence.
- Distributional divergence defined between model output from original input and model output from input with random perturbation.
- Virtual adversarial direction is calculated by taking the gradient of distributional divergence with respect to random perturbation.
- In this way virtual adversarial direction can be calculated on unlabeled data point.

### :small_blue_diamond: Mean Teachers are Better Role Models: Weight-Averaged Consistency Targets Improve Semi-Supervised Deep Learning Results
[[ArXiv](https://arxiv.org/abs/1703.01780)]
[[GitHub](https://github.com/CuriousAI/mean-teacher)]

_Antti Tarvainen and Harri Valpola_  
_Mar 2017, NeurIPS_  

- The proposed framework consists of two models: the student model and the teacher model.
- Both models evaluate the same input applying noise within their computation.
- The softmax output of the student model is compared with:
  - One-hot ground-truth label using classification cost (only for labeled data).
  - Teacher's output using consistency cost (for both labeled data and unlabeled data).
- Weights of the student model are updated with gradient descent.
- Weights of the teacher model are updated as an exponential moving average of the student's weights.

### :small_blue_diamond: Temporal Ensembling for Semi-Supervised Learning
[[ArXiv](https://arxiv.org/abs/1610.02242)]
[[GitHub](https://github.com/smlaine2/tempens)]

_Samuli Laine and Timo Aila_  
_Oct 2016, ICLR_

- Loss function of П-model consists of two components:
  - The first component is the standard cross-entropy loss, evaluated for labeled inputs only.
  - The second component, evaluated for all inputs, encourages consistent network output between two realizations of the same input stimulus, under two different augmentations and under two different dropout conditions.
- In temporal ensembling approach the network outputs from different epochs for the same data sample accumulated into weighted average with recent epochs having larger weight than distant epochs:
  - The first component of the temporal ensembling loss function is the standard cross-entropy loss, evaluated for labeled inputs only.
  - The second component, evaluated for all inputs, encourages consistency between the current network output and weighted average of the network outputs from previous epochs.

### :small_blue_diamond: Pseudo-Label: The Simple and Efficient Semi-Supervised Learning Method for Deep Neural Networks
[[ResearchGate](https://www.researchgate.net/publication/280581078_Pseudo-Label_The_Simple_and_Efficient_Semi-Supervised_Learning_Method_for_Deep_Neural_Networks)]

_Dong-Hyun Lee_  
_Jun 2013, Workshop on Challenges in Representation Learning, ICML_

- The model is trained in a supervised fashion with labeled and unlabeled data simultaneously.
- For unlabeled data, pseudo-labels are used as if they were true labels.
- Pseudo-label defined as the class which has maximum predicted probability for the unlabeled sample.
- Pseudo-labels recalculated every weights update.
