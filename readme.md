# Project: Transformer-based Classifier for Multi-NLI Task

## Overview

The [Multi-Genre Natural Language Inference (MultiNLI)](https://huggingface.co/datasets/nyu-mll/multi_nli) task is a challenging problem in natural language processing. It involves determining the logical relationship between two sentences: a premise and a hypothesis. The goal is to classify the relationship into one of three categories:

1. Entailment: The hypothesis is true given the premise.
2. Contradiction: The hypothesis cannot be true given the premise.
3. Neutral: The hypothesis may or may not be true given the premise.

In this project, you will develop a Transformer-based classifier for the multi-NLI (Natural Language Inference) task using the dataset provided by torchtext. You are required to use the transformers package from Hugging Face to implement your solution.

### Data Format

Each example in the MultiNLI dataset consists of:
- A premise sentence
- A hypothesis sentence
- A label indicating the relationship (entailment, contradiction, or neutral)

The model should output a classification for each pair of sentences, predicting whether the relationship is entailment, contradiction, or neutral.

Example of a data instance:
```json
{
    "promptID": 31193,
    "pairID": "31193n",
    "premise": "Conceptually cream skimming has two basic dimensions - product and geography.",
    "premise_binary_parse": "( ( Conceptually ( cream skimming ) ) ( ( has ( ( ( two ( basic dimensions ) ) - ) ( ( product and ) geography ) ) ) . ) )",
    "premise_parse": "(ROOT (S (NP (JJ Conceptually) (NN cream) (NN skimming)) (VP (VBZ has) (NP (NP (CD two) (JJ basic) (NNS dimensions)) (: -) (NP (NN product) (CC and) (NN geography)))) (. .)))",
    "hypothesis": "Product and geography are what make cream skimming work. ",
    "hypothesis_binary_parse": "( ( ( Product and ) geography ) ( ( are ( what ( make ( cream ( skimming work ) ) ) ) ) . ) )",
    "hypothesis_parse": "(ROOT (S (NP (NN Product) (CC and) (NN geography)) (VP (VBP are) (SBAR (WHNP (WP what)) (S (VP (VBP make) (NP (NP (NN cream)) (VP (VBG skimming) (NP (NN work)))))))) (. .)))",
    "genre": "government",
    "label": 1
}
```

## Project Requirements

**Minimum requirements**

1. Implement a Transformer-based classifier for the MultiNLI task using the Hugging Face `transformers` library.
2. Fine-tune the model on the MultiNLI dataset.
3. Evaluate the model's performance using appropriate metrics (e.g., accuracy, F1 score).
4. Provide a detailed analysis of the results, including examples of correct and incorrect predictions.

**Optional**

For additional points, you can explore one or more of the followings:

1. Incorporate structured knowledge (syntactic parsing of premise and hypothesis) provided by Multi-NLI in your framework to further enhance the performance.
2. Comparison with fine-tuning performance of different Transformer backbones of similar scales (e.g., BERT, RoBERTa, ALBERT) and provide reasonable analysis.
3. Explore parameter-efficent finetuning methods with `peft` library, e.g., prefix-tuning or LoRA (Low-Rank Adaptation) fine-tuning. Compare the performance and training curves of these methods with full fine-tuning.

## Submission Guidelines

1. Submit your Jupyter notebook or Python script via the course management system.
2. Include your report as a PDF file.
3. Ensure all code is well-documented and runs without errors.

## Resources

- MNLI dataset: https://huggingface.co/datasets/nyu-mll/multi_nli
- Hugging Face transformers library: https://huggingface.co/transformers/
- Tutorial on fine-tuning transformers: https://huggingface.co/transformers/training.html
- Parameter-efficient finetuning: https://huggingface.co/docs/peft/index

Good luck with your project!