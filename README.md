Correct order of application：
extract_id.py -> extract_url.py -> abstract_convert.py -> extract_sentence.py -> merged.py -> sentiment_analysis.py -> merge_title&abstract.py -> merged_title&abstract_sentiment.py -> clean.py -> predict.py

extract_id.py: extract id

clean.py: Sobering dataset, The three emotions previously processed by scibert are cleaned out, and then the DictSentiBert model is used to re mark emotions. This model is a pre training language model based on bert, which uses the text dataset, the corpus dataset, for training. In the process of processing the dataset, we first load the pre trained DcitSentibert model. In the sentiment analysis process, each sentence is first processed through a word segmentation device to convert the text into a model readable input format. Next, the model predicts the probability distribution of emotion categories (negative, neutral, positive) and calculates it using the softmax function. Select the category with the highest probability as the emotional score, and then map this score to the corresponding emotional label (negative, neutral, or positive). Each sentence will be labeled with this label and the labeled data will be saved back to the JSON file, updating the specific sentiment labels for each citation.


Partial datasets are shown in processed01, and the complete dataset reference link is: https://pan.baidu.com/s/1s0ZKq5pE8qMAfzGYw_Hj2g?pwd=8688 Extraction code: 8688
