---
title: Moderation Demo
emoji: 🛍️
colorFrom: blue
colorTo: purple
sdk: gradio
sdk_version: "5.9.1"
app_file: app.py
pinned: false
---

# Multimodal Listing Consistency Demo

A Gradio/Hugging Face Spaces presentation of an image-and-text classifier for a synthetic product-listing consistency task. Its labels are proxy classes and should not be interpreted as real policy violations.

## What is included

- Gradio image/title interface
- Lazy loading of the text encoder and image/text fusion checkpoint
- Weights-only checkpoint loading and source-level CI

## Run locally

```sh
python -m pip install -r requirements.txt
python app.py
```

## Verify

CI parses the Python source and checks the checkpoint/model architecture with a synthetic forward pass. Full text-encoder download, hosted runtime and complete user flow have not been run.

## Repository map

`app.py` defines the Gradio interface and fusion model. `models/fusion_model_final.pt` is the local checkpoint. Hugging Face deployment metadata is in the repository configuration.

## Evidence and limitations

The checkpoint loads into the expected architecture for a synthetic forward pass. This is not a validation of model semantics or the hosted Space.

This synthetic image/text mismatch task is not a content-moderation policy, safety filter or proof of prohibited content. Confirm data/model licenses, run the full hosted path and define a representative evaluation set before public use.

## License

No repository license file is included. Unless the project owner adds a license, do not assume the code, data or model artifacts may be redistributed or reused. Verify third-party data and model terms separately.
