# This Artwork Does Not Exist
Artwork generated using [guided diffusion](https://github.com/openai/guided-diffusion) by turning text into images with [CLIP](https://openai.com/blog/clip/).

## Model Name

512x512 diffusion (unconditional ImageNet)

### Modality

Images

### Intended Use

Generation of images with or without classifier guidance

## Detailed description

A 512x512 unconditional ImageNet diffusion model, fine-tuned for 8100 steps from the OpenAI trained 512x512 class-conditional ImageNet diffusion model. It was fine-tuned into an unconditional model in order to enable better guidance by CLIP (or any other non-ImageNet classifier).

## Short description

A 512x512 unconditional ImageNet diffusion model, fine-tuned from the OpenAI trained 512x512 class-conditional ImageNet diffusion model.

## License
MIT

## Training Data

ImageNet (ILSVRC 2012 subset)

Metrics / Evaluations: None
Limitations and Biases: -
Those of the parent model: -

These models sometimes produce highly unrealistic outputs, particularly when generating images containing human faces. This may stem from ImageNet's emphasis on non-human objects.

While classifier guidance can improve sample quality, it reduces diversity, resulting in some modes of the data distribution being underrepresented. This can potentially amplify existing biases in the training dataset such as gender and racial biases.

Because ImageNet and LSUN contain images from the internet, they include photos of real people, and the model may have memorized some of the information contained in these photos. However, these images are already publicly available, and existing generative models trained on ImageNet have not demonstrated significant leakage of this information.

Links: https://arxiv.org/abs/2105.05233 (Diffusion Models Beat GANs on Image Synthesis), https://github.com/openai/guided-diffusion
