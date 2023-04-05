## Unsupervised Domain Adaptation

### :small_blue_diamond: Unsupervised Domain Adaptation through Shape Modeling for Medical Image Segmentation
_Jul 2022, MIDL_  

[[ArXiv](https://arxiv.org/abs/2207.02529)]
[[GitHub](https://github.com/yyNoBug/VAE_segmentation)]

#### Main idea
At first step VAE network is trained on the source domain with the objective to reconstruct the ground truth masks. At the second step fixed VAE network is used as a regularizer for masks (shapes) produced during training of target domain segmentation model.

<img src="medical_unsupervised_domain_adaptation_images/shape_modeling_framework.png" height="400" />

##

### :small_blue_diamond: Unsupervised Domain Adaptation for Medical Image Segmentation via Self-Training of Early Features
_Dec 2021, MIDL_  

[[OpenReview](https://openreview.net/forum?id=wc9qnxw35tS)]
[[GitHub](https://github.com/ferasha/UDAS)]

#### Main idea
Only early layers of model pretrained on labeled source domain data adapted to target domain data. This is achieved by adding a segmentation
head for early features, and using the final predictions of the network as pseudo-labels for refinement.

<img src="medical_unsupervised_domain_adaptation_images/early_features_model.png" height="400" />

##

### :small_blue_diamond: Unsupervised Domain Adaptation for Medical Imaging Segmentation with Self-Ensembling
_Nov 2018, NeuroImage_  

[[ArXiv](https://arxiv.org/abs/1811.06042)]
[[GitHub](https://github.com/neuropoly/domainadaptation)]

#### Main idea
Mean teacher framework is applied to multi-site domain adaptation for medical image segmentation.

<img src="medical_unsupervised_domain_adaptation_images/self_ensembling_framework.png" height="400" />
