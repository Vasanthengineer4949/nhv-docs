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

## What is a good evaluation:

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

