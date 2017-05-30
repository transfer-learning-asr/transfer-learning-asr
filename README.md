# Transfer Learning for Speech Recognition on a Budget

Source code for 'Transfer Learning for Speech Recognition on a Budget' published at ACL 2017

## Abstract

End-to-end training of Automated Speech Recognition (ASR) systems requires massive data and compute resources.
We explore transfer learning based on model adaptation as an approach for training ASR models under constrained GPU memory,
throughput and training data. 
We conduct several systematic experiments adapting a Wav2Letter convolutional neural network originally trained for English ASR to the German language.
We show that this technique allows faster training on consumer-grade resources while requiring less training data in order to achieve the same accuracy,
thereby lowering the cost of training ASR models in other languages.
Model introspection revealed that small adaptations to the network's weights were sufficient for good performance, especially for inner layers.

## Modules

### Wav2Letter in keras with German corpora

All transfer learning experiments were performed using our Wav2Letter implementation in keras.
It supports both the English [LibriSpeech](http://www.openslr.org/12) corpus as well as several German corpora as described in the paper.

### Decoding using KenLM beam search

While keras and tensorflow do not support CTC decoding using a language model by default,
we developed a beam search decoding procedure based on [KenLM](http://kheafield.com/code/kenlm/).

## Install

```
git clone --recursive https://github.com/transfer-learning-asr/transfer-learning-asr.git
```

Then compile and install tensorflow-with-kenlm and run the wav2letter code.
