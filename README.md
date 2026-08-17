# Shiva27653-Proposed-SAR-Optical-Cloud-Removal-Model

# Proposed SAR–Optical Cloud Removal Model

## Overview

This repository contains an experimental SAR–optical cloud-removal
model for reconstructing cloud-reduced optical satellite imagery
using complementary SAR and optical observations.

The model takes cloudy optical imagery together with SAR information
and produces a reconstructed cloud-reduced optical image.

## Dataset

The model was developed and evaluated using the SEN12MS-CR dataset,
which provides paired:

- Sentinel-1 SAR imagery
- Cloudy Sentinel-2 optical imagery
- Cloud-free Sentinel-2 reference imagery

The dataset itself is not included in this repository.

## Demonstration

The following results were generated from a real sample from the
SEN12MS-CR dataset.

### Cloudy Input

![Cloudy Input](demo/cloudy.png)

### Model Prediction

![Model Prediction](demo/prediction.png)

### Cloud-Free Reference

![Ground Truth](demo/ground_truth.png)

The prediction demonstrates the model's ability to reconstruct a
cloud-reduced optical image from the available SAR and cloudy
optical observations.

## Checkpoint

The trained model checkpoint is provided as:

`best.pt`

The checkpoint is stored using Git LFS because of its size.

## Environment

The model was developed using:

- Python 3.12+
- PyTorch 2.6+
- CUDA-enabled GPU recommended

## Inference

The included demonstration script contains the inference procedure
used to load the trained checkpoint and generate the example result.

## Notes

This repository contains an experimental research implementation
and a qualitative demonstration. The included images are provided
as an example of the model output and are not presented as a
quantitative benchmark.

## Dataset Reference

SEN12MS-CR:

https://patricktum.github.io/cloud_removal/
