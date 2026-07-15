Masked Autoencoder
===================

Teaching a model to rebuild what it cannot see — a masked autoencoder (MAE) for self-supervised visual representation learning.

About
-----

Masked autoencoders learn useful image representations without labels by hiding a large portion of an image's patches and training a model to reconstruct the missing content from what remains visible. The reconstruction task forces the encoder to learn meaningful structure and semantics rather than memorizing pixels, which makes the learned representation useful for downstream tasks after pretraining.

This repository implements the masking and reconstruction pipeline: patch embedding, random masking, an encoder over the visible patches, and a lightweight decoder that reconstructs the full image.

Contents
--------

- `gen-ai-assignment-2.ipynb` — data loading, patch masking, encoder/decoder architecture, training loop, and reconstruction visualization.

Getting started
----------------

Clone the repository or download the notebook.

Install dependencies:

    pip install torch torchvision numpy matplotlib jupyterlab tqdm

Launch Jupyter and open the notebook:

    jupyter lab

Notes
-----

- Hardware: a GPU with CUDA is recommended for training at reasonable batch sizes; encoder/decoder training over image patches is memory-intensive.
- Masking ratio directly affects reconstruction difficulty and representation quality — higher masking ratios force the model to rely more on global structure rather than local pixel copying.

License
-------

MIT License — see `LICENSE`.

Author
------

Ayesha Mudassar — [github.com/AyeshaMudassar20](https://github.com/AyeshaMudassar20)
