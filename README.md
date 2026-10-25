---
title: Listing Consistency Model Demo
emoji: ðŸ›ï¸
colorFrom: blue
colorTo: purple
sdk: gradio
sdk_version: "5.9.1"
app_file: app.py
pinned: false
---

# Multimodal Listing Consistency Model

This Hugging Face Space serves the image-and-text fusion model developed from Rakuten France catalog examples. A user supplies a product image and listing text; the model returns the experiment's consistency class. Training mismatches were constructed by swapping catalog images between listings.

`app.py` defines the Gradio interface, DistilBERT multilingual-cased text encoder, ResNet18 image backbone, and fusion classifier. `fusion_model_final.pt` in the repository root is the trained checkpoint loaded by the app. Hugging Face metadata and dependencies are maintained at this repository root so the Space can build directly from it.

## Run locally

```sh
python -m pip install -r requirements.txt
python app.py
```
