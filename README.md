# Cross-Encoder Re-Rankers and Query Expansion with an LLM
This is the final assigment of the course *Information Retrieval*.

## Objectives
1. Get acquainted with fine-tuning and evaluatingcross-encoderre-rankers.
2. Learn about ensemble methods for combining the ranking runfiles of the different cross-encoder re-rankers.
3. Learn how to implement query expansion with an LLM, with and without pseudo-relevance feedback.

## Files
*TM_Final_Project.ipynb* contains the whole code that we used to implement bias detection, while *Text_Mining__Final_Assignment_2024* is the report where we described our goals, methodology, experiments and discussed the results.

## Tasks

### Task 1
We fine-tuned three different cross-encoders: 
- *cross-encoder/ms-marco-MiniLM-L-2-v2*
- *cross-encoder/ms-marco-TinyBERT-L-2-v2*
- *distilroberta-base*

Then, we  evaluated each of the fine-tuned cross-encoder models on the 43 queries of TREC DL’19, reporting NDCG@10, Recall@100, and MAP@1000as evaluation metrics.

Fine-tuning is done in *Task1_Tuning.ipynb*, while evaluation is perfomed in *Task1_Evaluation.ipynb*.

### Task 2
We applied five ensemble methods to the three models that we have considered in the previous task and we have evaluated the effectiveness if these ensembles on NDCG@10, Recall@100, and MAP@1000.

This part was implememted in *Task2_Task3.ipynb*.

### Task 3
We selected the most effective ensemble method identified in Task 2 and applied it to all possible combinations of two models, to gain a better understanding of the strengths and weaknesses of each model and the effectiveness of the ensemble method in different scenarios.

Also this task can be found in the file *Task2_Task3.ipynb*.

### Task 4
We perfomrmed query expansion by priompting a Large Language Model (LLM): *Zephyr-7b-beta*.
We reported the effectiveness of the cross-encoder before and after query expansion for the 43 queries on NDCG@10, Recall@100, and MAP@1000.

The code for this task can be found in file *Task4.ipynb*.

### Task 5
We employed pseudo-relevance feedback to perform query expansion  with an LLM. We reported the effectiveness of the cross-encoder before and after query expansion (with PRF) for the provided 43 queries and compared it with original query, and expansion without PRF.

This task was implemented in *Task5.ipynb*


File *Information_Retrieval_Final_Project.pdf* contains the report where we explained our implementation and discussed the results obtained.
