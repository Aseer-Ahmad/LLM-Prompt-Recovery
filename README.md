# LLM-Prompt-Recovery
https://www.kaggle.com/competitions/llm-prompt-recovery
Overview
LLMs are commonly used to rewrite or make stylistic changes to text. The goal of this competition is to recover the LLM prompt that was used to transform a given text.
NLP workflows increasingly involve rewriting text, but there's still a lot to learn about how to prompt LLMs effectively. This machine learning competition is designed to be a novel way to dig deeper into this problem.

The challenge: recover the LLM prompt used to rewrite a given text. You’ll be tested against a dataset of 1300+ original texts, each paired with a rewritten version from Gemma, Google’s new family of open models.

Evaluation Metric
For each row in the submission and corresponding ground truth, sentence-t5-base is used to calculate corresponding embedding vectors. The score for each predicted / expected pair is calculated using the Sharpened Cosine Similarity, using an exponent of 3. The SCS is used to attenuate the generous score given by embedding vectors for incorrect answers. Do not leave any rewrite_prompt blank as null answers will throw an error.


Dataset Description
The competition dataset comprises text passages that have been rewritten by the Gemma 7b-it LLM with undisclosed prompts. The goal of the competition is to determine what prompts were used.

Please note that this is a Code Competition. When your submission is scored, this example test data will be replaced with the full test set. Expect roughly 1,400 original texts in the test set.

Files
[train/test].csv

id - A unique identifier for the row.
original_text - The prompt the essay was written in response to.
rewrite_prompt - The target column. The prompt provided to Gemma.
rewritten_text - The output from Gemma.
sample_submission.csv A submission file in the correct format.

id
rewrite_prompt
Notes
Only one example is provided in both train.csv and test.csv
You should generate additional data to train your model against (example)
