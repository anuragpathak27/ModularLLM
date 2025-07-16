# 🧠 Modular LLM Architecture with Pluggable Reasoning Heads

A scalable and interpretable framework that enhances a frozen base language model (LLM) with **modular reasoning capabilities** using attachable **pluggable heads** for symbolic, logical, graph-based, or multimodal reasoning tasks.

## Overview

This project introduces a **controller-based architecture** where different reasoning modules ("heads") can be attached to a frozen LLM. Depending on the input type or intent, the controller routes the prompt to the appropriate reasoning head.

### Key Features
- Pluggable reasoning heads (e.g., Symbolic, Logical, Graph-based)
- Controller model for dynamic routing
- Frozen base LLM (e.g., LLaMA, GPT-2) for core generation
- Modular design with minimal retraining required
- Explainable reasoning path (transparent routing logic)

## Architecture

The system is built around a modular plug-and-play design that routes user prompts to specialized reasoning heads. A Controller Module interprets the prompt and dispatches it to the most appropriate reasoning head (e.g., symbolic, logical, or graph-based). The selected head performs reasoning, possibly augmenting or guiding a frozen base LLM to produce accurate and explainable results.

## WorkFlow

+-------------------+
|    User Prompt    |
+-------------------+
          |
          v
+---------------------+
|   Controller Module |
| (Intent Classifier) |
+---------------------+
     |     |      |
     |     |      |
     |     |      +--------------------+
     |     |                           |
     v     v                           v
+-------------+  +-------------+  +-------------+
| Symbolic    |  | Logical     |  | Graph-based |
| Reasoning   |  | Reasoning   |  | Reasoning   |
+-------------+  +-------------+  +-------------+
     \             \               /
      \             \             /
       \             \           /
        \             \         /
         \             \       /
          \             \     /
           \             \   /
            \             \ /
             v             v
           +--------------------+
           |   Frozen Base LLM  |
           | (e.g., GPT-2, LLaMA)|
           +--------------------+
                     |
                     v
           +--------------------+
           |  Final Response    |
           +--------------------+


## Reasoning Heads (Implemented)
 Symbolic – algebraic simplification, rule-based logic using SymPy

 Logical – Prolog-style query resolution

 Graph-based – node/edge reasoning using GNN or embeddings

 More coming soon...


## Demo (Coming Soon)
A Gradio demo will be added for interactive testing.

## Paper Reference
This project is part of the paper:
"Modular LLM Architecture with Pluggable Reasoning Heads: A Scalable Approach to Multi-Modal AI Reasoning"
Accepted at ETNCC 2025 for presentation

## Author
## Anurag Pathak

## License
This project is licensed under the MIT License.
