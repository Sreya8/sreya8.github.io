---
layout: page
title: Sentiment Analysis with DistilBERT
description: Finetuning DistilBERT for sentiment classification using PyTorch and Hugging Face Transformers with custom training pipelines.
img: assets/img/project_images/sentiment-analysis.jpg
importance: 4
category: machine learning
related_publications: false
# pdf: assets/pdf/sentiment_analysis.pdf
---

<div class="mt-4">
    <p>
        This project focuses on fine-tuning DistilBERT for sentiment analysis on movie review datasets, including IMDb and SST-2. The goal was to build a robust end-to-end pipeline for text classification using state-of-the-art transformer models while leveraging PyTorch and Hugging Face Transformers.
    </p>

    <h4>Tools & Frameworks:</h4>
    <ul>
        <li>Python, PyTorch for model building and training</li>
        <li>Hugging Face Transformers for pre-trained DistilBERT</li>
        <li>Scikit-Learn for dataset handling and evaluation</li>
        <li>TQDM for progress visualization during training</li>
        <li>CUDA for GPU-accelerated training</li>
    </ul>

    <h4>Approach:</h4>
    <ul>
        <li>Implemented a custom PyTorch classification model using DistilBERT as the base, adding a dropout layer and a linear classifier head with softmax output.</li>
        <li>Extracted the [CLS] token representation from the last hidden state for classification.</li>
        <li>Built custom Dataset and DataLoader pipelines for tokenization, batching, and efficient data feeding.</li>
        <li>Trained the model using AdamW optimizer and cross-entropy loss with careful checkpointing based on validation loss to ensure reproducibility.</li>
        <li>Set deterministic seeds and device configuration to ensure consistent results across runs.</li>
        <li>Monitored training and validation loss across multiple epochs, implementing early saving of the best model checkpoint.</li>
    </ul>

    <h4>Results:</h4>
    <ul>
        <li>Achieved strong sentiment classification performance on IMDb and SST-2 benchmark datasets.</li>
        <li>Validated model outputs to ensure correctness and reproducibility, with rounded predictions for consistency.</li>
        <li>Demonstrated effective integration of pre-trained transformer models with custom PyTorch pipelines.</li>
    </ul>

    <h4>Impact:</h4>
    <p>
        This project illustrates best practices for fine-tuning transformer-based models for NLP tasks, including dataset preparation, model architecture design, training strategies, and evaluation. It serves as a foundation for building more advanced sentiment analysis systems or other text classification applications in real-world settings.
    </p>

    <!-- <p>
        GitHub Link to the code: <a href="https://github.com/Sreya8/Sentiment-Analysis-DistilBERT" target="_blank">Sentiment Analysis with DistilBERT</a>
    </p> -->
</div>
