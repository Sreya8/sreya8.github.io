---
layout: page
title: GAN-Driven Facial Expression Augmentation
description: Animating static facial images using a First Order Motion GAN model for photorealistic facial expression augmentation.
img: assets/img/project_images/GAN-project.png
importance: 2
category: Machine Learning
related_publications: false
# pdf: assets/pdf/infinite_expressions.pdf
---

<div class="mt-4">
    <p>
        <strong>Infinite Expressions</strong> is a GAN-driven framework designed to animate static facial images by transferring dynamic expressions and head movements from high-quality video datasets. Leveraging the First Order Motion Model, the system integrates multiple deep learning components—keypoint detector, dense motion network, and occlusion aware generator to produce photorealistic animated outputs. This self supervised approach eliminates the need for heavily annotated datasets and generalizes across diverse objects.
    </p>

    <h4>Approach:</h4>
    <ul>
        <li>Keypoint detector maps facial features across frames.</li>
        <li>Dense motion network predicts dense motion fields to align source and driving poses.</li>
        <li>Occlusion-aware generator warps source images and inpaints occluded regions for realistic animation.</li>
        <li>Trained on the <a href="https://www.robots.ox.ac.uk/~vgg/data/voxceleb/">VoxCeleb</a> dataset using a self-supervised learning strategy.</li>
    </ul>

    <h4>Results:</h4>
    <ul>
        <li>Produces lifelike facial animations from static images.</li>
        <li>Perceptually realistic outputs validated through visual inspection and loss metrics (perceptual, equivariance, discriminator, and generator losses).</li>
        <li>Demonstrates robustness across unseen subjects and significant pose changes.</li>
    </ul>

    <h4>Impact:</h4>
    <p>
        This framework has potential applications in entertainment, education, and historical preservation, enabling animated storytelling, immersive learning, and dynamic reconstructions of historical figures.
    </p>

    <p>
        Download the full report: <a href="/assets/pdf/infinite_expressions.pdf" target="_blank">Infinite Expressions : GAN-Driven Facial Expression Augmentation (PDF)</a>
    </p>
</div>