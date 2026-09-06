# PlantHealth

PlantHealth is a project that will primarily work on solving a **Plant Health Detection and Classification** problem for agricultural robotics.

## Goal

Build a model that can identify a plant from an image and determine whether it is healthy or affected by a specific disease. The final system should produce a useful health prediction that can be used by the AgroBot simulation platform.

## Starting point

Two papers to read first:

* **Using Deep Learning for Image-Based Plant Disease Detection**, Mohanty, Hughes & Salathé, 2016. [Paper](https://ijmscs.org/index.php/ijmscs/article/view/96/65)
* **Robustness, vulnerability, and deployment readiness of CNNs, vision transformers, and vision–language models for plant disease diagnosis**, 2026. [Paper](https://www.sciencedirect.com/science/article/pii/S2772375526006593)

Not blueprints to copy, its just a starting point for how people have approached plant health detection.

## Model paths

There are several possible directions for solving the problem. Some starting points are:

* **CNN-based classifiers**: ResNet, EfficientNet, or similar models.
* **Vision Transformer models**: ViT or other transformer-based image classifiers.
* **Object detection + classification**: detect the plant/leaf first, then classify its health.
* **Vision-language / foundation models**: explore newer models that can reason about plant health and disease.

You do not need to try all of these. Pick an approach that makes sense for the problem and focus on making it work well.

## Project premise

The main challenge is building a system that can go beyond simply predicting one of 38 dataset classes.

The team can explore two main approaches:

1. **Direct classification:** predict the crop and disease together from the image.
2. **Detection + classification:** first detect the plant/leaf, then use the detected crop to limit the possible disease predictions.

The final system should handle different crops and diseases and be tested on difficult images where lighting, background, plant position, or image quality changes.

## Definition of done

By the end of the core project, the team should be able to show:

* A working plant health model that identifies the crop and its health/disease status.
* A clear evaluation using appropriate classification metrics, including per-class performance.
* Testing on images with conditions that differ from the clean training data, with an analysis of where the model fails.
* A working inference pipeline that can take an image and return a crop + health/disease prediction.
* The trained model successfully onboarded and running in the simulation platform, with a short recorded demo.

## Timeline

* **9 weeks** (you are free to split it up as you wish)

### General example (you are free to modify):

1. **Foundations:** Environment + sim access set up, papers read, dataset explored, and crops/diseases chosen.
2. **Build:** Plant health classification pipeline built and a first working model trained and evaluated.
3. **Improve & apply:** Improve performance, investigate difficult cases, test the model outside the original dataset conditions, and onboard it into the simulation platform.
4. **Wrap-up:** Final testing, error analysis, polish, final report and demo ready.



<!--ALTERNATE (DO NOT MODIFY):
## Timeline

- 7 weeks (core project)
- 9 weeks (extended)
- 12 weeks (advanced)

### 7 weeks — Core project

1. Foundations: Environment + sim access set up, papers read, dataset explored, and crops/diseases chosen.
2. Build: First classification model trained and inference pipeline built.
3. Improve: Model improved, evaluated, and major failure cases investigated.
4. Apply: Model onboarded into the simulation platform and final demo ready.

### 9 weeks — Extended

1. Foundations: Environment + sim access set up, papers read, dataset explored, and crops/diseases chosen.
2. Build: First classification model trained and inference pipeline built.
3. Improve: Tune the model, improve the data pipeline, and investigate failure cases.
4. Robustness: Test the model on more difficult images and investigate how well it handles changes in lighting, background, and image quality.
5. Apply: Improved model onboarded into the simulation platform and final demo ready.

### 12 weeks — Advanced

1. Foundations: Environment + sim access set up, papers read, dataset explored, and crops/diseases chosen.
2. Baseline: Build a strong baseline classifier and establish evaluation metrics.
3. Improve: Tune the model and improve the data pipeline.
4. Robustness: Test difficult and out-of-distribution images and perform detailed error analysis.
5. Advanced direction: Explore one deeper direction such as detection + classification, vision transformers, foundation models, or confidence estimation.
6. Apply: Final approach onboarded and tested in the simulation platform.
7. Wrap-up: Final evaluation, error analysis, report and demo ready.
-->
