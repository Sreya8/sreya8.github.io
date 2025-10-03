---
layout: page
title: Depression Detection with Audio-Text Transformers
description: Multi-modal transformer approach for detecting depression from audio and text.
img: assets/img/project_images/depression-cover.jpg
importance: 1
category: machine learning
related_publications: false
# pdf: assets/pdf/depression_detection.pdf
---

Download the complete report: <a href="/assets/pdf/depression_detection.pdf" target="_blank">Depression Detection Report (PDF)</a>.
Link to the code: <a href="https://github.com/Sreya8/Audio-Textual-Depression-Detection-with-Multi-modal-Transformer" target="_blank">GitHub</a>.

<div class="text-center mt-4">
    {% include figure.liquid path="assets/img/project_images/project-transformer-1.png" title="Workflow: Audio-Textual Depression Detection" class="img-fluid rounded z-depth-1" width="80%" %}
</div>

This project explores automatic depression detection using both audio recordings and text transcripts from clinical interviews (EATD-Corpus). 
We investigate multi-modal and single-modal models, leveraging transformer architectures and feedforward networks to extract meaningful features from speech and language.

### Dataset and Preprocessing

- <strong>EATD-Corpus</strong>: Audio recordings and transcript files from clinical interviews.
- <strong>Audio preprocessing</strong>: WAV files converted to Mel-spectrograms and pooled with a custom NetVLAD layer to produce fixed-size embeddings.
- <strong>Text preprocessing</strong>: Transcripts tokenized and embedded using <code>bert-base-uncased</code>. Sequences truncated/padded to 40 tokens.
- <strong>Data augmentation</strong>: Permutations of positive samples to increase training diversity.

### Models

- **Feedforward Multimodal Classifier**: Combines mean-pooled text embeddings and audio embeddings through fully connected layers.
- **Transformer Multimodal Classifier**: Separate transformer encoders for text and audio, outputs combined and classified.
- **Single-Modal Transformers**: Text-only and Audio-only transformers for ablation studies and interpretability.

### Tools and Frameworks

- **Audio Processing**: librosa, numpy, wave
- **Text Processing**: transformers (BERT)
- **Deep Learning**: PyTorch (all classifier models), TensorFlow/Keras (NetVLAD audio embeddings)
- **Evaluation Metrics**: Accuracy, Precision, Recall, F1 Score (sklearn)
- **Visualization**: matplotlib, seaborn (attention heatmaps)

### Training Setup

- 3-fold cross-validation
- Optimizers: Adam
- Learning rates: Feedforward = 1e-4, Transformer = 4e-5
- Loss: Binary Cross-Entropy with Logits
- Batch size: 32, Epochs: Feedforward 200, Transformer 250

### Key Results

| Model | Accuracy | Precision | Recall | F1 Score |
|-------|----------|-----------|--------|----------|
| Feedforward Multimodal | 85.3% | 0.82 | 0.96 | 0.88 |
| Transformer Multimodal | 79.8% | 0.77 | 0.92 | 0.84 |
| Text-Only Transformer | 93.6% | 0.90 | 1.00 | 0.94 |
| Audio-Only Transformer | 71.8% | 0.72 | 0.84 | 0.77 |

<br>

### Key Takeaways

- BERT embeddings capture crucial linguistic cues for depression prediction.
- NetVLAD audio embeddings encode prosodic and emotional signals from speech.
- Transformer models allow attention-based interpretability of key tokens.
- Text information dominates prediction performance, though multimodal models provide complementary insights.
- Permutation-based data augmentation improves positive sample representation.

### Applications

- Automated clinical depression screening tools
- Research in multimodal affective computing
- Understanding cross-modal linguistic and emotional cues in mental health


