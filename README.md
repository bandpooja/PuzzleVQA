# PuzzleVQA
Given a visual puzzle, the goal is to leverage vision-language models (VLMs) to analyze the image, apply reasoning to understand patterns, relationships, and logical rules, and select the correct answer from the provided options. For this we have used PuzzleVQA dataset.

[PuzzleVQA dataset](https://github.com/declare-lab/LLM-PuzzleTest/tree/master)


**Question:** What is the missing number of the part denoted with a question mark?

**Options:**  
- [7, 9, 1, 5]

![Alt text](https://github.com/declare-lab/LLM-PuzzleTest/raw/master/PuzzleVQA/data/images/grid_number/grid_number_0000.png)

## Observations on Model Performance

[](result.png)

We tested four models—**Gemma**, **Llama**, **Qwen**, and **Pixtral**—to evaluate their performance both **without fine-tuning** and **after fine-tuning** on **20 samples**. Below are the results:

| Model   | Answer without Fine-tuning | Answer after Fine-tuning |
|---------|----------------------------|--------------------------|
| Gemma   | 12                         | 18                       |
| Llama   | 10                         | 15                       |
| Qwen    | 9                          | 14                       |
| Pixtral | 5                          | 12                       |

### Performance Analysis

1. **Gemma-3**:
   - Gemma shows the highest improvement in performance after fine-tuning, with a score increase from **12** to **18**.
   - This indicates that Gemma benefits significantly from fine-tuning, suggesting that it adapts well to the specific task or dataset.

2. **Llama-3.2**:
   - Llama also shows a notable increase in performance, from **10** to **15**.
   - Although the improvement is substantial, it is slightly less than that of Gemma, but still indicates the positive effect of fine-tuning.

3. **Qwen**:
   - Qwen demonstrates a moderate improvement, moving from **9** to **14**.
   - This suggests that Qwen, while benefiting from fine-tuning, may not perform as effectively as Gemma and Llama on this particular task.

4. **Pixtral**:
   - Pixtral shows the lowest performance both before and after fine-tuning, with a score of **5** without fine-tuning and **12** after fine-tuning.
   - Although Pixtral does show an improvement, it still lags behind the other models, indicating it may need more data or adjustments to improve performance significantly.

   **Additionaly** requires fewer training steps to learn effectively—only **100 steps**, compared to the other models that require at least **200 steps**. This indicates that Gemma is more efficient in terms of learning and adapting to new data.

### Conclusion

- **Gemma** outperforms the other models both in raw score and in improvement after fine-tuning, making it the most effective choice for this task.
- **Fine-tuning** generally leads to improved performance across all models, confirming that adapting the models to the specific dataset or task is crucial for boosting their accuracy and relevance.
