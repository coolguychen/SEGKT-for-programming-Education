# SEGKT-for-Programming-Education
*SEGKT: A SENet-Integrated Graph Neural Network Model for Knowledge Tracing in Programming Education*

## Overview
This repository provides an overview of SEGKT, a knowledge tracing model specifically designed for programming education. The architecture of SEGKT is as follows:
![image](https://github.com/user-attachments/assets/aeba6c95-d4dc-4889-ad4b-6647d5c5feea)



## Dataset
The experimental data comes from the **CodeWorkout Dataset**. It is a publicly available Java programming dataset that contains source code submissions from students. This dataset was part of [the 2nd Computer Science Education Data Mining Challenge (CSEDM)](https://sites.google.com/ncsu.edu/csedm-dc-2021/home) and is accessible for educational research purposes. It includes programming exercises from 413 students, covering 50 problems in total.

The dataset is organized into 5 task sets (A1~A5), each containing a specific set of programming challenges designed to assess various programming concepts and difficulty levels. We have annotated each task set with knowledge concepts, allowing the model to trace students' mastery across various programming concepts. The distribution of knowledge concepts within each task set is detailed in the paper.  You can also access these annotations and additional data files at the following paths within the repository:
- Task set annotations: `data/$ass_id$/$ass_id$.xlsx`
- List of programming knowledge concepts: `data/all_concept.xlsx`
- Preprocessed dataset: `data/data_ast.csv`
  

| **Attribute**                | **Count** |
|------------------------------|-----------|
| Number of Students           | 413       |
| Number of Problems           | 50        |
| Number of Interactions       | 65,377    |
| Number of Knowledge Concepts | 72        |



## Experimental Results
Comparison and ablation experiments are conducted on the CodeWorkout dataset, and it demonstrates promising results:

- **Performance**: SEGKT outperforms baseline knowledge tracing models, including classic models like BKT, DKT, GKT and programming-oriented models like CodeDKT. The model achieves high AUC scores on tasks with varied knowledge concept combinations and difficulty levels.
-  **Ablation Analysis**: To understand the contribution of each component within SEGKT, we performed ablation experiments. These experiments analyze the impact of removing specific components, such as the SENet layer, AST-based score and question difficulty. The results show that each component plays a significant role in enhancing the model’s overall accuracy and robustness, highlighting the importance of each module in the model’s architecture.


## Future Work
Currently, the code for SEGKT is not yet publicly available, as we are finalizing additional improvements and documentation. We plan to release the full experimental code in a future update, which will include:

- Experimental setup instructions to replicate results, including hardware and software requirements.
- Training and evaluation scripts for SEGKT.

## Contact
For more information, please contact the developer at yhchen_616@163.com.

