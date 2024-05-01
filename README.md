# Named Entity Recognition with syntactic information

Named Entity Recognition (NER) is a crucial task in natural language processing (NLP) that involves identifying and classifying entities within a text into predefined categories such as names of persons, organizations, locations, dates, and more. Over the years, NER has been extensively researched, with various approaches ranging from rule-based systems to deep learning models. State-of-the-art (SOTA) NER models, especially those based on transformer architectures like BERT (Bidirectional Encoder Representations from Transformers) and its variants, have achieved remarkable performance in terms of accuracy and generalization. These models leverage pretraining on large corpora followed by fine-tuning on task-specific datasets, enabling them to capture intricate patterns in text and outperform traditional methods.

### Research Objective
Navigating vast datasets for model training can indeed pose challenges, particularly for smaller research teams. In our investigation, we sought to enhance the efficacy of modestly-sized models trained on limited datasets. Our focus lay in exploring whether augmenting these models with syntactic insights from Dependency Grammar (DG) and Head-Driven Phrase Structure Grammar (HPSG) could yield performance improvements. To conduct this experiment, we extracted syntactic features from both grammatical frameworks and juxtaposed the results against a baseline model trained on identical architecture but devoid of such syntactic cues. This comparative analysis aimed to discern the impact of syntactic information on model performance, offering insights into potentially more efficient strategies for NER in resource-constrained settings.

### Model Architecture
![image](https://github.com/nsingh475/NER_with_syntactic_information/assets/87938938/d67f723a-e2b8-44e8-b6aa-1d523cabb97e)

### Results
![image](https://github.com/nsingh475/NER_with_syntactic_information/assets/87938938/85616b69-db15-46d5-b31f-674df20d3fb1)
In terms of the main tags, both the model using DG syntactic structures and the model using HPSG syntactic structures received the same accuracy or outperformed the baseline model on both B-tags and I-tags. However, the baseline model outper formed the model using DG syntactic structures and the model using HPSG syntactic structures on O-tags. Additionally, the model using the DG syntactic structure outperformed the model using HPSGsyntactic structure across all three main tags. Finally, in terms of sub-tags, the model using the DG syntactic structure outperformed the baseline and the model using the HPSG syntactic structure across all sub-tags excluding the Time entity sub tag (tim). On the other hand, the model using the HPSGsyntactic structure received the same accuracy or underperformed against the baseline across all sub-tags except the Geographical entity sub-tag(geo). When compared against the model using the DG syntactic structure, the model using the HPSG syntactic structure underperformed across all sub-tags except the Time entity sub-tag (tim).




