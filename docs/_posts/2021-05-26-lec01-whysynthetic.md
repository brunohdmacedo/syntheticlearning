---
title: Why does synthetic data matter?
categories: ["machine learning", "computer graphics", "computer vision", "synthetic data", "IMPA"]
date: 2021-05-26 17:00:15 +0200
background: /assets/triangle-blue.png
description: In this seminar, we will present some problems that motivate the use of synthetic data and discuss technical issues for training machine learning models based on recent work in the field.
permalink: /why-synthetic-data
---

## [Please, check the slides here.](/syntheticlearning/presentation1.html)

### How do machines learn?

*This is a question that may not have a simple answer. However, without getting into philosophical questions, we can analyze some cases. *

The most common way to train machine learning models today is *supervised learning*. In this approach, we use labeled data to learn a model, a function that respects certain assumptions. We know the input values (data) and output values (labels) of this function and we can use it to adjust the parameters of our model, precisely because we know when it is getting it right and when it is wrong. This scenario leads us to one of the first difficulties in building datasets:

> "How to get the right data labels?"

Thinking about a classic example in computer vision, if we wanted to build a model that classifies chairs and sofas, how would we get images whose content we know to be chairs or sofas? In order to label the data, we need a human to evaluate each example and annotate the content according to the goal we want to achieve. This human component in such a repetitive process increases the cost of data acquisition and the likelihood of introducing errors into the process. This is an example of a situation that motivates the use of synthetic data, as having control of the data generation, we get the labels for each example automatically.

Before adopting this paradigm, however, some questions need to be answered, for instance: do the images need to be photorealistic? Do we still need real data for training? How can we increase the chances of a model trained on synthetic data to work well on real data? In this seminar, we will motivate the use of synthetic data and we will discuss technical issues for training machine learning models using this approach. With this introduction, we aim to understand the prerequisites for a good use of synthetic data and the generalization of trained models.

###### Video is recorded in Portuguese

<iframe width="560" height="315" src="https://www.youtube.com/embed/ttJaaAWwL0g" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>