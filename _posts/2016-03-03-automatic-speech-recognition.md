---
layout: post
title: Speech Recogntion
description:
modified: 2016-03-03
category: Automatic Speech Recognition
tags: atomicity integrity redundancy inconsistency ATM data isolation
imagefeature: cover3.jpg
comments: true
share: true
---
# Automatic Speech Recognition
When you start with this be ready for a big challenge it includes most areas of mathematics, machine learning, 
signal processing, lingustics of which you need not only have to have a an overview but a detailed idea how each 
area related to speech works with speech recognition.


Now since we are learning speech recognition we need to know what is **kaldii** speech recognition Toolkit,
Asterisk , AGI. I will cover introduction for each in next few articles.


First lets Know what is actually meant by speech recognition. It is perfectly defined at wikipedia as
“Speech recognition (SR) is the inter-disciplinary sub-field of computational linguistics which incorporates
knowledge and research in the linguistics, computer science, and electrical engineering fields to develop 
methodologies and technologies that enables the recognition and translation of spoken language into text 
by computers and computerized devices.”


Speech recognition may be speaker dependent or speaker independent.
A system trained only with the voice of one speaker works on the voice of that
speaker is known as speaker dependant because it will not work on any other persons voice. 
Such kind of system may be used for authentication purposes.


While speaker independent system is trained on voices of different people and can work on the voices of different people.
Now lets know what all are the components of Automatic Speech Recognition system:


- Signal processing and feature extraction
- Acoustic model (AM)
- Language model (LM)
- Hypothesis search


The **signal processing and feature extraction** component takes as input the audio signal,
enhances the speech by removing noises and channel distortions, converts the signal from time-domain to frequency-domain,
and extracts salient feature vectors that are suitable for the following acoustic models.


The **acoustic model** integrates knowledge about acoustics and phonetics, takes as input the 
features generated from the feature extraction component, and generates an AM score for the variable-length feature 
sequence.


The **language model** estimates the probability of a hypothesized word sequence, or LM score,
by learning the correlation between words from a (typically text) training corpora. The LM score often can be estimated
more accurately if the prior knowledge about the domain or task is known.


The **hypothesis search** component combines AM and LM scores given the feature vector sequence and the hypothesized 
word sequence, and outputs the word sequence with the highest score as the recognition result. 


In the following articles I will help you how to work practically on ASR and will teach you how to make a simplest
system of speech recognition. 


In the next article I will continue with the giving introduction on Kaldi Speech Recognition toolkit and provide you with 
steps on kaldi.

