---
title: "
dfsfsdfgvdgfdvfdvfdvdv"
collection: talks
type: "Machine Learning and ComputerVision"
permalink: /talks/2014-03-01-talk-3
venue: "Final Year Research Project"
date: 2024-03-01 
location: "University Of Moratuwa"
---

In this project, we developed an encoder model capable of extracting context, flow, and depth features from monocular videos. The uniqueness of this model lies in its ability to extract all three features using a single encoder, making it similar to human vision. The encoder is a CNN-based model called ConvNext, which is an improvement over the ResNet architecture, influenced by transformer architectures.

To provide the model with context understanding, we used the VICReg method. This involves minimizing the distance between embeddings from two augmented images, maintaining variance across a batch of embeddings, and removing relationships across embedding dimensions. The model is hierarchical, meaning that intermediate-level features are also extracted and used for reconstruction.

For flow and depth learning, we employed a more complex architecture. By using three frames to calculate the cost volume, we aimed to reconstruct the flow. Additionally, using left and right views of the images, we attempted to reconstruct the left view from the right using projection and smoothness errors. A transformer-based method was used to capture the connections along the temporal axis. These operations were performed at each hierarchical level, and connections between the hierarchies were established using an LSTM-based method. Finally, after aggregating all this information, a split decoder architecture was used to output both flow and depth.
