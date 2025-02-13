# Stable Diffusion XL Fine-tuning Project

## Overview

This project demonstrates the process of fine-tuning Stable Diffusion XL using DreamBooth and LoRA techniques. It was developed as part of a school project to explore and understand the capabilities of modern diffusion models and their applications in generating custom images.

## Project Structure

- `fine_tuning.ipynb`: Main notebook containing the complete pipeline
- `dataset_preparation.ipynb`: Helper notebook for preparing dataset metadata
- `examples/`: Directory containing example outputs
- `requirements.txt`: List of required packages

## Prerequisites

- Google Colab (recommended) or local machine with GPU
- Hugging Face account
- Python 3.8+
- ~40GB disk space for model weights
- For Colab: T4/P100 GPU or better
- For local: NVIDIA GPU with at least 12GB VRAM

## Dataset Requirements

For optimal results, prepare your dataset following these guidelines:

### Image Requirements

- Number of images: 10-25 high-quality images
- Resolution: Minimum 1024x1024 pixels
- Format: JPG or PNG
- Content variety:
  - Different angles (front, side, 3/4 view)
  - Various lighting conditions
  - Different backgrounds
  - Multiple poses
  - Avoid blur or excessive noise

### Dataset Organization

```
dataset/
├── images/
│   ├── image_1.jpg
│   ├── image_2.jpg
│   └── ...
└── metadata.parquet
```

## Setup Instructions

### 1. Hugging Face Setup

1. Create an account on [Hugging Face](https://huggingface.co)
2. Generate an access token (Settings -> Access Tokens)
3. Create a new model repository
4. **Important**: Do not share your access token in the notebook!

### 2. Environment Setup

For Google Colab (Recommended):

1. Open the notebook in Colab
2. Select GPU runtime (Runtime -> Change runtime type -> GPU)
3. Follow the notebook instructions

For Local Setup:

1. Create a virtual environment

```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

2. Install requirements

```bash
pip install -r requirements.txt
```

## Project Workflow

1. Dataset Preparation
2. Model Fine-tuning
3. Inference
4. (Optional) Modal.com Integration

## Important Notes

- This project uses SDXL base 1.0 and requires significant computational resources
- Training time: ~2-3 hours on Colab T4 GPU
- Keep your access tokens secure
- For academic/educational purposes only

## Experimental Features

The image refinement feature is currently experimental and under development. While it can improve image quality in some cases, results may vary significantly:

- Use with caution and always keep original images
- Results are highly dependent on prompt crafting
- May require multiple attempts with different parameters
- Best used for subtle enhancements rather than major changes

## Credits and Acknowledgments

This project builds upon:

- Hugging Face Diffusers library
- Stable Diffusion XL by Stability AI
- DreamBooth and LoRA training techniques

Special thanks to Adam Lucek for his comprehensive guide on Stable Diffusion fine-tuning: [Advanced Stable Diffusion LoRA Training Guide](https://docs.google.com/document/d/1KRHOdVA75olgOQNJOSlI29OYkfh-zTTXwaEssPlZ8rA/edit?tab=t.0#heading=h.yi9km4tgu2pk). His guide and accompanying YouTube content provided valuable insights and best practices for this project. For a deeper understanding of the topics covered here, I highly recommend checking out his materials.

## Additional Resources

- [Adam Lucek's Guide](https://docs.google.com/document/d/1KRHOdVA75olgOQNJOSlI29OYkfh-zTTXwaEssPlZ8rA/edit?tab=t.0#heading=h.yi9km4tgu2pk) - Comprehensive guide on LoRA training
- Hugging Face Diffusers Documentation
- Stable Diffusion XL Documentation

For those interested in exploring these concepts further, Adam's guide provides excellent additional context and advanced techniques not covered in this basic implementation.
