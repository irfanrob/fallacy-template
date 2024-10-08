### Overview

We present **Flee the Flaw (FtF)**, a dataset created for representing the structure of fallacious arguments. Our dataset consists of 400 instances in total (200 dev and 200 train) split between four target fallacy types (false dilemma, faulty generalization, fallacy of credibility, false causality) taken from the LOGIC[1] dataset. Each fallacy type in our dataset consists of 100 total instances split between both sets (i.e., 50 dev and 50 train). 

### Contents

- **ftf\_dataset.csv**: Our Flee the Flaw (FtF) dataset.
- **ftf\_prompts**: Folder containing the prompts that were used for the LLM experiments.
- **ftf_guidelines.pdf**: The guidelines used for creating FtF.



### ftf_dataset.csv columns
Below, we describe the columns in `ftf_dataset.csv`.


- **split**: `dev` or `train`
- **no**: Instance number.
- **input\_text**: Fallacious argument originally provided by LOGIC[1] dataset.
- **fallacy\_type**: Fallacy type for the given `input_text`: false dilemma, faulty generalization, fallacy of credibility, false causality.
- **a\_annotator\_1**: Slot-filler (a) from the `input_text` selected by annotator 1 for their selected `template_annotator_1`.
- **a\_annotator\_2**: Slot-filler (a) from the `input_text` selected by annotator 2 for their selected `template_annotator_2`.
- **a'\_annotator\_1**: Slot-filler (a') from the `input_text` selected by annotator 1 for their selected `template_annotator_1`.
- **a'\_annotator\_2**: Slot-filler (a') from the `input_text` selected by annotator 2 for their selected `template_annotator_2`.
- **c\_annotator\_1**: Slot-filler (c) from the `input_text` selected by annotator 1 for their selected `template_annotator_1`.
- **c\_annotator\_2**: Slot-filler (c) from the `input_text` selected by annotator 2 for their selected `template_annotator_2`.
- **c'\_annotator\_1**: Slot-filler (c') from the `input_text` selected by annotator 1 for their selected `template_annotator_1`.
- **c'\_annotator\_2**: Slot-filler (c') from the `input_text` selected by annotator 2 for their selected `template_annotator_2`.
- **x\_annotator\_1**: Slot-filler (x) from the `input_text` selected by annotator 1 for their selected `template_annotator_1`.
- **x\_annotator\_2**: Slot-filler (x) from the `input_text` selected by annotator 2 for their selected `template_annotator_2`.
- **template\_annotator\_1**: Template (1-5) selected for the respective `fallacy_type` template set by annotator 1.
- **template\_annotator\_2**: Template (1-5) selected for the respective `fallacy_type` template set by annotator 2.
- **is\_arg\_consequences\_annotator\_1**: Parameter used to determine if the fallacious argument can be represented using Walton (2008)'s argument from consequence scheme. `yes` if `template_annotator_1` is 1-4, else `no`
- **is\_arg\_consequences\_annotator\_2**: Parameter used to determine if the fallacious argument can be represented using Walton (2008)'s argument from consequence scheme. `yes` if `template_annotator_2` is 1-4, else `no`

### References
[1] Zhijing Jin, Abhinav Lalwani, Tejas Vaidhya, Xiaoyu Shen, Yiwen Ding, Zhiheng Lyu, Mrinmaya Sachan, Rada Mihalcea, and Bernhard Schoelkopf. 2022. Logical fallacy detection. In Findings of the Association for Computational Linguistics: EMNLP 2022, pages 7180–7198, Abu Dhabi, United Arab Emirates. Association for Computational Linguistics.
