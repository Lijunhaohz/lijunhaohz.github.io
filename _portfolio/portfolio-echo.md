---
title: "SJTU Echo: Voice QA Agent for Campus Guide and Information Service"
excerpt: "The capstone design project at University of Michigan - Shanghai Jiao Tong University Joint Institute.<br/><img src='/images/image-echo-main.png'>"
collection: portfolio
---

Duration: Sept 2024 - Dec 2024

[Source Code](https://github.com/xcczach/SJTU-Echo/tree/main)

![image-echo](/images/image-echo.png)

Background Introduction
======

Educational information retrieval is hindered by the inefficiency of traditional web browsing. It is difficult for students, faculty, and visitors to access specific and timely academic or campus-related announcements. This project is to build an intelligent voice agent system tailored for SJTU campus information QA, localizing the large language model with retrieval augmented generation (RAG).

![image-echo-1](/images/image-echo-1.png)

Concept Generation
======
The core component of the sub-system concepts is the localized large language model (LLM) with specialized knowledge collected from the information retrieval (IR) module. It involves an auto-speech recognition (ASR) module to detect the user’s voice query and a text-to-speech (T2S) module to generate a voice response. 

![image-echo-2](/images/image-echo-2.png)

![image-echo-main](/images/image-echo-main.png)

Design Description
======
Localization of LLM. Utilizing automated scrapping scripts, the design simulates web browsing behaviors for large-scale link extraction and content collection on the SJTU website. The specialized knowledge is wrapped under the RAG framework with hypothetical QA embedding. 
User Interaction. The design leverages Vue and Element Plus to build a web application, allowing users to interact with the QA agent using either text or voice input. The latter will be recognized by the ASR component SenseVoice [2]. Responses can either be shown in text or by generating audio using the T2S open-source model XTTSv2 [3]. We also used SadTalker [4] to provide immersive interaction with short videos of virtual humans. 

The QA interaction is simulated by creating a chat session and entering questions. The agent is able to provide text responses, relevant links, and virtual videos to the user. It keeps honest when dealing with unknown or unclear information. The following figure shows the demo.

![image-echo-4](/images/image-echo-4.png)

Validation and Conclusion
======
LLM Precision Validation. Ragas is a library performing evaluation of LLM applications. We focused on 5 metrics:
Context Recall, Faithfulness, Response Relevancy, Semantic Similarity, and Context Precision. The results show the satisfying precision of our model.

SJTU Echo demonstrates the potential of a localized multimodal QA agent in optimizing educational information retrieval methods. By integrating advanced technologies like speech recognition and video generation, the system provides precise, timely, and immersive responses to user queries with a user-friendly interface.
