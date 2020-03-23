# **Aircraft Maintenance Recommender (AiMaR)** 
## *Version 3.0*
###

***

> Developed By: **ArtifactOR Technology 智因科技**

> Composed By: **Zeyang Zhang**, ArtifactOR

> Last Modified: **23rd / Mar. / 2020**

***

### Introduction
AiMaR is an intelligent decision support system designed for aircraft maintenance engineers. It takes semi-structured fault descriptions (same as filing a fault report for standard procedure) for inputs and outputs a number of solutions generated (action, manual references, defect record references, changing components' serial number and quantities, alternative components, supportive components, etc.) based on maintenance records over the past decade.

The recommender incorporates Statistics, Natural Language Processing (NLP),  Machine Learning (in future versions), a number of data analytics techniques, as well as field knowledge and heuristics from expert, to provide a logical and scientific solution with high level of reliability, transparency and explainability to users. It could not only provide expert-level solutions to defects that are out of an engineer's expertise, but also provide proofs and references to an experienced engineer's intuition. Furthermore, an automatically generated semi-structured action could be filed directly to the reporting system, saving engineer's time from typing and checking maintenance manuals. 

The decision support system is expected to be utilized in the daily work of maintenance engineers, especially the new ones, as well as the training of apprentice. It fits in a niche where the aircraft fleet doubles it's size per year while the number of engineer in practice and engineers-to-be cannot catch the tail, let alone a long certification process of an engineer, which typically takes 3-5 years to get licensed and only then the engineer could independently change components on an aircraft.

Thus, as a strategic move, the maintenance decision support system is highly demanded in fast-growing airlines and it is expected to be able to save millions in both time and human resource costs. 

---

### Version 3 Highlights
- Self-developed word segmentation algorithm and sentence matching algorithm derived from classical models with modifications tailored to the context applied in Version 3 and proved to be better performed than previous versions 
- *Bi-Directional Maximum Match (BMM) Model* applied in word segmentation
- *Term Frequency - Inverse Document Frequency (TF-IDF)*, *Cosine Similarity*, and *Levenshetein Edit Distance* Models applied in sentence similarity computation 
- Combined scoring approaches applied: *Weighted Exact / Fuzzy Match Scoring* & *Weighted Sentence Vector Distance Computing* 
- Extend supported chapters from 1 to 4 and sub-chapters from 2 to 113
- Final score refined for comparison between solutions
- Detailed score available for transparency
- Unstructured inputs allowed
- Record dict separated into sub-chapters
- Runtime (a few seconds) and memory requirement significantly decreased
- Modular structure designed for distributed computation 

---

### Version 3 Deprecated
- Web interface suspended from release in Version 3.0 (expecting consecutive test versions starting from V.3.1)
- Textual logic inferences suspended due to unsatisfied performance in Version 3.0
- Tree-like fault classifier deprecated
- Structured fault description inputs deprecated 
- Match of stations abandoned due to lack of data
- Probability of solving based on current suggestion
- Reference records other than the most fitted one 

---

### Version 3 Dependencies

Developed based on Python 3.7 with:
- [numpy] - Version 1.16.1
- [jieba] - Version 0.42.0 *(Deprecating in Version 4)*
- [pypinyin] - Version 0.37.0
- [unicodedata2] - Version 12.1.0
- [json] - Built-In
- [copy] - Built-In
- [time] - Built-In
- [math] - Built-In

---

### Future Versions 
- Following Version 3.* will focus on testing web interfaces with frameworks and UIs from Version 2.*
- Version 4 will be built with a new web interface under HTML Bootstrap Framework as previous versions, using Flask to connect with the recommender
- Version 4 also intends to further extend supported chapters to non-frequent ones 
- Version 5 intends to add Machine Learning aspect to the recommender, by dynamically and automatically change scoring weights and parameters based on useer feedbacks
- Later versions will target on the perfection (semi-automated generation) of keywords / stopwords section, as it is the most crucial part contributing to the accuracy of the recommendation, while extending he supported chapters

---

![](https://github.com/ArtifactorZeyang/ArtifactorLogo/raw/master/ARTIFACTOR_logo_full.png)

**ArtifactOR Technology 智因科技**

***Analysed. Optimised. Realised.***
***开源节流 · 降本增效***

*Copyright Reserved. 2020*


