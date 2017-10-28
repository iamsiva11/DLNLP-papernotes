
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


## Further research directions 

