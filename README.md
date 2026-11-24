# Impactframe — Qwen Image Edit 2512 LoRA

A specialized LoRA trained on **Qwen Image Edit 2512** that gives the model true conceptual and visual knowledge of **anime/manga impact frames** while preserving full logical instruction-following and reasoning capabilities.

## Why This LoRA Exists
Out of the box, base **Qwen Image Edit 2512/2511** and other open-source reasoning/editing models lack direct knowledge of what an impact frame actually is—resulting in generic contrast filters or broken compositions when prompted for impact frames.

Meanwhile, existing impact frame LoRAs on older checkpoints are purely rigid, keyword-triggered style models with **zero logical reasoning or instruction-following support**. Because this LoRA is trained directly on **Qwen Image Edit 2512** with full natural-language captioning, you can logically direct *where* the impact lands, *how* the lighting reacts, and *what* happens in the scene instead of relying on blind tag-spamming.

## Download
Download `ImpactFrame-Qwen-ImageEdit.safetensors` from the page and place it in your `models/loras/` folder (e.g., `ComfyUI/models/loras/`).

## Model & Inference Specifications
- **Base Model:** Qwen Image Edit 2512/2511
- **File Format:** `.safetensors`
- **Primary Trigger Word:** `Impactframe`
- **Recommended LoRA Strength:** `0.7`
- **Supported Visual Concepts & Keywords:** `blast`, `shine`, `silhouette`, `shockwave`, `energy burst`, `radial impact lines`, `high-contrast flash`
- **Supported Modes:**
  - **Image-to-Image (I2I) / Image Editing:** Primary target workflow; extensively tested for converting existing action frames into impact frames while respecting scene structure.
  - **Text-to-Image (T2I):** Fully supported for generating impact frame compositions from scratch.

## Training Data & Methodology

- **Base Architecture:** Qwen Image Edit 2512

- **Dataset Size:** 150 curated impact frame images

- **Captioning Strategy:** 150 natural-language captions (1:1 image-to-caption pairing)