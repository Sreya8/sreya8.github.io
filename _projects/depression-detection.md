---
layout: page
title: Depression Detection with Audio-Text Transformers
description: Multi-modal transformer approach for detecting depression from audio and text.
img: assets/img/project_images/depression-cover.jpg
importance: 1
category: Machine Learning
related_publications: false
# pdf: assets/pdf/depression_detection.pdf
---

<div class="text-center mt-4">
    {% include figure.liquid path="assets/img/project_images/project-transformer-1.png" title="Audio-Textual Depression Detection with Multi-Modal Transformer" class="img-fluid rounded z-depth-1" %}
</div>

<div class="mt-4">
    <p>
        This project presents a multi-modal transformer-based model for automatic depression detection using audio and text from clinical interviews. 
        The model leverages self-attention mechanisms to capture cross-modal interactions, improving both diagnostic accuracy and interpretability. 
        By analyzing attention weights, we identify the most influential audio and text features driving predictions, providing insight into key factors contributing to depression.
    </p>

    <h4>Key Results:</h4>
    <ul>
        <li>F1 score on EATD dataset: 0.82</li>
        <li>Accuracy on DAIC-WOZ dataset: 75.8%</li>
        <li>Outperforms baseline LSTM and Bi-LSTM models</li>
        <li>Attention visualizations highlight critical linguistic and emotional cues</li>
    </ul>

    <p>
    Download the full report: <a href="/assets/pdf/depression_detection.pdf" target="_blank">Depression Detection Report (PDF)</a>
    </p>

</div>
