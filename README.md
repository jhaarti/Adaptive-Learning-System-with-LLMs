# Adaptive Learning System Using Open-Source LLM
This repository provides an adaptive learning system using an open-source large language model
(LLM) to dynamically generate educational tasks, evaluate responses, and fine-tune itself based on
performance. The adaptive cycle allows the model to continuously improve its accuracy and adapt
to increasing complexity, providing a self-improving learning system.

## Project Overview
This adaptive learning system operates in cycles, allowing the model to adjust its understanding and
task difficulty based on performance. Here’s how it works:
1. Generate Task: The model generates questions based on specified topics and difficulty levels,
adapting over time as it fine-tunes on generated data.
2. Generate Response: The model (acting as the “student”) generates answers to the questions,
simulating a student’s response to each generated task.
3. Evaluate Response: Responses are evaluated by comparing them to expected answers using
semantic similarity scoring.
4. Update Difficulty: The system adjusts task difficulty based on the score, increasing or decreasing
complexity to match the model’s performance.
5. Fine-Tune Model: Task-response pairs are used to fine-tune the model, allowing it to learn from
previous tasks and improve accuracy.
This cyclic process allows the model to become more precise in generating relevant responses, and
the fine-tuning step reinforces learning from prior mistakes, enabling gradual improvement.

## Why This System Works
- Continuous Improvement: The fine-tuning step allows the model to adapt based on evaluated
responses, progressively enhancing performance on similar tasks.- Dynamic Difficulty Adjustment: By adjusting task difficulty based on performance, the system
ensures the model is always challenged but not overwhelmed, simulating a real learning curve.
- Versatile Adaptability: This setup can be applied to various topics, from simple questions to more
complex, nuanced inquiries, making it a scalable approach to model training.

## These Models Are Used
• GPT-2 for Task and Response Generation: GPT-2 is a widely accessible and effective
open-source model for generating language-based tasks and responses. It is flexible enough
for fine-tuning, making it ideal for creating an adaptive learning loop where performance
improves over time.
• Sentence Transformers for Evaluation: Sentence Transformers are specifically designed
for semantic similarity tasks. By embedding both the generated responses and reference
answers, this model provides a robust metric for evaluating response accuracy, allowing us
to quantify how well the model is learning.

## Alternative Options
If desired, you could replace GPT-2 with other transformer models from Hugging Face, such as
DistilGPT-2, GPT-J, or GPT-Neo, depending on your computational resources and specific needs.
Similarly, there are various other Sentence Transformer models optimized for semantic similarity
tasks that could be used for evaluation.

## Requirements
To run this project, you’ll need the following dependencies:
- transformers: For loading and fine-tuning the language model.
- sentence-transformers: For evaluating response accuracy using semantic similarity.
- datasets: For managing the generated data and handling fine-tuning.
- torch: For PyTorch support.
- 
Install these packages via pip:
```bash
pip install transformers sentence-transformers datasets torch


