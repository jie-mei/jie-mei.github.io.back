---
layout: post
title: Introduction to NLI
date: 2018-06-22
categories: update
---
The natural language inference task is to find a logic relationship between two sentences.
More specifically, given two sentences, one is called a _premise_ and the other one is call a _hypothesis_,
we need to judge whethe they have the same, conflict, or non-related meanings.
Formally, we call these three types of relationships as _entailment_, _neutral_, and _contradiction_.

> __premise__: A gray dog with blue eyes laying on a bright blue carpet while chewing on something.
> __hypothesis__: A gray dog is running down the street.  
> __relation__: neutral

In some cases, however, the meaning of the sentences can be convoluted and thus hard to predict their relations.

> __premise__: If you need this book, it is probably too late unless you are about to take an SAT or GRE.
  (Taking a test makes it not late)  
> __hypothesis__: It's never too late, unless you're about to take a test.
  (Taking a test makes it too late)  
> __relation__: contradiction

The difficulty of the above example are three folds:

1. hard to identify the connection between test and the book, 
2. hard to know that the book in the premise is not important when comparing with the hypothesis,
3. has limited information to infer SAT or GRE is a test.

This type of hard cases, appears quite often in the benchmark dataset.
Since this task is hard, the competitive metheds are all based on neural networks.
There is a tendency to use deeper and more complex network structures in the recent publications and preprints.
