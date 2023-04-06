# Unsupervised Domain Adaptation Hackathon Starter

:rocket: Short list of resources to spark the imagination and to ensure the fast start  

## Collections

- Awesome Domain Adaptation, [[GitHub](https://github.com/zhaoxin94/awesome-domain-adaptation)]  

- Leaderbord For Unsupervised Domain Adaptation methods, [[Page](https://uda-survey.github.io/survey/leaderboard)]  
<sup>Thanks to Ron for pointing out to this page  :blush:</sup>

## Surveys

- Domain Adaptation for Medical Image Analysis: A Survey, _Feb 2021_, [[ArXiv](https://arxiv.org/abs/2102.09508)]
- Unsupervised Domain Adaptation for Semantic Image Segmentation: a Comprehensive Survey, _Dec 2021_, [[ArXiv](https://arxiv.org/abs/2112.03241)]

## Papers

:books: List of papers that span most popular ideas in medical unsupervised domain adaptation for image segmentation

### :small_blue_diamond: Unsupervised Domain Adaptation through Shape Modeling for Medical Image Segmentation
_Jul 2022, MIDL_  

[[ArXiv](https://arxiv.org/abs/2207.02529)]
[[GitHub](https://github.com/yyNoBug/VAE_segmentation)]

#### Main idea
At first step the VAE network is trained on the source domain with the objective to reconstruct the ground truth masks. At second step the fixed VAE network is used as a regularizer for masks (shapes) produced during training of the target domain segmentation model.

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

### :small_blue_diamond: Structure-Driven Unsupervised Domain Adaptation for Cross-Modality Cardiac Segmentation
_Dec 2021, TMI_  

[[IEEEXplore](https://ieeexplore.ieee.org/document/9463875)]

#### Main idea
At first step the landmark detection module is trained to extract the anatomical cardiac structure represented by a set of 3D landmarks. At second step the segmentation module is trained with domain-agnostic inputs: an extracted set of points and a set of edges from the canny operator.

<img src="medical_unsupervised_domain_adaptation_images/structure_driven_uda_framework.png" height="450" />

##

### :small_blue_diamond: Unsupervised Bidirectional Cross-Modality Adaptation via Deeply Synergistic Image and Feature Alignment for Medical Image Segmentation
_Feb 2020, TMI_  

[[ArXiv](https://arxiv.org/abs/2002.02255)]
[[GitHub](https://github.com/cchen-cc/SIFA)]

#### Main idea
In order to address domain shift from complementary perspectives both image and feature alignments are learned simultaneously in the proposed framework.

<img src="medical_unsupervised_domain_adaptation_images/sifa_framework.png" height="400" />

##

### :small_blue_diamond: Unsupervised Domain Adaptation via Disentangled Representations: Application to Cross-Modality Liver Segmentation
_Jul 2019, MICCAI_  

[[ArXiv](https://arxiv.org/abs/1907.13590)]

#### Main idea
At first step the framework is trained to decompose a latent image reperesentation into a domain-invariant content space, which preserves the anatomical information, and a domain-specific style space, which represents the modality information. At second step the segmentation model is trained with content-only images.

<img src="medical_unsupervised_domain_adaptation_images/dadr_framework.png" height="300" />

##

### :small_blue_diamond: Data Efficient Unsupervised Domain Adaptation for Cross-Modality Image Segmentation
_Jul 2019, MICCAI_  

[[ArXiv](https://arxiv.org/abs/1907.02766)]

#### Main idea
Prior distributions for the source features and target features are forced to be close to a fixed prior distribution. To achieve this KL-divergence loss is applied between prior distributions of latent features and fixed prior distribution.

<img src="medical_unsupervised_domain_adaptation_images/data_efficient_uda_framework.png" height="350" />

##

### :small_blue_diamond: Unsupervised Domain Adaptation for Medical Imaging Segmentation with Self-Ensembling
_Nov 2018, NeuroImage_  

[[ArXiv](https://arxiv.org/abs/1811.06042)]
[[GitHub](https://github.com/neuropoly/domainadaptation)]

#### Main idea
Mean teacher framework is applied to multi-site domain adaptation for medical image segmentation.

<img src="medical_unsupervised_domain_adaptation_images/self_ensembling_framework.png" height="400" />

##

### :small_blue_diamond: Unsupervised domain adaptation in brain lesion segmentation with adversarial networks
_Dec 2016, IPMI_  

[[ArXiv](https://arxiv.org/abs/1612.08894)]

#### Main idea
Domain adaptation is achieved by applying adversarial loss to features from different layers of segmentation network. 

<img src="medical_unsupervised_domain_adaptation_images/adversarial_networks_framework.png" height="250" />
