# Effective Approaches to Attention-based Neural Machine Translation.

[Effective Approaches to Attention-based Neural Machine Translation](https://arxiv.org/abs/1508.04025) (Aug 2015)

* This  paper  examines two simple and effective classes of attentional  mechanism

* A global approach which always attends to all source words and a local one that only looks at a subset of source words at a time. 

* Global -  resembles the model of (Bahdanau et al., 2015) but is simpler architecturally.

* Local - can be viewd as an interesting blend between the hard and soft attention models proposed  in  (Xu et al., 2015):  it  is  computationally  less  expensive  than  the  global  model  or  the soft attention; at the same time, unlike the hard attention, the local attention is differentiable almost everywhere,  making  it  easier  to  implement  and train.

* Comparison to (Bahdanau) - The main difference is how to score similarities between current decoder input and encoder outputs.
Bahdanau <> Luong
Additive <> Multiplicative 
Local attention <> global attention

* Because of the simpler and more data flow, global attention may be a good candidate for implementing in declarative deep learning libraries such as TensorFlow, Theano, and wrappers like Keras.


### Highlights
---

* Global Attention

* aka Luong attention 

* It is interesting to observe that dot works well for the global attention.

* Provided a simpler and faster variant of the attention mechanism that doesn't attend over the hidden states of the encoder at each time step in the deocder. 

* Instead, it computes the a single batched dot product between all the hidden states of the decoder and encoder once after the decoder has processed all inputs in the target. This however comes at a minor cost in model performance. One advantage of this model is that it is possible to use the cuDNN LSTM in the attention based decoder as well since the attention is computed after running through all the inputs in the decoder.

* Examine  different Choices of Attentional Architectures attention (global, local-m,  local-p)  and  different  alignment  functions (location, dot, general, concat ) 

Evaluate the alignment quality using the alignment error rate (AER) metric simiair to how attention was visuallised in (Bahdanau et al., 2015)

### Other existing Notes of this paper
---

https://github.com/dennybritz/deeplearning-papernotes/blob/master/notes/effective-approaches-nmt-attention.md

