---
title: The Superalignment Problem
author: Dennis G. Wilson
date: '2024-05-22'
tags:
  LLM
  generative ai
  alignment
  newsletter
---

(This post was also published on [Good Computer](https://goodcomputer.substack.com/p/the-superalignment-problem).)

### And the problem with the superalignment problem

Last week, there were a number of doomsday headlines around [the departure](https://www.businessinsider.com/jan-leike-ilya-sutskever-resignations-superalignment-openai-superintelligence-safe-humanity-2024-5) of some high-level members of OpenAI who worked on "[superalignment](https://openai.com/index/introducing-superalignment/)." Aligning AI with human values has long been a important part of AI research, often termed ethical AI or simply useful AI. With the rise of large language models (LLMs), the concept of alignment has gained significant attention. In this post, I'll explore the definition of alignment, the current methods used in LLMs, and challenge the scope of the "superalignment" problem.

**Understanding Alignment**

Alignment, in its simplest form, refers to tuning AI model responses to ensure they produce the "correct" answers by aligning their outputs with labeled data. This term is often used in the context of LLMs, where there isn't always a single correct answer. Instead, what is considered correct can be subjective. Thus, alignment encompasses human values, goals, and ethics in generated text, aiming to produce responses that are considered correct by human standards.

For example, there is no single correct answer to "the best movie is," but a human-aligned model might generate, "The best movie is The Godfather, based on popular opinion and critical acclaim," or "The best movie is Citizen Kane, which is often cited as a groundbreaking achievement in filmmaking." These are better responses than "the best movie is [Spider-Man: Turn Off the Dark](https://en.wikipedia.org/wiki/Spider-Man:_Turn_Off_the_Dark)," firstly because that's not a movie, and secondly because it was a critical and commercial failure. A well-aligned model should tend to generate the former responses more often than the latter.

**Reinforcement Learning from Human Feedback (RLHF)**

To orient LLMs towards human preferences and values, the current method of choice is [Reinforcement Learning from Human Feedback](https://en.wikipedia.org/wiki/Reinforcement_learning_from_human_feedback) (RLHF). Briefly, RLHF involves creating models that score human preference and use these scores to guide text generation. This requires a pretrained LLM, trained on a text-generation task like [next-token prediction](https://goodcomputer.substack.com/p/an-introduction-to-large-language), and a dataset of human preferences.

Imagine you have two sentences of generated text, say the above sentences about movies. If enough humans rate the Godfather sentence as better than the Spider-Man one, that can provide a clear signal to a model that the first sentence is better. You train a model on the human preference dataset, and then use that preference model to score generated text, optimizing the pretrained LLM to generate text that scores highly on the human preference model.

This requires a huge dataset of human-annotated text, and it is unclear where most LLMs like ChatGPT or Gemini get their RLHF data from. You may have participated in this data if you've selected one text completion over another in a model like ChatGPT or character.ai. The idea has been proposed to [use AI](https://arxiv.org/pdf/2309.00267) to generate this preference, but that has [mixed results](https://arxiv.org/pdf/2402.12366) and can perpetuate a vicious cycle of bad alignment.

**Challenges of Alignment**

The challenge of constructing a human preference model is that it is inherently subjective and context-dependent; what is considered "good" text can vary widely between individuals and cultures. Even Yann LeCun, Meta's Chief AI Scientist, [stated](https://x.com/ylecun/status/1628898906611367936) that "RLHF is hopeless because the space of wrong answers is very large, and the space of tricky questions has a very long tail." Gathering data on what is the "correct" best movie to predict might be "tricky," but more serious matters like the "correct" stance on the Israel-Hamas war are fraught with complexity and nuance. Is this the use case we want to put LLMs to?

**The Superalignment Problem**

"Superalignment" was [recently proposed by OpenAI](https://openai.com/index/introducing-superalignment/) with the goal of ensuring that superintelligent AIs act consistently with human values across all possible scenarios. This was posed as a new technical challenge, given that "humans won't be able to reliably supervise AI systems much smarter than us" ([OpenAI](https://openai.com/index/introducing-superalignment/)). The [idea](https://arxiv.org/abs/2312.09390) of the OpenAI team that just left was to create an alignment model to supervise the learning of a superintelligent AI. Other research [suggests](https://arxiv.org/abs/2403.14683) that LLMs may not be able to adapt to the dynamic nature of human ethics and global scenarios, and that substantial changes in LLM architectures are needed to achieve superalignment.

[![OpenAI's "Weak-to-Strong" alignment](https://github.com/openai/weak-to-strong/raw/main/weak-to-strong-setup.png)](https://github.com/openai/weak-to-strong)

The issue with the "superalignment" problem, in my opinion, is that it is ill-posed. Superalignment assumes that there will be a singular, superintelligent AI that can be aligned with human values across all possible scenarios. This is a tall order for multiple reasons. First, human values and goals are complex, diverse, and change over time. Second, the space of possible scenarios is vast and unpredictable, and current machine learning methods, which tend to work best on their training set and not [outside of it](https://arxiv.org/pdf/2402.08955), may not be able to generalize to new scenarios. Third, the idea of a singular superintelligent AI is still largely theoretical and goes against the [long-standing trend of AI research](https://ai100.stanford.edu/) towards more specialized, domain-specific models.

**Domain-Specific Alignment**

Domain-specific AI has long sought to align AI with human values in specific contexts. A widely studied example is the alignment of driverless cars with safety considerations. The [Moral Machine](https://www.moralmachine.net/) experiment, which crowdsourced human judgment on ethical dilemmas faced by autonomous vehicles, highlights the challenge of encoding diverse human preferences. Given moral dilemmas where not everyone in an accident can be saved, participants were asked to choose between sacrificing passengers or pedestrians, often choosing to save children and pregnant women over others. Whether or not driverless cars can [function well enough](https://www.bloomberg.com/news/features/2022-10-06/even-after-100-billion-self-driving-cars-are-going-nowhere) to take these preferences into consideration, the "alignment" of driverless cars is a narrow enough scope for reasonable study. Despite the inherent challenges of modeling diverse human values, the narrow focus on driverless cars' alignment makes the task more feasible.

As AI continues to be applied in various fields, ensuring that AI is beneficial for humanity will require alignment in those specific contexts. Social media recommendation algorithms should be aligned to prioritize users' mental health, autonomous vehicles should be aligned to prioritize safety, and medical diagnostic AI should be aligned to prioritize patient well-being. While progress in LLMs and chatbot alignment is impressive, focusing on aligning AI with human values in specific applications will allow for the use of domain-specific knowledge and [regulation](https://goodcomputer.substack.com/p/european-union-ai-act) to ensure that AI technologies serve human interests effectively.

**TL;DR**

The "superalignment" problem is unreasonable given the complexity of human values, the vast space of possible scenarios, and the framing around a singular superintelligent AI. Instead, aligning specific AI with human values in application domains, such as driverless cars or social media recommendation algorithms, is a more feasible and effective approach to ensuring that AI technologies serve human interests.
