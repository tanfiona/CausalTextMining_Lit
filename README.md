# Causal Text Mining - Literature Review
This repository documents and summarizes publications relevant to the extraction of causal relations from text. We split publications into four categories: (1) Methodology, (2) Dataset, (3) Survey, and (4) Theory. 
<br>
Pull requests or suggestions are welcome.

### 1. Methodology
| Title | Author(s) | Year | Summary | Links |
| --- | --- | --- | --- | --- |
| Text mining for causal relations | Roxana Girju and Dan Moldovan | 2002 | Abstract: Given a semantic relation, the automatic extraction of linguistic patterns that express that relation is a rather difficult problem. This paper presents a semi-automatic method of discovering generally applicable lexico-syntactic patterns that refer to the causal relation. The patterns are found automatically, but their validation is done semi-automatically | [PDF](https://www.aaai.org/Papers/FLAIRS/2002/FLAIRS02-071.pdf) |
| Identifying predictive causal factors from news streams | Ananth Balashankar, Sunandan Chakraborty, Samuel Fraiberger, Lakshminarayanan Subramanian | 2019 | Predictive Causal Graph (PCG) measures word occurences' influence on future words. This method improves prediction error of stock price time series and allows extraction of causal pairs with temporal predictive causality, potentially useful for hypothesis testing. | [PDF](https://www.aclweb.org/anthology/D19-1238/) | Identifying predictive causal factors from news streams | Ananth Balashankar, Sunandan Chakraborty, Samuel Fraiberger, Lakshminarayanan Subramanian | 2019 | Predictive Causal Graph (PCG) measures word occurences' influence on future words. This method improves prediction error of stock price time series and allows extraction of causal pairs with temporal predictive causality, potentially useful for hypothesis testing. | [PDF](https://www.aclweb.org/anthology/D19-1238/) |
| Conditional Causal Relationships between Emotions and Causes in Texts | Xinhong Chen, Qing Li, Jianping Wang | 2020 | This paper proposes a method for the detection of a pair of emotion and cause clauses conditional on the context of the claims (1 indicates a document is conditional, 0 indicates it is not). They also manually labelled a working dataset of 561 conditional and 1524 non-conditional documents, and generate context-type and emotion-type negative examples that results in non-causal documents. For their model, they feed word embedding vectors into a BiLSTM model and encoded through concatenation, another BiLSTM or attention-based method. Two prediction heads, one for prediction with context and another for predicting causal label directly, are aggregated by prioritising direct predictions. Aggregation method improves F1 score across all three encoding methods, of which, BiLSTM was the best performing. Their results are sensitive to dataset label distribution. Note: Corpus seems to be in Chinese only.| [PDF](https://www.aclweb.org/anthology/2020.emnlp-main.252/), [Source](https://github.com/mark-xhchen/Conditional-ECPE) |

### 2. Dataset
| Title | Author(s) | Year | Summary | Links |
| --- | --- | --- | --- | --- |
| Causal-TimeBank | Paramita Mirza, Rachele Sprugnoli, Sara Tonelli and Manuela Speranza | 2014 | *TBA* | [PDF](https://www.aclweb.org/anthology/W14-0702/), [Source](https://github.com/dhfbk/Causal-TimeBank) |
| BECauSE Corpus 2.0 | Jesse Dunietz, Lori Levin, Jaime Carbonell | 2017 | *TBA* | [PDF](https://www.aclweb.org/anthology/W17-0812/), [Source](https://github.com/duncanka/BECAUSE) |
| SCITE | Zhaoning Li, Qi Li, Xiaotian Zou, Jiangtao Ren | 2021 | *TBA* | [PDF](https://arxiv.org/abs/1904.07629), [Source](https://github.com/Das-Boot/scite) |


### 3. Survey
| Title | Author(s) | Year | Summary | Links |
| --- | --- | --- | --- | --- |
| Automatic Extraction of Causal Relations from Natural Language Texts: A Comprehensive Survey | Nabiha Asghar | 2016 | *TBA* | [PDF](https://arxiv.org/abs/1605.07895) | 
| Identification of Causal Dependencies by using Natural Language Processing - A Survey | Erika Nazaruka | 2019 | *TBA* | [PDF](https://dl.acm.org/doi/10.5220/0007842706030613) | 
| A Review of Dataset and Labeling Methods for Causality Extraction | Jinghang Xu, Wanli Zuo, Shining Liang, Xianglin Zuo | 2020 | *TBA* | [PDF](https://www.aclweb.org/anthology/2020.coling-main.133/) |
| A Survey on Extraction of Causal Relations from Natural Language Text | Jie Yang, Soyeon Caren Han, Josiah Poon | 2021 | *TBA* | [PDF](https://arxiv.org/abs/2101.06426) | 

### 4. Theory



### A. Remarks
* *TBA*: To be added 
* If you have any concerns or questions, feel free to contact me at [tan.f@u.nus.edu].


```
@misc{FionaCausalLit2021,
  author = {Tan, Fiona Anting},
  title = {Causal Text Mining Literature Review},
  year = {2021},
  publisher = {GitHub},
  journal = {GitHub repository},
  howpublished = {\url{https://github.com/tanfiona/CausalTextMining_Lit}}
}
```
