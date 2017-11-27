# Neural Machine Translation by Jointly Learning to Align and Translate 
---

[Neural Machine Translation by Jointly Learning to Align and Translate](https://arxiv.org/pdf/1409.0473.pdf) (ICLR, Sep 2014 )


Summary 
---

* The authors claim that fixed-length vector is a bottleneck in improving the performance of this basic encoder–decoder architecture.

* To fix that, soft-search for parts of a source sentence that are relevant to predicting a target word, without having to form these parts as a hard segment explicitly.

* The most important distinguishing feature of this approach from the basic encoder–decoder is that it does not attempt to encode a whole input sentence into a single fixed-length vector. Instead, it encodes the input sentence into a sequence of vectors and chooses a subset of these vectors adaptively while decoding the translation.

* The network encodes the input sentence into a sequence of vectors and chooses a subset of these vectors adaptively while decoding the translation

* The proposed novel architecture(referred as RNNsearch) consists  of  a  bidirectional  RNN  as  an  encoder

* Why bidirectional RNN?  - Firstly, they want the annotation of each word to summarize not only the preceding words, but also the following words. Bidirectional RNN contains the summaries of  both  the  preceding  words  and  the  following  words. Secondly -  bidirectional RNN

* Provide visualisation of the attention and allignment of the source and the target words in a sentence.

* The attention matrix is easily interpretable as well, and visualizations in the paper show that higher weights are being assigned to input words that correspond to output words irrespective of their order in the sequence (unlike an attention model that uses a mixture of Gaussians which is monotonic).

* When referring to alignment; they mean to align each target word with the relevant words, or their annotations, in the source sentence as it generated a correct translation.

* A similar approach of aligning an output symbol with an input symbol was proposed recently by Graves (2013) in in the context of handwriting synthesis.

* Works better with long sentences

* Proposed attention mechanism is a weighted sum of the input hidden states



### Next steps 
---

One of challenges left for the future is to better handle unknown, or rare words.


### Highlights
---

Major breakthrough in seq2seq after the fixed representation of the vector(“compressed” vector) idea

No fixed size representation

introduced attention mechanism

Visualising the attention

Attention is referred to as alignment in this paper. Soft and hard alignment.


### Other existing Notes of this paper
---

https://github.com/abhshkdz/papers/blob/master/reviews/neural-machine-translation-by-jointly-learning-to-align-and-translate.md

https://github.com/dennybritz/deeplearning-papernotes/blob/master/notes/nmt-jointly-learning-to-align-and-translate.md

https://theneuralperspective.com/2016/10/02/neural-machine-translation-by-jointly-learning-to-align-and-translate-attention-in-rnns/

https://www.commonlounge.com/discussion/9c03330f7b50498a9a6a7a5afc4631d4/

https://wiki.math.uwaterloo.ca/statwiki/index.php?title=neural_Machine_Translation:_Jointly_Learning_to_Align_and_Translate

http://www.shortscience.org/paper?bibtexKey=journals/corr/BahdanauCB14#abhshkdz

https://blog.tomrochette.com/machine-learning/papers/dzmitry-bahdanau-neural-machine-translation-by-jointly-learning-to-align-and-translate

http://blog.csdn.net/Eric_KEY/article/details/76283816

https://zhuanlan.zhihu.com/p/21287807 (In chinese, translate to eng )

https://github.com/abhshkdz/papers/blob/master/reviews/neural-machine-translation-by-jointly-learning-to-align-and-translate.md
