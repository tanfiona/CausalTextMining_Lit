# Causal Text Mining - Literature Review
This repository documents and summarizes publications relevant to the extraction of causal relations from text. We split publications into four categories: (1) Methodology, (2) Dataset, (3) Survey, and (4) Theory. 
<br>
Pull requests or suggestions are welcome.


### 1. Methodology
| Title | Author(s) | Year | Summary | Links |
| --- | --- | --- | --- | --- |
| Text mining for causal relations | Roxana Girju and Dan Moldovan | 2002 | Authors propose a semi-automatic algorithm to find lexico-syntactic patterns that refer to the causal relation. They utilise seed noun phrases (NP) to identify *\<NP1 Verb NP2\>* patterns from news articles, and ranked the causation verbs by ambiguity and frequency. Results were validated by human annotation. Downside of their work is they only focus on explicit simple causatives (ignores resultative and instrumental causatives), and their identified causal verbs are not classified by direction (It is important to distinguish that *"A cause by B"* == "*B causes A*"). | [PDF](https://www.aaai.org/Papers/FLAIRS/2002/FLAIRS02-071.pdf) |
| Identifying predictive causal factors from news streams | Ananth Balashankar, Sunandan Chakraborty, Samuel Fraiberger, Lakshminarayanan Subramanian | 2019 | Predictive Causal Graph (PCG) measures word occurences' influence on future words. This method improves prediction error of stock price time series and allows extraction of causal pairs with temporal predictive causality, potentially useful for hypothesis testing. | [PDF](https://www.aclweb.org/anthology/D19-1238/) | Identifying predictive causal factors from news streams | Ananth Balashankar, Sunandan Chakraborty, Samuel Fraiberger, Lakshminarayanan Subramanian | 2019 | Predictive Causal Graph (PCG) measures word occurences' influence on future words. This method improves prediction error of stock price time series and allows extraction of causal pairs with temporal predictive causality, potentially useful for hypothesis testing. | [PDF](https://www.aclweb.org/anthology/D19-1238/) |
| Economic Causal-Chain Search Using Text Mining Technology | Kiyoshi Izumi and Hiroki Sakaji | 2020 | Authors extract causal chains using linguistic patterns from Japanese financial statement summaries and news articles. Classification of causal sentences were based on linear SVM. Authors also created a user interface that allows interactive edits and searches. Note: Works on Japanese texts. | [PDF](https://aclanthology.org/W19-5510.pdf), [Source](https://socsim.t.u-tokyo.ac.jp/ccs/) |
| Conditional Causal Relationships between Emotions and Causes in Texts | Xinhong Chen, Qing Li, Jianping Wang | 2020 | This paper proposes a method for the detection of a pair of emotion and cause clauses conditional on the context of the claims (1 indicates a document is conditional, 0 indicates it is not). They also manually labelled a working dataset of 561 conditional and 1524 non-conditional documents, and generate context-type and emotion-type negative examples that results in non-causal documents. For their model, they feed word embedding vectors into a BiLSTM model and encoded through concatenation, another BiLSTM or attention-based method. Two prediction heads, one for prediction with context and another for predicting causal label directly, are aggregated by prioritising direct predictions. Aggregation method improves F1 score across all three encoding methods, of which, BiLSTM was the best performing. Their results are sensitive to dataset label distribution. Note: Corpus seems to be in Chinese only.| [PDF](https://www.aclweb.org/anthology/2020.emnlp-main.252/), [Source](https://github.com/mark-xhchen/Conditional-ECPE) |
| CauseNet: Towards a Causality Graph Extracted from the Web. | Stefan Heindorf and Yan Scholten, Henning Wachsmuth, Axel-Cyrille Ngonga Ngomo, Martin Potthast | 2020 | This paper is the first to construct a large-scale knowledge graph of causal relations from the web. They collected over 11 million causal relations with an estimated extraction precision of 83% from ClueWeb12 web crawl and Wikipedia articles. Their extraction method is: (1) Using causal relations as seeds, they identified popular linguistic patterns that represent relations, filtering the pattern based onn support>=2. (2) They use the pattern to identify more sentences in corpus. (3) Subsequently, they train a BiLSTM-CRF sequence tagger to tag BIO labels to identify cause-effect noun-phrases, to construct graph. Their work excludes study of causal statements that are: implicit, cross-sentences, domain-specific and negated. | [PDF](https://papers.dice-research.org/2020/CIKM-20/heindorf_2020a_public.pdf), [Source](https://github.com/causenet-org/CIKM-20) |


### 2. Annotated Dataset
| Title | Author(s) | Year | Summary | Links |
| --- | --- | --- | --- | --- |
| Causal-TimeBank | Paramita Mirza, Rachele Sprugnoli, Sara Tonelli and Manuela Speranza | 2014 | *TBA* | [PDF](https://www.aclweb.org/anthology/W14-0702/), [Source](https://github.com/dhfbk/Causal-TimeBank) |
| AltLex | Christopher Hidey, Kathleen McKeown | 2016 | Using parallel texts from English Wikipedia and Simple Wikipedia, the authors experimented with various automatic methods to classify causal statements, with their best using bootstrapping. Other efforts involve KL-divergence to tie sentence pairs that have the same causal implication. They also use FrameNet, WordNet and VerbNet features. | [PDF](https://aclanthology.org/P16-1135.pdf), [Source](https://github.com/chridey/altlex) |
| BECauSE Corpus 2.0 | Jesse Dunietz, Lori Levin, Jaime Carbonell | 2017 | *TBA* | [PDF](https://www.aclweb.org/anthology/W17-0812/), [Source](https://github.com/duncanka/BECAUSE) |
| Penn Discourse TreeBank (PDTB) | Bonnie Webber, Rashmi Prasad, Alan Lee, Aravind Joshi | 2019 | Improvement of explicit, implicit, AltLex relations which include causal relations. There are also added sense relations annotations which include temoporal, contingency and comparison relations that are relevant.| [PDF](https://catalog.ldc.upenn.edu/docs/LDC2019T05/PDTB3-Annotation-Manual.pdf), [Source](https://catalog.ldc.upenn.edu/LDC2019T05) |
| SCITE | Zhaoning Li, Qi Li, Xiaotian Zou, Jiangtao Ren | 2021 | *TBA* | [PDF](https://arxiv.org/abs/1904.07629), [Source](https://github.com/Das-Boot/scite) |
| CausalQG | Katherine Stasaski, Manav Rathod, Tony Tu, Yunfang Xiao, Marti A. Hearst | 2021 | The authors use linguistic patterns to extract causal sentences from text (2-3 sentence span) and evaluate a portion of their dataset using crowdworkers. Next, they use ProphetNet to generate both cause and effect questions and evaluate against automatic and human methods. | [PDF](https://aclanthology.org/2021.bea-1.17.pdf), [Source](https://github.com/kstats/CausalQG) |


### 3. Survey
| Title | Author(s) | Year | Summary | Links |
| --- | --- | --- | --- | --- |
| Automatic Extraction of Causal Relations from Natural Language Texts: A Comprehensive Survey | Nabiha Asghar | 2016 | *TBA* | [PDF](https://arxiv.org/abs/1605.07895) | 
| Identification of Causal Dependencies by using Natural Language Processing - A Survey | Erika Nazaruka | 2019 | *TBA* | [PDF](https://dl.acm.org/doi/10.5220/0007842706030613) | 
| A Review of Dataset and Labeling Methods for Causality Extraction | Jinghang Xu, Wanli Zuo, Shining Liang, Xianglin Zuo | 2020 | *TBA* | [PDF](https://www.aclweb.org/anthology/2020.coling-main.133/) |
| A Survey on Extraction of Causal Relations from Natural Language Text | Jie Yang, Soyeon Caren Han, Josiah Poon | 2021 | *TBA* | [PDF](https://arxiv.org/abs/2101.06426) | 


### 4. Theory
| Title | Author(s) | Year | Summary | Links |
| --- | --- | --- | --- | --- |
| Causality - 2nd Ed | Judea Pearl | 2009 | *TBA* | [PDF](https://www.cambridge.org/core/books/causality/B0046844FAE10CBF274D4ACBDAEB5F5B) |


### 5. Talks/Lectures/Videos
Links to relevant lectures and talks:
* Judea Pearl (2012) on ["The Mechanization of Causal Inference"](https://youtu.be/iNm4nFBFmvo)
* Judea Pearl (2012) on ["The Mathematics of Cause and Effect"](https://youtu.be/IiXvpPyhMw8)
* Judea Pearl (2013) on ["The Mathematics of Causal Inference, with Reflections on Machine Learning and the Logic of Science"](https://youtu.be/zHjdd--W6o4)
* Judea Pearl & Team (2013) on ["Causes and Counterfactuals: Concepts, Principles and Tools"](https://youtu.be/d-aVKnV3bBw)
* David Sontag (2019) on ["Causal Inference"](https://ocw.mit.edu/courses/electrical-engineering-and-computer-science/6-s897-machine-learning-for-healthcare-spring-2019/lecture-videos/lecture-14-causal-inference-part-1/) for the module "Machine Learning for Healthcare"
* Elias Bareinboim (2019) on ["Causal Data Science: A general framework for data fusion and causal inference"](https://www.youtube.com/watch?v=dUsokjG4DHc&ab_channel=CausalAI)
* Elias Bareinboim (2020) on ["Causal Reinforcement Learning"](https://crl.causalai.net/)
* Elias Bareinboim (2020) on ["On the Causal Foundations of Artificial Intelligence (Explainability & Decision-Making)"](https://youtu.be/fNuMHDrh6AY)
* Brady Neal's [Youtube channel on "Causal Inference"](https://www.youtube.com/channel/UCbOJ2eEdvf2wOPrAmA72Gzg)


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
