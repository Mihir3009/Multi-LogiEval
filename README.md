# Multi-LogiEval: Towards Evaluating Multi-Step Logical Reasoning Ability of Large Language Models

You may want to check out our paper here - https://arxiv.org/abs/2406.17169

As Large Language Models (LLMs) continue to exhibit remarkable performance in natural language understanding tasks, there is a crucial need to measure their ability for human-like multi-step logical reasoning. Existing logical reasoning evaluation benchmarks often focus primarily on simplistic single-step or multi-step reasoning with a limited set of inference rules. Furthermore, the lack of datasets for evaluating non-monotonic reasoning represents a crucial gap since it aligns more closely with human-like reasoning. To address these limitations, we propose _Multi-LogiEval_, a comprehensive evaluation dataset encompassing multi-step logical reasoning with various inference rules and depths. _Multi-LogiEval_ covers three logic types — propositional, first-order, and non-monotonic consisting of more than 30 inference rules and more than 60 of their combinations with various depths. Leveraging this dataset, we conduct evaluations on a range of LLMs including GPT-4, ChatGPT, Gemini-Pro, Yi, Orca, and Mistral, employing a zero-shot chain-of-thought. Experimental results show that there is a significant drop in the performance of LLMs as the reasoning steps/depth increases (average accuracy of $\sim68\%$ at depth-1 to $\sim43\%$ at depth-5). We further conduct a thorough investigation of reasoning chains generated by LLMs which reveals several important findings. We believe that _Multi-LogiEval_ facilitates future research for evaluating and enhancing the logical reasoning ability of LLMs.

## Data Release

Please see `./data` folder to access the _Multi-LogiEval_ dataset.

**Licence:** MIT License

```data/``` contains both versions of the dataset and is distributed in the folder as follows:

    ├── ...
    ├── data
        ├── d1_Data
        │   ├── first_order_logic
        |   |   ├── rule_1.json
        |   |   ├── rule_2.json
        |   |   ├── ...
        |   |   └── rule_n.json
        │   ├── nm_logic
        |   |   ├── rule_1.json
        |   |   ├── rule_2.json
        |   |   ├── ...
        |   |   └── rule_n.json
        │   └── propositional_logic
        |       ├── rule_1.json
        |       ├── rule_2.json
        |       ├── ...
        |       └── rule_n.json
        ├── d2_Data
        │   ├── first_order_logic
        |   |   └── ...
        │   ├── nm_logic
        |   |   └── ...
        │   └── propositional_logic
        |       └── ...  
        ├── d3_Data
        │   ├── first_order_logic
        |   |   └── ...
        │   ├── nm_logic
        |   |   └── ...
        │   └── propositional_logic
        |       └── ...
        ├── d4_Data
        │   ├── first_order_logic
        |   |   └── ...
        │   ├── nm_logic
        |   |   └── ...
        │   └── propositional_logic
        |       └── ...
        ├── d5_Data
        │   ├── first_order_logic
        |   |   └── ...
        │   ├── nm_logic
        |   |   └── ...
        │   └── propositional_logic
        |       └── ...
        └── multivariable_fol_Data
            ├── fol_multi_1.json
            ├── fol_multi_2.json 
            ├── ... 
            └── fol_multi_7.json


In all these folders, the JSON file corresponding to each inference rule is formatted as below:

### JSON file format for _Multi-LogiEval_

```JSON
{
    "logic": "str",
    "rule": "str",
    "depth": "str",
    "samples": [
        {
            "id": "int",
            "context": "str",
            "question": "str",
            "answer": "str"
        },
        {
            "id": "int",
            "context": "str",
            "question": "str",
            "answer": "str"
        },
        {
            "id": "int",
            "context": "str",
            "question": "str",
            "answer": "str"
        }
    ]
}
```

            
