
# Sequence to Sequence Learning with Neural Networks (NIPS, Sep 2014)

[Sequence to Sequence Learning with Neural Networks](https://arxiv.org/abs/1409.3215)


# TLDR - Quick summary
---

Sequences pose a challenge for DNNs because they require that the dimensionality of the inputs and outputs is known and fixed. The RNN can easily map sequences to sequences whenever the alignment between the inputs the outputs is known ahead of time. However, it is not clear how to apply an RNN to problems whose input and the output sequences have different lengths with complicated and non-monotonic relationships. To fix this, a multilayered Long Short-Term Memory (LSTM) is used to map the input sequence to a vector of a fixed dimensionality, and then another deep LSTM to decode the target sequence from the vector.


# Key Points
---

* Pioneering research work in Deep learning based sequence modelling. Although DNNs work well whenever large labeled training sets are available, they cannot be used to map sequences to sequences.

* The authors show that a multilayer LSTM RNN (4 layers, 1000 cells per layer, 1000d embeddings, 160k source vocab, 80k target vocab) can achieve competitive results on Machine Translation tasks.

* The authors find that reversing the input sequence leads to significant improvements, most likely due to the introduction of short-term dependencies that are more easily captured by the gradients. 

* LSTM did not have difficulty on long sentences, which was a surprise.

* The model is evaluated on MT tasks and achieves competitive results (34.8 BLEU) by itself, and close to state of the art if coupled with existing baseline systems (36.5 BLEU).

* The LSTM also learned sensible phrase and sentence representations that are sensitive to word order and are relatively invariant to the active and the passive voice.

* Reversing the words in the source sentence lead to significant improvement - key technical contributions of this work(only source sentence but not the target sentences)

* Deep LSTMs significantly outperformed shallow LSTMs

* When the sequence of words are turned into a vector of fixed dimensionality; the representations are sensitive to the order of words, while being fairly insensitive to the replacement of an active voice with a passive voice.


## Questions
---

* The authors we do not have a complete explanation to why inverting the input actually works.


## Illustration
---

![Arch image in the paper](https://adriancolyer.files.wordpress.com/2016/05/seq2seq-fig-1.png)

So for example, instead of mapping the sentence a, b, c to the sentence α, β, γ, the LSTM is asked to map c, b, a to α, β, γ, where α, β, γ is the translation of a, b, c . This way, a is in close proximity to α,b is fairly close to β , and so on, a fact that makes it easy for SGD to “establish communication” between the input and the output. We found this simple data transformation to greatly boost the performance of the LSTM



### Other existing Paper Notes of this paper
---

https://blog.acolyer.org/2016/06/02/sequence-to-sequence-learning-with-neural-networks/

https://www.commonlounge.com/discussion/37abd2ad4e7849a39b66ef750f95ec0d

https://gist.github.com/shagunsodhani/a2915921d7d0ac5cfd0e379025acfb9f

https://github.com/dennybritz/deeplearning-papernotes/blob/master/notes/seq2seq-with-neural-networks.md

