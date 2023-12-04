---
layout: post
title: From Quantitative Finance to Machine Learning
date: 2023-11-21 00:00:00
tags: Digital-Transformation DevEng Machine-Learning
categories: reflections
description: Know me better through where did I start and how I ended up doing Machine Learning, especially Large Language Models. 

toc:
  sidebar: left
_styles: >
  ol {
    list-style-type: decimal;
    padding-left: 20px;
  }
  ul {
    list-style-type: disc;
    padding-left: 20px;
  }
  ol ul, ul ul {
    list-style-type: circle; /* or 'circle', 'square', 'decimal', etc. */
    padding-left: 40px;
  }
  ol ol, ul ol {
    list-style-type: decimal; /* or 'circle', 'square', 'decimal', etc. */
    padding-left: 40px;
  }
---

At present, I am seeking a full-time position as a Machine Learning Engineer or Data Scientist, starting from January 2023. I recently completed my internship with the Walmart Sourcing Tech team in Shanghai, where I served as a Machine Learning Engineer. During my tenure, I developed and trained an LLM-driven chatbot from scratch to provide 24/7 internal technical support, complementing our human associates.  

From July 2021 to March 2022, I worked as a Data Scientist at Buy-Quickly and the Alibaba Tmall Division. My primary responsibility was to design a clustering algorithm tailored for a specific segment of online consumers. Additionally, I initiated a data pipeline project at Buy-Quickly.  

During my undergraduate studies, I was involved in two significant research projects. The first was at the Attitude Research Lab, where we delved into the impact of technical interventions on consumer psychology, with a particular focus on ambivalent attitudes. The second was at the Intelligent Finance Lab. Here, I contributed to a study examining the transformations, and transfer tendencies of Chinese industries over the past three decades.

### Digital Transformation is what I have been pursuing

Digital Transformation is what I see as my pursuit. Over the years of my experiences in different industries, I have witnessed the power of data and technology, but I have also seen a great number of companies falling behind the trend, especially in traditional industries, where labor in the main force of production but the power of data and technology has yet to be harvested. I want to be part of the change, to help companies and organizations to transform digitally, to help them to be more efficient, more productive and more sustainable.
I believe there are several different phases of digital transformation. Starting from AUTOMATION, it is the most basic and fundamental step for standard production procedure. INFORMATION is the next step, where data from all departments are collected and stored, and the company starts to make decisions taking data as a reference. INTELLIGENCE is the last step, where data is utilized for prediction and optimization. I have seen many companies stuck at the first step, and I want to help them to move forward.    

You can find more about my thoughts on digital transformation in this [post](https://eric-miao.github.io/blog/2023/oped/)


### Promote Orange Industry in Rural China with Technology

>- TIME: 03/2018 - 08/2018
>- PLACE: Shimian, Sichuan, China
>- ROLE: Volunteer 

In 2018, I embarked on a project to empower a rural community in Sichuan, China, which was primarily involved in orange farming, in another word, help them sell their oranges and improve their lives. We helped them establish online distrbutions channels and built a mobile app for them to reach customers all over China. We also shot a video to promote the local travel industry. The project is still ongoing and I am happy to witness the progress they have made.
Please check out the following video for more details.

Here is a more comprehensive review of the project: [link](https://eric-miao.github.io/blog/2023/orange-orchand/)


<div class="col-sm mt-3 mt-md-0">
    {% include video.html path="https://www.youtube.com/embed/rh0tNTY2uNY?si=zNEUJqHOUhHQ6ftm" class="img-fluid rounded z-depth-1" %}
</div>
<div class="caption">
    This is the video that we made for the local industry.
</div>

### Upgrade of Inventory Management of Manufacturing Industry

>- TIME: 12/2020 - 02/2021
>- PLACE: Jinsung, Yantai, China
>- ROLE: Digital Transformation Consultant

In the winter of 2020, I was involved in a digital transformation project in a manufacturing company in Yantai, China. The company has a long history and a considerable market share. However, the inventory system of this specific branch was still in the early stage of automation. The company was facing a series of problems, including low efficiency, high cost, low accuracy and inconsistency. I was responsible for upgrading the inventory infrastructure and optimizing the inventory management process. I designed a new tray management system, adding RFID chips to the trays and installing RFID readers at the entrance and exit of the warehouse so that all the materials can be tracked in real-time in and out the space. This system was integrated with their ERP system, automating the whole process of production, greatly improving the efficiency and accuracy of the inventory management.

<div class="row justify-content-sm-center">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/rfid.jpg" title="title image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The RFID chip that is attached to the tray.
</div>

### Enhance Efficieny of E-Commerce Analysis with Data Pipeline

>- TIME: 07/2021 - 03/2022
>- PLACE: Alibaba/BuyQuickly, Shanghai, China
>- ROLE: Data Scientist

After graduating from undergraduate school, I joined an E-Commerce company in China as a Data Scientist. During that time, I also served at Alibaba Group with similar duty. This is the first time that I was able to brought Machine Learning and Data Scientist to achieve progess in digital transformation. I have constructred a data pipeline, where statistics from various sources can be collected, processed and visualized automatically. The goal of the system is to minize the time spent on routinely data collection and encourage associate to focus on more valuable tasks.  

<div class="row justify-content-sm-center">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/data_pipeline.png" title="title image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    An abstraction of the pipeline.
</div>

At the same time, I devised and implemented an algorithm to score customers in online luxury market and further segmented them into several categories with unique distinguishing features. This is for our clients to better characterize their target audience for personalized advertisement as well as locate themselves in an alien market. This methodology as well a utility toolkit going with it has been published to thousands of online merchants to accelerate their business. 

To view the whitebook of this project, please refer to this [post](https://eric-miao.github.io/projects/tmall/).

### Large Language Model journey

>- TIME: 06/2023 - 08/2023
>- PLACE: Walmart, Shanghai, China
>- ROLE: Machine Learning Engineer

The emerge of LLM pushed the Machine Learning to another peak. Fortunately, this is not a field that is too far from me to reach. During the summer of 2023, I interned at Walmart and tried to conduct some of the LLM work.
During my internship at Walmart Sourcing Tech I worked on a groundbreaking project aimed at desting and speesting lesing tered Chater. the prima chiede the entor neste
This project began from scratch, I planned to finetune a model, considering the limited resources we had. After rigorous testing, evaluation and leveraging our computational power, I landed on the facebook/opt-1.3b and bigscience/bloom-560m models. The corpus consists of Q&A session records, wiki documents, and technical support emails, with prompt engineering which helped a lot. Since I only had 4 Tesla T4 GPU, I took advantage of LoRA and DeepSpeed ZeRO3 for acceleration and computation reduction. After 2 months' finetuning and iterating, I achieved a remarkable 70% accuracy in the Chatbot's responses, almost as good as a human associate. To further enhance its performance, l integrated a text embedding database to upback the Chatbot's responses.
I deployed to the Azure and took the initiative to develop a user-friendly web client with Python.
During my tenure, the Chatbot was live for three weeks, during which the user feedback on accuracy and performance were collected for future model refinements and improvements.

<div class="row justify-content-sm-center">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/chatbot.png" title="title image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    An demonstration of the Chatbot that I have developed.
</div>

## Future

I see myself as a Machine Learning Engineer as well as a Digital transformation promoter. However, Digital transformation will be a lengthy and tough journey in any industry. It contains several stages, each of which is a complex system question involving not only technical solutions, but also a comprehensive adjustment of the system as a whole.
I desire to devote myself to promote digital transformation in more realms, harnessing the power of technology and making a better world.