---
category: commonsense/kb
path: ''
title: 'Enhancing Neural Data-To-Text Generation Models with External Background Knowledge'
pdf: 
bibtex: 
appendix: 
code: 
type: 'EMNLP 2020'
layout: nil
---

### Goal
improve reliability and adequacy while maintaining fluent output 

### Idea
Data-to-text -> two steps (text planning + plan realization)

### Method 
- *text planner*: non-nueral, determines the information structure and expresses it into a sequence of ordered trees
- each plan captures 1) the ordering of facts within the sentence, 2) the ordering of entities within a fact 3) the structure between facts that whare an entity
- plan data building: input triplets -> exhaustive generation of plans -> find *matching* plans using ref text
- plan realizer: neural NMT system. 
- eval on WebNLG corpus
<img src="/imgs/step-by-step.png"/>

### Contributions
- proposed adding an explicit symbolic planning component to a neural data-to-text NLG system
- The system performs on par with a strong end-to-end neural system regarding automatic eval metrics, while substantially outperforms regarding faithfulness to the input

### Limitations
- no referring strucutre between sentences (limited fluency)
- no way to decide order between trees (some sentences might be better come before other sentences)

### Comments
- Was interesting to see how coreference resolution can complicate the task and the method.
- has many good references to text planning 