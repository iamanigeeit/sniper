# SNIPER (Single-Shot Network Initialization Pruning Evolving-Rate) Training

This library is meant to accelerate neural net training by initially starting at a high sparsity so that gradient updates go to important weights, then progressively reducing sparsity to fine-tune the model. The process is explained in this [paper](https://arxiv.org/abs/2211.07283) submitted to ICASSP 2023. It works best for training models which require many epochs on a limited dataset; otherwise the efficiency gains are limited and the dataset has to be sampled when weight importance is computed.

Please refer to the [example notebook](example.ipynb) for usage.
