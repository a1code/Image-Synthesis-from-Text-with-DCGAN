# Enhancing-Text-Embedding-for-GAN-based-Text-to-Image-Translation

**Note**: Please refer [ProjectDescription.pdf](https://github.com/a1code/Enhancing-Text-Embedding-for-GAN-based-Text-to-Image-Translation/blob/main/ProjectDescription.pdf) and [ProjectSlides.pdf](https://github.com/a1code/Enhancing-Text-Embedding-for-GAN-based-Text-to-Image-Translation/blob/main/ProjectSlides.pdf) for details.   
YouTube Link for the final presentation is [here](https://www.youtube.com/watch?v=e43h1iVaNPM).  
Colab Notebook with the full code is [here](https://github.com/a1code/Enhancing-Text-Embedding-for-GAN-based-Text-to-Image-Translation/blob/main/code.ipynb).   

**Dataset** : [Oxford-102 flowers dataset](https://www.robots.ox.ac.uk/~vgg/data/flowers/102/).  
For our implementation, we used the images that can be accessed [here](https://drive.google.com/drive/folders/1uORr7J-8jWaovhcH7IhOzFIb2liV2w7j?usp=sharing).  
For each image, we have text descriptions that can be accessed [here](https://drive.google.com/drive/folders/18H5iIRidsH7FHuz0VBI3toSWQ8M4caIt?usp=sharing).   
Due to limited RAM/GPU memory on Google Colaboratory, we resized the RGB training images to 64 x 64 spatial size.

**Implementation Summary**:  
• Implemented the DC-GAN architecture in PyTorch and trained the model with Oxford-102 flowers dataset for generating flower images from text captions.     
• Wrote modules for ResNet-50 image encoder, multihead attention Transformer text encoder, transposed convolutions as generator and a CNN image discriminator for joint training.   
• Experimented with an embedding loss formulation between the input image encodings and the corresponding text embeddings while training as an attempt to learn better representations.    

**Abstract**:  
Text-to-Image (T2I) translation aims to generate a semantically consistent and visually realistic image conditioned on a textual description. Over the recent years, advancement in GAN architectures has showed very promising results for generative image problems in general, and T2I in particular. In this work, we focus on the task of learning text representations for T2I problem, such that they effectively capture the visual characters of the corresponding images. We try to jointly learn these embeddings with the GAN model parameters, instead of pre-training the encoder as proposed in most state-of-the-art models. We expect that this experiment will provide insights into learning representations that improve the generated image qualities from existing SoTA GAN-based T2I models.

**Observations**:
The trained models can be accessed [here](https://drive.google.com/drive/folders/1HD-aTKy2Ll_qjXA5hdY9YaH1Gm3T7Kjj?usp=sharing).   
Based on analyzing the generated images on the dev set we did hyperparameter tuning for our model. The results on dev set for the last round of model tuning can be accessed [here](https://drive.google.com/drive/folders/1wk-dBL39o2_OJWK2kqs82zU0keGJadwT?usp=sharing).   
Finally, we run the generation on our held-out test set. The results can be accessed [here](https://drive.google.com/drive/folders/1oHnMIbz7cTV8eXt44XZtcuU7cGsQJDZb?usp=sharing).   
Due to time constraints we did not quantitatively measure the quality of the generated images. Instead, we relied on human evaluation to check whether generated images are well conditioned on given text descriptions.
