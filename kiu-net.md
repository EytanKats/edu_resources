
# KiU-Net

Jose, V. Jeya Maria, Vishwanath Sindagi, I. Hacihaliloglu and V. Patel.
“KiU-Net: Towards Accurate Segmentation of Biomedical Images using Over-complete Representations.”
ArXiv abs/2006.04878 (2020)

[ArXiv](https://arxiv.org/abs/2006.04878) | [GitHub](https://github.com/jeya-maria-jose/KiU-Net-pytorch)


## Main contribution
Paper proposes a novel architecture combining the features of both under-complete and over-complete deep networks.  
This architecture captures finer details better than the standard encoder-decoder architecture of U-Net
thus aiding in precise segmentation.


## Intuition
The standard encoder-decoder architecture of U-Net belongs to the family of under-complete convolution auto-encoders.
The increasing receptive field size over the depth of the network constrains it to focus more
on the higher-level features.  
However, it is important to note that tiny structures require smaller receptive fields.  
In over-complete architectures the data is projected onto a higher dimension in the intermediate layers.
The filters in this type of architecture learn finer low-level features due to the decreasing size
of receptive field as we go deeper in the encoder network.

![](/images/kiu-net/receptive_field.png)


## Technical details

### Architecture
Model (KiU-Net) consists of two branches when one of them is an over-complete network (KiNet)
and other - under-complete network (UNet).  
Features from two branches combined at each block level by cross residual fusion block (CRFB).
This block extracts complementary features from both network branches and forwards to both of them respectively.  
Finally, the features from both branches are added and forwarded through 1x1 convolution layer
to produce the segmentation mask.

![](/images/kiu-net/architecture.png)


## Results

### 2D Ultrasound brain scans of preterm neonates
The dataset was collected during the study and manually annotated by an expert ultrasonographer.

Qualitative comparison:  
![](/images/kiu-net/us_dataset_qualitative_results.png)

Quantitative comparison:  
![](/images/kiu-net/us_dataset_quantitative_results.png)

### GLAnd segmentation (GLAS) dataset
GLAnd Segmentation (GLAS) dataset contains microscopic images of Hematoxylin and Eosin (H&E) stained slides
and the corresponding ground truth annotations by expert pathologists.

Qualitative comparison:  
![](/images/kiu-net/glas_dataset_qualitative_results.png)

Quantitative comparison:  
![](/images/kiu-net/glas_dataset_quantitative_results.png)


