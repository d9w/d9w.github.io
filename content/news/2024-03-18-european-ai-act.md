---
title: The European AI Act
author: Dennis G. Wilson
date: '2024-03-17'
tags:
  - European AI Act
  - generative ai
  - legislation
  - biometrics
  - newsletter
---

(This post was also published on [Good Computer](https://goodcomputer.substack.com/p/european-ai-act).)

> "Thou shalt not make a machine in the likeness of a human mind." - Frank Herbert, Dune

Governing artificial intelligence is a difficult task. Govern too loosely and society may suffer from the negative consequences of a rapidly advancing technology that is poorly understood. Govern too strictly, or prohibit it entirely, as in Frank Herbert's Dune, and society may miss out on the benefits of new technology based on AI.

This week, the European Union took a major step towards sensible governance of AI with the [EU AI Act](https://artificialintelligenceact.eu/). The act is designed to protect the rights of individuals and ensure that AI is used in a way that is safe and respects human rights. In this post, I'll look at the key ideas of this act and argue that it is a good base framework for future legislation.

The AI Act defines AI as follows:

> 'AI system' is a machine-based system designed to operate with varying levels of
> autonomy and that may exhibit adaptiveness after deployment and that, for explicit
> or implicit objectives, infers, from the input it receives, how to generate outputs such
> as predictions, content, recommendations, or decisions that can influence physical or
> virtual environments

Nearly every word in this definition could be the subject of lengthy debate, but I'd like to focus on the broad scope of the definition. The act is designed to be future-proof, and the definition encompasses a wide range of technologies. An [earlier definition](https://eur-lex.europa.eu/legal-content/EN/TXT/?uri=CELEX%3A52021PC0206) relied on an explicit list of techniques from "machine learning approaches" to "Bayesian estimation." We don't know what techniques AI will use in the future, so leaving this open allows for interpretation in the future. The definition may even be too broad, as it could encompass technologies that are not considered AI, such as a database query. However, future litigation will refine this definition, and the base is sufficient to be useful without being overly restrictive.

The act is much more explicit when it comes to applications of AI. The act is risk-based, meaning that the level of regulation will depend on the level of risk associated with the technology. Risk is defined as "the combination of the probability of an occurrence of harm and the severity of that harm," and is broken down into four categories: Unacceptable, High, Low, and Minimal Risk. Unacceptable risk systems are permitted, high risk systems are heavily regulated, low risk systems mostly have transparency requirements, and minimal risk systems are unregulated. 

Examples of prohibited applications of AI, under certain conditions, include
 [social scoring systems](https://www.technologyreview.com/2022/11/22/1063605/china-announced-a-new-social-credit-law-what-does-it-mean/), [assessing an individual's criminal risk](https://www.wired.com/story/doj-predictive-policing-lawmakers-demand/), [facial recognition](https://www.cnil.fr/en/facial-recognition-20-million-euros-penalty-against-clearview-ai), 
[biometric categorization like racial profiling](https://arstechnica.com/information-technology/2016/03/facebooks-ad-platform-now-guesses-at-your-race-based-on-your-behavior/),
 and [emotion recognition in workplaces](https://patents.google.com/patent/US10496947B1/en) or [educational institutions](https://www.sciencedirect.com/science/article/abs/pii/S036013152200032X). These aren't abstract examples; these are all technologies that have been developed and used already. The prohibition of these technologies is one of the strongest direct implications of the act.

High-risk AI systems are ones which are used as a safety component or that profile individuals. Providers of these systems must prove that they are managing the risk by providing documentation, designing systems to allow for human oversight, and being transparent about the system and its data. An example of this sort of system is automated hiring software, which is a [growing](https://www.findem.ai/) [market](https://clickup.com/home-1) fraught with problems of [bias](https://www.bbc.com/worklife/article/20240214-ai-recruiting-hiring-software-bias-discrimination) and [a lack of transparency](https://www.forbes.com/sites/forbestechcouncil/2023/09/25/ai-bias-in-recruitment-ethical-implications-and-transparency/). Another example is medical devices, which face both [incredible potential gains](https://www.theparliamentmagazine.eu/news/article/hitech-health-how-artificial-intelligence-is-revolutionising-healthcare) from AI as well as [many potential risks](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC9908503/). These high-risk applications are the most likely to be the subject of future litigation, and the act provides a framework for this litigation by setting a standard of the necessary compliance for these systems.

One point which was heavily debated is the [regulation of generative AI](https://www.nature.com/articles/d41586-024-00497-8) like ChatGPT. These technologies have been split into two tiers. The first tier covers all general-purpose models, except those used only in research or published under an open-source license. These will be subject to transparency requirements, including detailing their training methodologies and energy consumption, and must show that they respect copyright laws. The copyright point has been the subject of [much ongoing litigation in the US](https://www.thefashionlaw.com/from-chatgpt-to-deepfake-creating-apps-a-running-list-of-key-ai-lawsuits/). The second and stricter tier will cover general-purpose models deemed to have "high-impact capabilities," which pose a higher "systemic risk", such as massive language models like ChatGPT.[^1] While preliminary, the handling of generative AI is impressively done, considering how quickly the technology has advanced during the development of this act.

[^1]: One of the lines to differentiate high-impact is a rare specificity of the act: 10^25 floating point operations (FLOP) during training. To me, drawing the line on training FLOPs feels arbitrary and likely to be outdated in the future. 

The act clearly follows, and is designed to work with, the [General Data Protection Regulation (GDPR)](https://gdpr.eu/), a law designed to protect the privacy and personal data of individuals in the EU, adopted on April 14, 2016 and effective since May 25, 2018. Over the course of years, the GDPR has been refined and interpreted through [court cases](https://www.fieldfisher.com/en/insights/the-cjeus-judgement-in-meta-platforms-inc-v-bundekartellamt-the-spotlight-on-lawful-bases-for-processing-data) and the application of [fines](https://www.laquadrature.net/2021/07/30/amende-de-746-millions-deuros-contre-amazon-suite-a-nos-plaintes-collectives/). For example, the 
protection of data transferred between the EU and the US has been extensively debated in the [Schrems I](https://eur-lex.europa.eu/legal-content/EN/TXT/?uri=CELEX%3A62014CJ0362), and, following the publication of the GDRP, [Schrems II](https://curia.europa.eu/juris/liste.jsf?num=C-311/18) cases [^2]. The GDPR as written in 2016 was not the definitive stance on data privacy in the EU, but it was a necessary first step from which European agencies could act to protect individuals' privacy and data. Many other countries have adopted or are considering laws [similar to the GDPR](https://biblio.ugent.be/publication/8726790/file/8726791.pdf).

[^2]: The matter of US-EU data transfer may still be up for [further litigation](https://noyb.eu/en/european-commission-gives-eu-us-data-transfers-third-round-cjeu).

The European AI act is just the beginning of what will likely be a long process of refining and interpreting the rules governing AI in the EU. EU member states need to sign it, and even then it doesn't [go into effect immediately](https://artificialintelligenceact.eu/ai-act-implementation-next-steps/). As with the GDPR, the AI Act will be discussed and debated through court cases and the application of fines. Given the breakneck pace of progress in AI, it is necessary that this first step was taken. Securing development in AI so that it is safe and respects human rights is a difficult task, but this act is a momentous step in the right direction.

