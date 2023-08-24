# README: Training and Inference with Stable Diffusion XL using Hugging Face's Diffusers

This README provides an overview of how to use Hugging Face's Diffusers library for training and inference with the Stable Diffusion XL model. The Stable Diffusion XL model is a powerful image-to-image translation model that leverages diffusion models.

## Table of Contents

- [Installation](#installation)
- [Training Stable Diffusion XL](#training-stable-diffusion-xl)
- [Inference with Stable Diffusion XL](#inference-with-stable-diffusion-xl)
- [Conclusion](#conclusion)

## Installation

Before starting, make sure to install the required packages using the provided commands:

```bash
!pip install git+https://github.com/huggingface/diffusers
!pip install invisible_watermark transformers accelerate safetensors
!pip install bitsandbytes
```

The above commands will install the necessary packages for working with the Stable Diffusion XL model.

## Training Stable Diffusion XL

To train the Stable Diffusion XL model, follow these steps in the notebook:

1. **Login to Hugging Face Hub:**
   Before beginning training, you'll need to log in to the Hugging Face Hub using the `notebook_login()` function. This step is necessary to access and download the required models.

2. **Define Model and Training Configuration:**
   Modify the training configurations in the script `train_dreambooth_lora_sdxl.py` to suit your requirements. You can adjust parameters like `model_name`, `OUTPUT_DIR`, `instance_prompt`, etc., to tailor the training process to your needs.

3. **Launch Training:**
   Start the training process by using the `accelerate launch` command in your terminal. The provided script `train_dreambooth_lora_sdxl.py` should be used with appropriate arguments. This command initiates the training with the specified configurations, such as batch size, learning rate, and checkpointing settings.

4. **Optional: Convert to Checkpoint (if needed):**
   If you intend to convert the trained model into a checkpoint format, you can use the provided script `convert_diffusers_to_original_stable_diffusion.py`. This step is optional and can be executed after training is complete.

By following these steps, you can effectively train the Stable Diffusion XL model according to your desired specifications. Finally saving trained LORA weights one can load them for a normal inference.
