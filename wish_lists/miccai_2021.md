# MICCAI 2021: papers to dive in

___

### [Self-supervised Visual Representation Learning for Histopathological Images](https://arxiv.org/abs/2109.03299)
Yang et al.

This paper proposes **self-supervised** pretraining method for histopathological images.
Augmentation-based **contrastive learning** adopted for self-supervision 
while pretrained generative model used as a regularizer to prevent encoder collapse.

___

### [TransPath: Transformer-Based Self-supervised Learning for Histopathological Image Classification](https://link.springer.com/chapter/10.1007/978-3-030-87237-3_18)
Wang et al.

This paper proposes **self-supervised** pretraining method for histopathological images.
Hybrid architecture consisting of convolutional and **transformer** parts is used to capture both local and global features.
Augmentation-based **contrastive learning** adopted for self-supervision
while two parallel paths shares a similar structure but different network weights.

___

### [Self-Supervised Longitudinal Neighbourhood Embedding](https://arxiv.org/abs/2103.03840)
Ouyang et al.

This paper proposes **self-supervised** pretraining method for longitudinal brain MRIs.
Very interesting technique of matching latent vectors directions (of different subjects) is used **to shape latent space**.
As a result, **the latent space encodes the global morphological change** linked to aging.

___

### [Learning from Subjective Ratings Using Auto-Decoded Deep Latent Embeddings](https://arxiv.org/abs/2104.05570)
Li et al.

This paper proposes training strategy to overcome the probelem of **inter-rater variablitity**.
During training **rater-specific latent embedding** is learned for each rater and further merged with activation maps of ResNet blocks.
In this way model is aware of rater-specific annotation *style*.
During inference mean of all or *most sucessfull* (accoding to validation) raters can be taken as final prediction.

___

### [AutoFB: Automating Fetal Biometry Estimation from Standard Ultrasound Planes](https://arxiv.org/abs/2107.05255)
Bano et al.

This paper proposes framework to perform **all the relevant measurements for fetal weight estimation within a unified automated system**.
First, given ULS standard plane multiclass segmentation is applied while classes are head, abdomen, femur and background.
Next, segmentation mask is adjusted using shape prior.
Finally measurements are taken while **metric scale (px/mm) is extracted automatically** from caliper visible on the left-hand side of US images.

___

### [Detecting When Pre-trained nnU-Net Models Fail Silently for Covid-19 Lung Lesion Segmentation](https://arxiv.org/abs/2107.05975)
Gonzalez et al.

This paper proposes method to estimate **uncertainty of segmentation** and detect **Out-of-Distribution samples**.
The method is based on calculation Mahalanobis distance for inference sample from Gaussian distribution estimated for training dataset. 
Mahalanobis distance is computed in low-dimensional feature space to ensure computationally inexpensive calculation.
Proposed approach can be **seamlessly integrated into segmentation pipelines** without requiring changes in model architecture or training procedure.

___

### [CoTr: Efficiently Bridging CNN and Transformer for 3D Medical Image Segmentation](https://arxiv.org/abs/2103.03024)
Xie et al.

This paper proposes **hybrid architecture consisting of convolutional and transformer parts** for 3D segmentation task.
In order to enable use of multi-scale feature maps as input to transformer **deformable self-attention mechanism** was utilized that 
significantly reduced computational and spatial complexity.

___

### [Orthogonal Ensemble Networks for Biomedical Image Segmentation](https://arxiv.org/abs/2105.10827)
Larrazabal et al.

This paper propose method to enforce **diversity of models in ensamble** by using filter-wise **inter-model orthogonal constraints** during training.
Models in ensamble trained sequentially.

___

### [Federated Contrastive Learning for Volumetric Medical Image Segmentation](https://link.springer.com/chapter/10.1007/978-3-030-87199-4_35)
Wu et al.

This paper proposes **self-supervised** pretraining method within the framework of **federated learning**.
**Momentum** encoder of each client produces feature vectors which further shared with other clients.
**Contrastive loss** is computed by each client based on both local and remote features.
Features are considered to be positive if originated from the same anatomical region.

___

### [Controllable Cardiac Synthesis via Disentangled Anatomy Arithmetic](https://arxiv.org/abs/2107.01748)
Thermos et al.

This paper proposes **framework to generate cardiac images with desired characteristics** (for example with specific pathology).
Image is generated from **disentagled representations of anatomy structures** (left ventricle, right ventricle and myocardium)
and **disentangled representation of imaging modality** (MRI).
Disentanglment is based on the previous work and this work is focuses only on image generation.
Proposed approach can be used to enrich existing dataset by generating images with rare medical conditions.

___

### [Collaborative Image Synthesis and Disease Diagnosis for Classification of Neurodegenerative Disorders with Incomplete Multi-modal Neuroimages](https://link.springer.com/chapter/10.1007/978-3-030-87240-3_46)
Pan et al.

This paper proposes **framework for multi-modal (PET and MRI) diagnosis**.
This framework is **able to generate missing modality (if missing) from the existing one**.
Sysnthesis and diagnosis modules are **trained collaborately**.
This poses feature-consistent constraint to the synthesis process while diagnosis module trained on both real and synthesized images.

___

### [Semi-supervised Meta-learning with Disentanglement for Domain-generalised Medical Image Segmentation](https://arxiv.org/abs/2106.13292)
Liu et al.

This paper proposes **semi-supervised domain generalization** framework.
Domain generalization is achieved by two techniques: **(1) meta-learning and (2) disentanglment**.
For each iteration of training domain shift is simulating by randomly splitting the source domains to meta-train set and meta-test set.
Image features are disentangled to 3 components: (1) anatomy information, (2) common cross-domain imaging characteristics and (3) specific imaging characteristics for each domain.

___

### [Cooperative Training and Latent Space Data Augmentation for Robust Medical Image Segmentation](https://arxiv.org/abs/2107.01079)
Chen et al.

This paper proposes a **cooperative training framework** for learning a **robust segmentation network from single-domain data**.
First model in framework learns image features for image reconstruction and shape features for initial segmentation while second refines initial segmentation.
Latent space augmentation generates challenging examples by masking the most task-important latent space features. 





