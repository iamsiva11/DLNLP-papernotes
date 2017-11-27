# Massive Exploration of Neural Machine Translation Architectures

[Massive Exploration of Neural Machine Translation Architectures](https://arxiv.org/pdf/1703.03906.pdf)

# Summary 

* Major drawback of NMT architectures - lots of training time(typically requiring days to  weeks of GPU time to converge)

* Requires heavy computational resources - exhaustive  hyperparameter search , over 250,000 GPU hours, datasets of several million examples, requires dozens of GPUs.

* Explores experimental architectures by playing with depth, skip connections,  residual connections from other existing architecture.

* With Careful hyperparameter tuning and good initialization, it is possible to achieve state of  the art performance on standard WMT benchmarks. 

* Future research directions  - the efficient use of embedding parameters, the role of attention mechanisms as weighted skip connections as opposed to memory units, the need for better optimization methods for deep recurrent networks, and the need for a better beam search robust to hyperparameter variations.

---

## Practical insights and advice on working with seq2seq 

* Deep  encoders  are  more  difficult to optimize than decoders.

* Dense residual connections yield better performance than regular  residual  connections,  

* LSTMs outperform  GRUs.

* Well-tuned beam  search  is  crucial  to  obtaining  state  of the art results. 

* With a large vocabulary, the embedding layer can account for a large fraction of the model parameters.

* Bidirectional encoders generally outperform unidirectional encoders, but not by  a  large  margin

* The  encoders  with  reversed source consistently outperform their non-reversed counterparts,  but  do  not  beat  shallower  bidirectional encoders.

* Bidirectional encoders with 2 to 4 layers performed best.  Deeper encoders were significantly more unstable to train,  but show potential if they can be optimized well.

* Deep 4-layer decoders slightly outperformed shallower decoders.

* Residual  connections were necessary to train decoders with 8 layers and dense residual connections offer additional robustness.

* Parameterized additive attention yielded the overall best results.

* A  well-tuned   beam   search   with   length penalty  is  crucial.   Beam  widths  of  5  to  10 together with a length penalty of 1.0 seemed
to work well.

* Large embeddings with 2048 dimensions achieved the best results, but only by a small margin. Even small embeddings with 128 dimensions seem to have sufficient capacity to capture most of the necessary semantic information
