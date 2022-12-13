Introduction:

A team of researchers and doctors from Qatar University, Doha, Qatar, have collected and indexed this dataset of 
X-ray images for hip implants from different publicly available online medical sources such as medicine journals 
(articles) and radiology websites. All images should at least include a stem and a cup of the hip implant, and 
the images have to be X-ray images. These images were carefully checked to avoid duplications and the clinical 
experts in the team evaluated each of the images to make sure that the collected X-ray images are for hip 
implants. For patients who had undergone total hip arthroplasty surgery, an anteroposterior (AP) view of the 
X-ray images for the patients with fixed (control group) and loosened hip implants were collected, while the 
X-ray images having a wire or plate attached with the implant were excluded. Authors managed to collect 200 hip
implant X-ray images

This Project implements three modern attention-free, multi-layer perceptron (MLP) based models for image 
classification:

The MLP-Mixer model, by Ilya Tolstikhin et al., based on two types of MLPs.
The FNet model, by James Lee-Thorp et al., based on unparameterized Fourier Transform.
The gMLP model, by Hanxiao Liu et al., based on MLP with gating.

					The MLP-Mixer model
The MLP-Mixer is an architecture based exclusively on multi-layer perceptrons (MLPs), that contains two types of
MLP layers:

1. One applied independently to image patches, which mixes the per-location features.
2. The other applied across patches (along channels), which mixes spatial information.

This is similar to a depthwise separable convolution based model such as the Xception model, but with two 
chained dense transforms, no max pooling, and layer normalization instead of batch normalization.

--------------------------------------------------------------------------------------------------------------

					The FNet model
The FNet uses a similar block to the Transformer block. However, FNet replaces the self-attention layer in the 
Transformer block with a parameter-free 2D Fourier transformation layer:

1. One 1D Fourier Transform is applied along the patches.
2. One 1D Fourier Transform is applied along the channels.

-------------------------------------------------------------------------------------------------------------

					The gMLP model
The gMLP is a MLP architecture that features a Spatial Gating Unit (SGU). The SGU enables cross-patch 
interactions across the spatial (channel) dimension, by:

1. Transforming the input spatially by applying linear projection across patches (along channels).
2. Applying element-wise multiplication of the input and its spatial transformation.





