# TOPSIS for Pre-trained Model Comparison on Text Summarization

This project applies the TOPSIS (Technique for Order of Preference by Similarity to Ideal Solution) method to compare the performance of three pre-trained text summarization models using evaluation metrics like ROUGE and BLEU scores.

## Models Used

The following pre-trained text summarization models were evaluated:

- **facebook/bart-large-cnn**
- **google/pegasus-xsum**
- **t5-small**

## Evaluation Metrics

The models were evaluated using the following metrics:

- **ROUGE-1**: Measures the overlap of unigrams between the generated and reference summaries.
- **ROUGE-2**: Measures the overlap of bigrams between the generated and reference summaries.
- **ROUGE-L**: Measures the longest common subsequence between the generated and reference summaries.
- **BLEU Score**: Measures the precision of n-grams in the generated summary compared to reference summaries.

## Results

### Evaluation Metrics

| Model                    | ROUGE-1 | ROUGE-2 | ROUGE-L | BLEU Score | TOPSIS Rank |
|--------------------------|---------|---------|---------|------------|-------------|
| facebook/bart-large-cnn   | 0.31    | 0.11    | 0.24    | 0.21       | 1           |
| google/pegasus-xsum       | 0.30    | 0.12    | 0.23    | 0.23       | 2           |
| t5-small                  | 0.12    | 0.02    | 0.11    | 0.08       | 3           |

### Results Summary

From the table above, we can observe the following:

- **facebook/bart-large-cnn** achieved the highest ROUGE and BLEU scores, ranking 1st according to the TOPSIS method.
- **google/pegasus-xsum** performed slightly worse but still outperformed **t5-small**, with a rank of 2nd.
- **t5-small** scored the lowest across all metrics, thus ranking 3rd in the comparison.

### Note

The values above are based on the test data provided. Actual results may vary depending on the specific input text used for summarization.

## Conclusion

This analysis highlights the relative performance of different pre-trained models for text summarization using the TOPSIS method. Based on the evaluation metrics, **facebook/bart-large-cnn** is the most suitable model for text summarization, followed by **google/pegasus-xsum**, with **t5-small** being the least effective.