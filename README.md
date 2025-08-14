EnlightenGAN 

A GAN-based unsupervised method requiring unpaired low/normal-light images. 

Uses a generator-discriminator framework for learning image enhancement mappings. 

More prone to color artifacts but often achieves sharper visual outputs. 

Inference time: ~0.0078s/image on GPU. 

      Generator: 

A U-Net-style encoder-decoder network with skip connections. 

Takes in a low-light image and produces an enhanced image. 

Encodes image features into deep representations and decodes them with detail-preserving skip connections. 

      Discriminator: 

A PatchGAN-style CNN that learns to distinguish between real well-lit images and enhanced outputs from the generator. 

Provides adversarial loss feedback to the generator to improve realism. Multi-Component Loss: 

Adversarial Loss (from GAN training) 

Reconstruction Loss (L1 between output and input) 

Illumination Consistency Loss 

Perceptual Loss (based on VGG features) 

