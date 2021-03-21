### Kiu-net: Towards accurate segmentation of biomedical images using over-complete representations

Valanarasu, J.M.J., Sindagi, V.A., Hacihaliloglu, I. and Patel, V.M., 2020, October.  
In International Conference on Medical Image Computing and Computer-Assisted Intervention (pp. 363-373). Springer, Cham.

[Paper](https://arxiv.org/abs/2006.04878) | [Code](https://github.com/jeya-maria-jose/KiU-Net-pytorch) | [Summary](/paper_summary/kiu-net.md)

**Main contribution**  
Architecture combining the features of both under-complete and over-complete deep networks.  
This architecture captures finer details better than the standard encoder-decoder architecture of U-Net
thus aiding in precise segmentation.


### TransUNet: Transformers Make Strong Encoders for Medical Image Segmentation

Chen, J., Lu, Y., Yu, Q., Luo, X., Adeli, E., Wang, Y., Lu, L., Yuille, A.L. and Zhou, Y., 2021.  
arXiv preprint arXiv:2102.04306.

[Paper](https://arxiv.org/abs/2102.04306) | [Code](https://github.com/Beckschen/TransUNet)

**Main contribution**  
Hybrid CNN-Transformer architecture in which Transformer block replaces the last convolution block in U-Net encoder.  
This architecture allows to leverage both detailed high-resolution spatial information from CNN features
and the global context encoded by Transformer.
