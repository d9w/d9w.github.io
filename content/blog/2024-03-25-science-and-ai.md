---
title: Will AI destroy science or solve it?
author: Dennis G. Wilson
date: '2024-03-25'
tags:
  - science
  - generative ai
  - language models
  - academia
---

Is AI the new way to do science, or is AI destroying science? This question was shoved into the spotlight again last week after some very ill-advised uses AI-generated content in research papers came to light. In this blog post, I'll take a look at the current state of AI in science, focusing on LLMs in academic publishing, and argue that AI is not going to destroy science, nor is it going to solve it and replace all human researchers.

Last week, the site formerly known as Twitter had some fun pointing out academic articles with AI generated images and text. [Gary Marcus](https://en.wikipedia.org/wiki/Gary_Marcus) wrote [two](https://garymarcus.substack.com/p/the-year-of-the-big-balled-rat) [posts](https://garymarcus.substack.com/p/the-exponential-enshittification) on what he termed the "exponential enshittification" of science due to the use of generative AI in scientific research. One of the more [amusing examples](https://twitter.com/DrCJ_Houldcroft/status/1758111493181108363) is a generated diagram of a rat in a [now-redacted article](https://www.frontiersin.org/articles/10.3389/fcell.2023.1339390/full) in Frontiers in Cell and Developmental Biology. Users pointed out that Google Scholar searches for phrases like "Certainly, here is a list," "my last knowledge update," or "I am a language model" turn up many results of seemingly valid scientific articles.

The problem identified is the use of AI-generated text and images in scientific articles. AI-generated text can contain fabricated or misleading information, which can have serious consequences for scientific progress and public trust in science. AI-generated images are a completely different level of problematic, and it is hard to imagine how they could be useful in a scientific context. Thankfully, however, the use of AI-generated images in scientific articles seems to be less common than the use of AI-generated text, so I will focus on the latter.

I decided to take a look at 100 articles that came up when searching for the example generated AI phrases on Google Scholar; "my last knowledge update" was by far the most common. I collected the articles in a Zotero group, which you can access [here](https://www.zotero.org/groups/5463061/good-computer/collections/USVXT2XU). This is intended as a representative sample, but not an exhaustive list, as I'm sure there are other articles that contained clearly generated text but weren't caught by the above search terms, and I went through enough articles to get [temporarily blocked by Google Scholar](https://support.google.com/chrome/thread/3959611/error-403-when-trying-to-export-citation-from-google-scholar-to-endnote?hl=en). So, 100 articles it is.

Of the 100 articles, 68 of them had some form of journal or publication listed correctly. Some of the other articles, like [this one](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=4745790) didn't have proper Scholar listings, while most of the others were  [preprints](https://easychair.org/publications/preprint_download/Q1nB) or were uploaded on [ResearchGate](https://www.researchgate.net/profile/Ali-Maksuti/publication/376587468_Financial_Integration_of_North_Macedonia_and_Adjustments_of_Financial_Reports_to_the_Value_of_European_Union/links/657ed0a79d7bc03b30826de1/Financial-Integration-of-North-Macedonia-and-Adjustments-of-Financial-Reports-to-the-Value-of-European-Union.pdf). ResearchGate, for those lucky enough to not be familiar, is like the Facebook of academia, but somehow even worse than that sounds.

Only two of the articles were published in journals referenced by the [Directory of Open Access Journals](https://doaj.org/): [the first](https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=10268931) in [IEEE Access](https://ieeeaccess.ieee.org/), and [the second](https://scholar.archive.org/work/hdvweein6bd65fi4t4q2fbmv6q/access/wayback/https://ojs.jass.pk/ojs/index.php/jass/article/download/406/160) in a journal titled ["Journal of Arts & Social Sciences"](https://journals.squ.edu.om/index.php/jass). It is worth noting that I couldn't find any reliable information about the impact factor of JASS and that the article in question can't be downloaded from the journal's website, but only from the [Internet Archive](https://archive.org/). It's safe to say that this journal isn't the height of academic publishing.

Five of the 100 articles were conference papers, specifically from the IEEE conferences [ICSCAN](https://ieeexplore.ieee.org/abstract/document/10395119), [ICDSAAI](https://ieeexplore.ieee.org/abstract/document/10452604), [RMKMATE](https://ieeexplore.ieee.org/abstract/document/10369395), [ICACCTech](https://ieeexplore.ieee.org/abstract/document/10441736), [ICECA](https://ieeexplore.ieee.org/abstract/document/10395164). It is worth noting that none of these conferences are not even indexed in the [CORE database](https://www.core.edu.au/conference-portal), which is used to determine academic conference quality. Hilariously, [one of the articles](https://ieeexplore.ieee.org/abstract/document/10395164) is about AI writing tools and includes the clearly generated phrase "by considering the evolution of these tools beyond my last knowledge update in September 2021, this study equips individuals with insights" and does not acknowledge the use of an AI writing tool, as [required by the IEEE](https://journals.ieeeauthorcenter.ieee.org/become-an-ieee-journal-author/publishing-ethics/guidelines-and-policies/submission-and-peer-review-policies/#ai-generated-text).

So, as a summary, there were two articles in somewhat reputable journals, five in non-ranked conference proceedings, and the rest were either preprints or published in non-referenced journals. This analysis is not intended to minimize the problems of language models in generative AI, however I do think that the claim that this is an AI-driven ["exponential enshittification" of science](https://garymarcus.substack.com/p/the-exponential-enshittification) are a bit overblown. Science has been plagued with [predatory journals](https://scienceouverte.univ-rennes.fr/en/predatory-journals) and conferences for years. Google Scholar is known to be "[filled with junk science](https://web.archive.org/web/20161110004415/https://scholarlyoa.com/2014/11/04/google-scholar-is-filled-with-junk-science/)" and  [bibliometric analyis for academics](https://elsevier.digitalcommonsdata.com/datasets/btchxktzyw/6) often relies on other sources of information like [Scopus](https://www.scopus.com/) or [Web of Science](https://www.webofscience.com/wos/). Generative AI leading to an increase of publications in predatory or low-quality journals is a problem, but the existence of these journals, conferences, and articles is not a new problem, and means to address this problem, while imperfect, are already in place.

Rather, there is an argument that writing assistance from large language models will benefit science. Many papers with interesting results have been rejected due to their presentation, English level, or writing style. AI tools can help researchers with these issues, allowing them to focus on the science itself. Copying and pasting generated text into a paper should be forbidden, but the use of language models to translate, correct, or rephrase text could help progress scientific communication if done properly. [This editor statement](https://link.springer.com/article/10.1007/s11019-023-10176-6) makes some common-sense recommendations:

> LLMs or other generative AI tools should not be listed as authors on papers
> Authors should be transparent about their use of generative AI, and editors should have access to tools and strategies for ensuring authors’ transparency
> Editors and reviewers should not rely solely on generative AI to review submitted papers
> Editors retain final responsibility in selecting reviewers and should exercise active oversight of that task
> Final responsibility for the editing of a paper lies with human authors and editors

The use of LLMs in academic publishing is also only a small part of the image of AI in science. There are many, many ways in which AI can be implicated in science, and it is a subject I plan on returning to in future posts.There's a series of [workshops](https://ai4sciencecommunity.github.io/) on AI for science, a number of [research](https://www.ai4science.caltech.edu/) [groups](https://ai4science-amsterdam.github.io/), and government initiatives from the [EU](https://research-and-innovation.ec.europa.eu/research-area/industrial-research-and-innovation/key-enabling-technologies/artificial-intelligence-ai-science_en) and the [US](https://new.nsf.gov/focus-areas/artificial-intelligence/nairr) which mention or focus on AI in science. The Nature article ["Scientific discovery in the age of artificial intelligence"](https://www.nature.com/articles/s41586-023-06221-2) does a great job of summarizing recent advancements in AI for science.

One argument that has been put forward is that AI is best used as a tool to aid in scientific understanding, rather than as a replacement for human scientists. AI can help scientists analyze large datasets, design experiments, generate new hypotheses, and iterate over scientific literature. [This article](https://www.nature.com/articles/s42254-022-00518-3) argues that AI can be useful as a "computational microscope," allowing for complex simulations and data analysis, as a source of inspiration through analysis of scientific literature, data, or models, and as an "agent of understanding" through explaining concepts to scientists. Similar points were recently argued by [Stephen Wolfram](https://en.wikipedia.org/wiki/Stephen_Wolfram) in his [blog post](https://writings.stephenwolfram.com/2024/03/can-ai-solve-science/) and 2.5 hour long [webinar](https://www.youtube.com/watch?v=goYaSkxG8LA) entitled "Can AI Solve Science?" [^1]. Wolfram points out that AI can help find interesting or surprising subjects of study, assist in the creation of human-accessible narratives for complex scientific phenomena, and identify patterns or relationships within vast amounts of data that might not be immediately apparent to human researchers. However, he also cautions against over-reliance on AI, emphasizing that the ultimate understanding and advancement of science will still depend on human creativity, intuition, and the ability to conceptualize new frameworks and theories.

[^1] The central, and very interesting, argument of Wolfram's post is that the effectiveness of AI in science depends on computational reducibility. Some problems, which are reducible, can be broken down into simpler steps that can be approximated or solved by AI. For problems that are not reducible, such as the three-body problem in physics, the approximations offered by machine learning won't work in certain cases, or will require simulating the full system. By leveraging AI as a tool within the broader context of human-led research, scientists can navigate the vast and often unpredictable terrain of computational irreducibility, uncovering pockets of reducibility that offer new insights and breakthroughs.

AI isn't going to destroy science, nor is it going to solve it and replace all human researchers. As argued above, it can certainly accelerate science, and the question of whether [accelerating science is desirable](https://www.scientificamerican.com/article/the-dangers-of-fast-science/) should be discussed. The temptation to prioritize quantity over quality, to publish first and question later, [must be resisted](https://www.nature.com/articles/520429a), as ensuring the credibility of scientific endeavors in the face of AI's double-edged promise is paramount. Using Midjourney to generate fake rat testes is definitely not the way to build trust in science.
