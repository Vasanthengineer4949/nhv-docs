# Evaluation of LLMs Is All You Need

## Introduction

🔍 **Unlocking the Unseen:** Delve into the world of LLM evaluation, a facet often underestimated yet holding the power to transform your model's prowess! 💎

🔢 **Crucial Queries Explored:**

- **Why Evaluate LLMs?** Discover the critical need for evaluation in maximizing model potential. Uncover why this step is a cornerstone of success, and how it can take your model from good to extraordinary.

- **What to Evaluate?** Explore the multifaceted approach to evaluation. Understand the dimensions that demand attention – from coherence to context handling – and how they collectively shape model effectiveness.

- **Where to Evaluate From?** Learn about the datasets that fuel evaluation. Explore the diverse sources required to gauge the model's performance across various aspects addressed in the 'What' section.

- **How to Execute Evaluation?** Unveil the strategies and techniques to conduct effective evaluation. From methodologies to metrics, this section provides the roadmap to assessing and enhancing model powers

🚀 **Elevate Your Model:** Elevating your model's performance is just a click away! Through comprehensive evaluation, you can turn setbacks into triumphs, failures into stepping stones towards success. 📈 This video is your complete A-to-Z guide, providing insights that can reshape your approach to LLMs.

## Evaluation

- Model evaluation is the process of analyzing the performance of the model with the help of some metrics
- Evaluating an LLM performance involves assessing factors such as language fluency, coherence, contextual understanding, factual accuracy, and ability to generate relevant and meaningful responses.

## What is a good evaluation?

- **Correlated with outcomes:** Appropriate metrics used for appropriate models
- **Very less number of metrics, in an ideal world single metric:** Easy to track and monitor and make a judgement accordingly
- **Fast and automatic as possible to compute:** We can't completely automate the evaluation. It is important to have a human intervention but yet the evaluation should be as automated and fast as possible

## Why the conventional methods of evaluation doesn't work for LLMs?

- The data used while training and production are always not the same. It can be as different as possible

- Another key bottleneck is that in LLMs we wont have definitive results. It has a complex generation behavior which is hard to understand. Though the sentence generated would be different from the ground truth the generated sentence will provide the same contextual meaning.

- **For eg:**

```

In Traditional ML, lets consider a scenario of sentiment analysis

    pred = [P, N, P, P]
    label = [P, N, P, N]

For the above set to be evaluated we can use metrices like accuracy which here will be 0.75 but that cannot be the case for LLMS

For LLMs, lets consider a case of summarization of a context given

    pred = Usually LLMs works very well with wide variety	of NLP tasks because they are great generalists by nature
    label = LLMs are great generalists, so they usually work pretty good with variety of NLP tasks

Both convey the same meaning if we see it in a contextual way then the model can be given 100% but usually traditional methods are not qualitative but quantitative.

```

Thus it is hard to have a conventional metric to quantify the evaluation.

## Critical Questions of Evaluation

There are four main questions to consider in evaluation. They are:

- Why to evaluate?
- What to evaluate?
- Where to evaluate?
- How to evaluate?

Now lets answer each question in detail one by one right now

## Why to evaluate?

Here are some of the reasons why evaluation is very necessary and why it is said to be one of the most underrated aspect of the LLM pipeline

### Increase model performance

By evaluating the model one can understand the strengths and weaknesses of a model. Once a models weaknesses are known one can then move onto the next steps to increase the performance working on the weaknesses of the model.

**For eg:** PromptBench indicates a fact that the current LLMs are sensitive to adversarial prompts which implies that you can gain better performance with careful prompt engineering

### Better Human-LLM interaction

With better evaluations it can provide better guidance for human-LLMs interaction which can lead to some better experience of the users

**For eg:** Once you know if your model is exhibiting an emotion for a specific way of interaction then a work around could be made to make the interaction better to get the desired output from the model

### Safety and Reliability

LLMs have a broad applicability and are used in various sectors even in some sectors which may require safety and reliability like some financial or healthcare institutions. So it is important to ensure the safety and reliability of the model

Thus it is important to have evaluation as one of the most important discipline in the LLM building pipeline

## What to evaluate

Once we find the answer to the question we can claim the strengths and weaknesses of LLMs. the answer to the question is the different tasks which are there to evaluate against the model. Here are the broad categories in which there are the tasks against which the model to be evaluated.

- Natural Language Processing
- Robustness, Ethics, Bias and Trustworthiness
- Social Science
- STEM
- Applications

### Natural Language Processing Tasks

The main objective behind the development of LLMs was to get enhanced performance in NLP tasks be it understanding or generation

#### Natural Language Understanding

It represents wide range of tasks that aims at model having a better understanding of the input provided. Here are the tasks which comes under the umbrella of NLU

##### Sentiment Analysis

Sentiment analysis involves analyzing and interpreting the emotion in text. Typically it is binary or triple. LLMS have shown great performance overall but with low resourced language it wasnt able to perform as expected

##### Text Classification

Though it is as similar as sentiment analysis, it just not focuses on the sentiment it also includes all the processing and different aspects of the text. Again as provided in sentiment analysis the inference holds here as well with great performance but there are some future work to be done with low resourced languages

##### Natural Language Inference

It is a task of determnining whether the given hypothesis logically follows the given context known as the premise. ChatGPT outperforms others in handling factual input. It is possible due to RLHF training process which helps in favoring to human preferences. But usally LLMS have poorly in case of NLI tasks and there are large improvements needed in this field

##### Semantic Understanding

It refers to understanding of the language and the concepts associated. It involves the interpretation and comprehension of words, phrases, sentences and the relationship between them thus processing goes beyond the surface level and understanding the underlying meaning and intent. In individual events LLMs possess a great understanding but with multiple events the performance among events has been subpar. With evaluating against basic phrases the LLMs perform poorly. So in general LLMs semantic understanding performance is poor with lot of room for improvment


#### Reasoning

Reasoning intuitively if we see also involves semantic understanding which has been a significant challenge for models. To effectively handle reasoning tasks the model not only needs to understand the provided information but also utitlixe reasoning based on the understood information. The evaluation can be broadly categorized into mathematical reasoning, commonsense reasoning, logical and domain-specific reasoning. 

Under these categories overall performance has been satisfactory but with high complexity in mathematical or logical reasoning the model performance has been subpar. Models have shown  good performance with commonsense reasoning but with domain specific reasoning there are lots of room for improvement. So in general reasoning capabilities of model needs to improve a lot

#### Natural Language Generation

It evaluates the capabilities of LLMs in generating specific texts which consists of several tasks including summarization, dialogue generation, machine translation, QA and open ended generation applications

##### Summarization

It is one of the most popular tasks going right now which aims to learn a concise abstract for the given input sentences. In controllable text summarization LLMs have been more extractive compared to human summaries. On general summarization has been having a general performance in summarization tasks and there are requirements for further improvement

##### Dialogue

Evaluating the performance of LLMs on dialogue tasks is crucial to the develoipment of dialogue system which acts as the interface for human LLM interaction. On general with good NLU capabilites it has given some good performance but here are some of the challenges for the models in which the models tend to make errors usually: long-term multi-turn conversational dependency, fundamental reasoning failure and hallucination

##### Translation

LLMs are explicitly not trained for translation task but still they have shown great performance for translation tasks. On an overall factor LLMs have performed translation very well with a scenario like X -> Eng with English being the target language but in the vice versa scenario it has not performed very well and with low resourced languages it has been more worse

##### Question Answering

QA is a crucial technology in acting as an interface for human-LLM interaction and it has been found useful in many scenarios like search engines, intelligent customer services, QA systems and may more. Overall LLMs have been nearly flawless with the performance on QA tasks but there are potential improvement in answering questions based on social, event and commonsense knowledge

##### Open Ended Generation tasks

There are different generation tasks other than the tasks discussed above in which there are tasks like sentence style transfer, variety of writing tasks such as informative, professional, creative and many more. In general LLMs have shown great proficiency in their writing capabilities

##### Multilingual Tasks

LLMs generally have performed poorly when it comes to non-Latin languages like Indic languages and even worse with languages with limited resources. So there is a huge room of improvement for LLMs with multilingual tasks

##### Factuality

Factuality in the context of LLMs refers to the extent to which the text generated by the model align with real world truths and verifiable facts. Thus evaluating factuality is of great importance in order to trust the model and use it. For a model to be factual it should not generate misleading or false information also known as factual hallucination. To evaluate the model on this aspect TruthfulQA can be used as a benchmark whcih is designed to cause models to make mistakes in providing factual answers. the findings implicate that increasing sizes does not make the model truthful for which there is a improvement needed

### Robustness, Ethic, Bias and Trustworthiness

Some of the crucial aspects of evaluation of LLMs includes robustness, ethics, bias and trustworthiness all checking its personal characteristics under circumstances

#### Robustness

Robustness studies the stability of the model when facing unexpected inputs such as adversarial prompts and OOD. For evaluating on this aspect there are different benchmarks like AdvGLUE, PromptBench and many more. On an overall aspect the model is said to be prompt sensitive and model generally tends to exhibit subpar performance with adversarial prompts

#### Ethics and Bias

LLMs have been found to internailize, spread and potentially magnify harmful information existing in the open domain corpus in which it was pretrained on thus exhibiting some bias and its own ethics. When role playing was introduced to the model it caused biased toxicity to some specific entitites upto 6x. Also LLMs were found to have moral biases and cultural values. All these might result in serious risk after deployment of LLMs into the society

#### Trustworthiness

A model is said to be evaluated for its trustworthiness in the following eight aspects: 

- toxicity
- stereotype bias
- adversarial robustness
- OOD robustness
- adversarial demonstration robustness
- privacy
- machine ethics
- fairness

To deploy a model into a real world scenario it is important for the model to be trustworthy

### Social Science

Social science involves the study of human society and the individual behaviours also including some subjects like economics, sociology, political science, law. Evaluating the performance of of LLMs in social science is important to know its social problem solving ability and applicability of knowledge to such problems. Overall LLMs has benefitted individuals in addressing social science related tasks improving productivity

### STEM - Science, Technology, Engineering and Mathematics

Evaluation of models in STEM can help in various aspects like personal education, research, etc... to increase productivity. 

#### Math

In mathematics with simple arithmetic tasks it has performed very well but with tasks like trigonometry, logarithm the performance has been subpar finding it challenging. It has been competent handling fractions, decimal numbers, negative and irrational numbers as well but has failed poorly with lengthy complex and challenging mathematical equations and problems. In general the effectivenss of LLMs is highly influenced by the complexity of the problem

#### Science

In science it has provided some commendable performance with biology and general simple science related tasks but there are improvments needed with chemisty and physics related tasks especially in physics since the model performs worse in physics than in chemistry problems. Thus improvement is needed in this field

#### Engineering

In the order of difficulty the tasks can be ordered as code generation, software engineering and commonsense planning where in the code generation and software engineering aspect LLMs outperform SOTA outputs and even human outputs but improvements are needed in common sense planning showing there is need for improvement in complex engineering tasks

### Application

#### Agent Application

Instead of just using LLMs on general language tasks LLMs have been equipped with tools lately to expand the capabilites of LLM like ToolLM a comprehensive framework to equip llms with tool use capabilites and there are some other models like KOSMOS-1 for general patterns understanding, TALM again for utilization of tools, Toolformer for optimal use of specific APIs and so on and so forth.

#### Search and Recommendation

Assessment of LLMS in search and recommendation is broadly categoried into two areas where firstly in information retrieval LLMs have outperformed SOTA models right now and people find it easy and less time consuming to search in ChatGPT than in Google search.

With enormous NLP capabilites LLMs have proven to be a way to build recommendation systems comprehending user preferences, item descriptions and any type of contextual informations. But there have been scenarios of unfair recommendations from LLMs like ChatGPT which emphasizes the importance of evaluation of fairness in recommendation

#### Personality Testing

It measures the personality traits and behavioral tendencies of LLMs applied in wide range ofg tasks showing that LLMs can perform like humans but still there are limitations in current model to effectively understand and generate humour

#### Specific applications

LLMs have been said to have a broad applicability but when they are applied on tasks like log parsing, game designing it showed some limitations with the tasks but with potential to improve

## Where to evaluate

Now that we know the tasks/facets in which the model needs to be evaluated lets move on to the next section which is about the benchmarks for LLM. Here are some of the benchmarks for LLMs

### Chatbot Arena

- Chatbot Arena is a platform which is used to compare the performances of diverse chatbot models with anonymous user engagement and voting which shows the preferences of the users in realtime scenarios
- Thus chatbot arena is a benchmark which provides insights about the strengths and weaknesses of Chatbot models

> Benchmark: [Link](https://chat.lmsys.org/){ .md-button }

### MT-Bench

- MT-Bench is another benchmark to evaluate the conversational capability of a LLM.

- It evaluates on multi-turn dialogues using questions which are comprehensive in nature created in order to handle the conversations which replicates real case scenarios showing the closest to models practice performance

- In simple words it is used to evaluate the model's multi turn conversation capability

> Benchmark: [Link](https://huggingface.co/spaces/lmsys/mt-bench){ .md-button }

### HELM - Holistic Evaluation of Language Models

- A benchmark as the name suggests provides a comprehensive assessment of LLMs

- It evaluates the LLMs across 42 scenarios with 59 metrics. Some of the scenarios are QA, IR, Summarization, Reasoning, Coherence, etc... including domain specific knowledge. Some of the metrics are pass@1, rouge, f1, etc...

> Benchmark: [Link](https://crfm.stanford.edu/helm/latest/){ .md-button }

### BIGBench - Beyond the Imitation Game Benchmark

- Bigbench is one of the famous benchmarks going around right now which provides around 204 challeging tasks from 450 authors.

- It covers various domains like math, biology, commonsense reasoning and many more

> Benchmark: [Link](https://github.com/google/BIG-bench){ .md-button }

### KOLA - Knowledge Oriented Language Model Evaluation

- KoLA focuses on the comprehension capabilities of the models

- It is an important benchmark to assess the indepth language understanding and reasoning capabilities of the LLMs

> Benchmark: [Link](https://github.com/THU-KEG/KoLA){ .md-button }

### DynaBench

- A benchmark which supports dynamic benchmarking

- With Dynabench, it collects human-in-the-loop data dynamically, against the current state-of-the-art, in a way that more accurately measures progress

- It is a more robust way considering it is a crowd sourced mechanism

> Benchmark: [Link](https://dynabench.org/){ .md-button }

### MMLU - Measuring Massive Multitask Language Understanding

- MMLU is a benchmark designed to evaluate the models in a zero shot and few shot setting making it more challenging

- It covers 57 different subjects in STEM, humanities, social science and many more domains

- It has difficulty levels from elementary to professional where it tests both the world knowledge and problem solving ability accordingly

> Benchmark: [Link](https://github.com/hendrycks/test){ .md-button }

### AlpacaEval

- It is an automated evaluation benchmark of instuction following models which asssesses the performance of the models across NLP tasks with almost 20K annotations

- It provides an idea on models robustness, diversity and many more capabilites of LLMS in various domains

> Benchmark: [Link](https://github.com/tatsu-lab/alpaca_eval){ .md-button }

### Open LLM

- Huggingface Open LLM leaderboard servs an evaluation benchmark by having a public competitive platform 

- It compares and assesses the different models performance on various tasks

> Benchmark: [Link](https://huggingface.co/spaces/HuggingFaceH4/open_llm_leaderboard){ .md-button }

### GLUE-X

- It is an attempt to create an unified benchmark consisting of 14 publicly available dataset for evaluating the model performance on OOD scenarios

- It mainly focuses the robustness of the model under various scenarios

> Benchmark: [Link](https://github.com/YangLinyi/GLUE-X){ .md-button }

### PromptBench

- PromptBench is an another benchmark which focuses on the OOD and adversarial robustness of th model

- Ir provides a standardized evaluation framework to compare the different prompt engineeering methods and their impact on model performance thus leading to enhancement of model performance

> Benchmark: [Link](https://github.com/microsoft/promptbench){ .md-button }


### SPECIFIC TASK BENCHMARKS

The above mentioned benchmarks mainly focuses on the general language level capabilities of the model. The following table shows for specific task

|Task Name|Task Focus|Link|
|---------|----------|----|
|**SOCKET**| Social Knowledge of LLMs |[Link](https://huggingface.co/datasets/Blablablab/SOCKET)|
|**ARB**| Advanced Reasoning Tasks across multiple domains |[Link](https://github.com/TheDuckAI/arb)|
|**TRUSTGPT**| Ethical considerations - Toxicity, Bias and Values Alignment in context|[Link](https://github.com/HowieHwong/TrustGPT)|
|**CEval**| Reasoning Capabilities in Chinese | [Link](hhttps://cevalbenchmark.com/)|
|**M3Exam**| Comprehensive framework with multiple exams in modalities, languages and levels | [Link](https://github.com/DAMO-NLP-SG/M3Exam)|
|**MATH**| Math Reasoning and Problem solving | [Link](https://github.com/hendrycks/math)|
|**APPS**| Rigorous benchmark to evaluate LLM's capability to generate python code | [Link](https://github.com/hendrycks/apps)|
|**CUAD**| Legal documents review| [Link](https://www.atticusprojectai.org/cuad)|
|**CVALUES**| LLMs safety and responsibility standards |[Unable to find](#specific-task-benchmarks)|

Along with the above mentioned benchmarks there are lots of other benchmarks like ANLI, LIT, CoQA, LAMBADA, HellaSwag, LogiQA, MultiNLI and many more. There is a very recent benchmark which came by the name of ToolBench

### ToolBench

- A benchmark which is used to evaluate tool-augmented LLMs

- It has 53 commonly used API tools , 264 dialogues and 568 API calls

- It focuses on enhancing the LLMs practical application

> Benchmark: [Link](https://github.com/OpenBMB/ToolBench){ .md-button }

## How to evaluate

Now that we have the benchmark to evaluate it is time to find the answer for the question of how to evaluate. There are two main ways of evaluation. They are:

### Automatic evaluation

- Automatic evaluation is the most popular method of evaluation which involves using popular metrics or indicators like ROUGE, BLEU, Accuracy, F1-score, etc... due to its very less complexity

- With NLU and math tasks which is deterministic in nature this evaluation protocol is used

- Though there are lots of advantages it is not the best way to evaluate due its subjective nature

- LLM-Eval is a recently proposed method fo automatic evaluation of open domain conversations

- An another LLM based method is PandaLM which uses an LLM as a judge to evaluate different models

### Human evaluation

- The capabilites of LLMs has surpassed the standard performance metrics requiring some human evaluation in cases where automatic evaluation is not suitable. **For eg:** Open ended generation

- Usually it is more preferable to have human evaluation for generation tasks

- It is more accurate, comprehensive and close to the real world scenario. But it is highly complex and costly

- In a practical scenario, both the evaluation methods are considered and weighed based on the situation - **AUTO HUMAN EVAL - THE WAY TO GO**

## Success and Failure Cases of LLMs

### Success

- Generation of text with fluency
- NLU tasks such as classification
- Robust contextual comprehension
- Satisfying performance across NLP tasks

### Failure

- Bias and Inaccuracy while generation
- Limited comprehending abilities with complex reasoning and logic tasks
- No dynamic knowledge updataion
- Prompt sensitive
- Subpar performance in counterfactual tasks

