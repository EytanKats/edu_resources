# MICCAI 2021: papers to dive in

___

### Self-supervised Visual Representation Learning for Histopathological Images
Yang et al.

This paper proposes **self-supervised** pretraining method for histopathological images.
Augmentation-based **contrastive learning** adopted for self-supervision 
while pretrained generative model used as a regularizer to prevent encoder collapse.

___

### TransPath: Transformer-Based Self-supervised Learning for Histopathological Image Classification
Wang et al.

This paper proposes **self-supervised** pretraining method for histopathological images.
Hybrid architecture consisting of convolutional and **transformer** parts is used to capture both local and global features.
Augmentation-based **contrastive learning** adopted for self-supervision
while two parallel paths shares a similar structure but different network weights.

___

### Self-Supervised Longitudinal Neighbourhood Embedding
Ouyang et al.

This paper proposes **self-supervised** pretraining method for longitudinal brain MRIs.
Very interesting technique of matching latent vectors directions (of different subjects) is used **to shape latent space**.
As a result, **the latent space encodes the global morphological change** linked to aging.

___

### Learning from Subjective Ratings Using Auto-Decoded Deep Latent Embeddings
Li et al.

This paper proposes training strategy to overcome the probelem of **inter-rater variablitity**.
During training **rater-specific latent embedding** is learned for each rater and further merged with activation maps of ResNet blocks.
In this way model is aware of rater-specific annotation *style*.
During inference mean of all or *most sucessfull* (accoding to validation) raters can be taken as final prediction.

___

### AutoFB: Automating Fetal Biometry Estimation from Standard Ultrasound Planes
Bano et al.

This paper proposes framework to perform **all the relevant measurements for fetal weight estimation within a unified automated system**.
First, given ULS standard plane multiclass segmentation is applied while classes are head, abdomen, femur and background.
Next, segmentation mask is adjusted using shape prior.
Finally measurements are taken while **metric scale (px/mm) is extracted automatically** from caliper visible on the left-hand side of US images.

___

### Detecting when pre-trained nnU-Net models fail silently for Covid-19 lung lesion segmentation
Gonzalez et al.

This paper proposes method to estimate **uncertainty of segmentation** and detect **Out-of-Distribution samples**.
The method is based on calculation Mahalanobis distance for inference sample from Gaussian distribution estimated for training dataset. 
Mahalanobis distance is computed in low-dimensional feature space to ensure computationally inexpensive calculation.
Proposed approach can be **seamlessly integrated into segmentation pipelines** without requiring changes in model architecture or training procedure.

___

### CoTr: Efficiently Bridging CNN and Transformer for 3D Medical Image Segmentation
Xie et al.

This paper proposes **hybrid architecture consisting of convolutional and transformer parts** for 3D segmentation task.
In order to enable use of multi-scale feature maps as input to transformer **deformable self-attention mechanism** was utilized that 
significantly reduced computational and spatial complexity.

___

### Orthogonal Ensemble Networks for Biomedical Image Segmentation
Larrazabal et al.

This paper propose method to enforce **diversity of models in ensamble** by using filter-wise **inter-model orthogonal constraints** during training.
Models in ensamble trained sequentially.

___

### Federated Contrastive Learning for Volumetric Medical Image Segmentation
Wu et al.

This paper proposes **self-supervised** pretraining method within the framework of **federated learning**.
**Momentum** encoder of each client produces feature vectors which further shared with other clients.
**Contrastive loss** is computed by each client based on both local and remote features.
Features are considered to be positive if originated from the same anatomical region.

___





