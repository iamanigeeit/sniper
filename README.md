# SNIPER (Single-Shot Network Initialization Pruning Evolving-Rate) Training

This library is meant to accelerate neural net training by initially starting at a high sparsity so that gradient updates go to important weights, then progressively reducing sparsity to fine-tune the model. The process is explained in this [paper](https://arxiv.org/abs/2211.07283) submitted to ICASSP 2023. It works best for training models which require many (>20) epochs on a limited dataset, since we make one pass through the data in the beginning to assess weight importance.

Please refer to the [example notebook](example.ipynb) for usage on image classification. We can train 2x faster than the dense model and yet achieve better eventual performance (left -- accuracy, right -- loss):

<img src="final_graph.png">
