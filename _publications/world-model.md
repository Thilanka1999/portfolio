---
title: "World Model - Generalized Human Level Vision Model"
collection: publications
category: manuscripts
permalink: /publication/2009-10-01-paper-title-number-1
excerpt: 'Final Year Research Project Conduct in University Of Moratuwa'
date: 2024-07-01
venue: 'University Of Moratuwa'
slidesurl: ''
paperurl: 'https://github.com/Avishka-Perera/multitask-pipeline'
citation: 'Final Year Research Project, University Of Moratuwa'
---


- Objective: Designed and implemented an image encoder model capable of extracting flow, depth, and content features from monocular videos, showcasing robust generalizability across domains.
- Key Achievements: Trained on outdoor datasets and tested on indoor datasets, the model outperformed baseline metrics from referenced research papers.
- Technical Contributions:

    - Conducted model fine-tuning, hyperparameter optimization, and architecture design, incorporating a hierarchical encoder to enhance feature extraction.
    - Developed pipelines for downstream tasks such as classification and segmentation.
    - Employed transformer-based decoders to capture temporal patterns during training.
    - Utilized advanced visualization tools to analyze model performance and domain shifts.

- Outcome: Delivered a scalable and high-performing model with significant real-world applicability in video analysis tasks.

In this project, we developed an encoder model capable of extracting context, flow, and depth features from monocular videos. The uniqueness of this model lies in its ability to extract all three features using a single encoder, making it similar to human vision. The encoder is a CNN-based model called ConvNext, which is an improvement over the ResNet architecture, influenced by transformer architectures.

To provide the model with context understanding, we used the VICReg method. This involves minimizing the distance between embeddings from two augmented images, maintaining variance across a batch of embeddings, and removing relationships across embedding dimensions. The model is hierarchical, meaning that intermediate-level features are also extracted and used for reconstruction.

For flow and depth learning, we employed a more complex architecture. By using three frames to calculate the cost volume, we aimed to reconstruct the flow. Additionally, using left and right views of the images, we attempted to reconstruct the left view from the right using projection and smoothness errors. A transformer-based method was used to capture the connections along the temporal axis. These operations were performed at each hierarchical level, and connections between the hierarchies were established using an LSTM-based method. Finally, after aggregating all this information, a split decoder architecture was used to output both flow and depth.
