---
title: Are LLMs just predicting the next word
date: 2024-12-18 00:00:00
categories: [AI]
post_description: Are LLMs just predicting the next word
---

I will be writing a series discussing aspects of large language models (LLMs) and the intersection with this and other areas such as:
evolutionary biology/neuroscience
sense of self/consciousness
Jailbreaking

This first post will mainly be about a broad overview on LLMs and why they are doing more than ‘just predicting the next word’.

Multiple times I have had conversations with friends and random people on the internet talking about the recent AI advancements and their capabilities. Many times I have heard "they can't actually do X, they are just predicting the next word". This argument is understandable and normally comes from people that have understood partially how a Large Language Model (LLM) works but are missing some subtle points.

First let's start with the transformer architecture and the inner workings of LLMs. There are some great explainer videos that give a better explanation (see [here](https://www.youtube.com/watch?v=LPZh9BOjkQs)) but in a few sentences: A machine learning model is fed billions of words from the internet, it modifies its internal weights to get better at predicting what the next word is. As it trains for longer, and as it gets more data, the model becomes better at predicting the next word. All of this is relatively simple maths which is calculating the difference between the predicted next word and the actual next word and then modifying its weights (internal structure). After the training is done, the model is capable of writing essays, solving complex maths problems, writing code; recent benchmarks even have it in the top 10% of competitive programmers.

After hearing this, it is fair to assume some people will think that these models can’t be intelligent. It can’t be doing anything more than just memorising things and getting the next word. Statistical prediction is not the same as intelligence. However, once we look a bit deeper at this issue we start to see the significance of what is happening under the hood, how is the model getting better at predicting the next word? What information does language provide?

A succinct and simple way to understand why predicting the next word better leads to an intelligent system is from an example given by Ilya Sutskuver who describes a story where a model is passed in a murder mystery where its task is to predict the final word of the story: the revelation of who the murderer is. Throughout the story, characters are developed, the environment is set, subtle clues are littered throughout the book. As the model improves its ability to predict the next word, we can see that it actually needs to have a stronger grasp of complex human emotions, cause and effect, high level abstract concepts like jealousy, game theory, human circumstances etc. This example gives a clue into the direction of what improved prediction does. A better predictor of the next word actually requires a stronger, more coherent, more accurate world model. As more data is fed into the model, and it is trained for longer, the model improves its ‘understanding’ of the world.

An important paper that illustrated glimpses of language models being able to understand abstract concepts was the [Sentiment Neuron Paper](https://openai.com/index/unsupervised-sentiment-neuron/) by OpenAI. In this paper, researchers trained a language model to predict the next word of Amazon reviews. While training this model, they discovered a neuron (an internal part of the model) that correlated strongly with the sentiment (emotional tone) of the review. This neuron appeared on its own, even though the model was never trained to predict the sentiment of the review. This showed early glimpses of language models being able to abstract higher level concepts without being explicitly told to. The explanation for why this sentiment neuron appeared is that, by having an abstract understanding of sentiment, the model is better able to predict what the review will say. Having the abstract representation of sentiment is also an example of compression. The LLMs goal during training is to accurately ‘learn’ from all the data it has been given and so to somehow compress this data within its weights, abstract concepts arise to help this happen.

Recently more work has been done on interpretability and looking deeper inside what the LLM is doing. Anthropic wrote a [paper](https://transformer-circuits.pub/2023/monosemantic-features/index.html) attempting to extract interpretable features that are activated within an even larger model. Within their investigation they were able to extract multiple high level concepts like ‘secrecy’, ‘immunology’ and ‘social/political identities’. This paper shows even more evidence that high level abstractions are represented within the model and that models understand these concepts. Even with models with 100 billion parameters, the model can’t just hard code every single data point and just memorise all the data. It must do some sort of compression through extracting the high level, important features from a novel, an article, a codebase. By abstracting the concept of ‘secrecy’ it is better able to predict and understand how a spy would behave and how to plan a surprise party which in turn would make the model better at predicting the next word.

By noticing that abstract concepts are represented internally within the model, I am trying to make the point that language models are doing more than just predicting. In order to predict the next word, having an understanding of abstract concepts leads to better prediction. But the next question is why. Why are the models learning and representing abstract concepts, why do it in this particular way. It may give too much credit to say that these mathematical language models “learn abstract concepts to better predict the next word” and it might be analogous to saying that “animals evolved to have pretty colors to attract mates”. In the evolution analogy, we are putting too much autonomy into the subject “animals” and anthropomorphising evolution as a force that is consciously acting on animals. Evolution is just the consequence of biological structures randomly mutating and the surviving animals reproducing more. It can almost be described as the consequence of nature.

The same can be said about any machine learning model. There is no ‘learning abstract concepts’ just like animals aren’t actively evolving. In a machine learning model, the loss function of predicting the next word is decreasing and in order to do this, abstractions are represented within the model weights in order to more effectively compress the data. Just like animals don’t evolve to become a better animal, animals just live and die and the curve function of the universe optimises the fittest animal to survive; Machine learning models don’t ‘learn’ they just optimise their compression and encoding of the data they train on, and the curve function of the loss is what they optimise on. The key to this is compression. Compression is intelligence. LLMs train on billions of words and must somehow be able to predict the next word given an input. To do this as effectively as possible, abstract concepts are represented within the model’s weights because instead of having to store the understanding of things like “jim wanting candy” and “brian wanting money”, a higher level concept of “want” and “desire” can represent more general scenarios.

So while it's technically true that LLMs predict the next word, this framing misses the complexity of what that prediction requires. To do this task well, these models develop sophisticated internal representations that capture meaningful aspects of our world and high level abstraction. The question isn't whether they're 'just' predicting words - it's what that prediction tells us about the nature of intelligence and what is required to accurately predict the next word.