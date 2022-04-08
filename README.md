
# Topic Modelling for Dutch Texts
This repository contains the code that was created as part of the MA Linguistics (Text Mining) thesis and the internship at Inspectie Leefomgeving & Transport: _"An Empirical Framework for Topic Modelling for Dutch Texts based on Newspaper Articles on Soil Pollution"_


## 
## Folders
This section describes the data and models that are found in the folders.
### Data
• _data-2010-2020.tsv_: original unpreprocessed dataset containing newspaper articles from 2010 to 2020 \
• _complete-clean-preprocessed-data-2010-2020-1.tsv_: preprocessed data\
• _Woonplaatsen_in_Nederland_2020_20122021_042012.csv_: CBS residencies with minor adaptations\
• _gold_top2vec.tsv_: documents with gold labels for annotation study\
• _human_evaluation_results.tsv_: responses of annotation study to gold label\
• _ILT-survey.tsv_: original results annotation study (straight from Google Forms)

### Embedding models
• _robbert-v2-dutch-base-finetuned-model_: Fine-tuned RobBERT model\
• _d2v.docvectors_ - Trained Doc2Vec vectors from scratch (used for BERTopic)\
• _d2v.model_  Doc2Vec Model (used for BERTopic)\
• _d2v.model.trainables.syn1.npy_: Doc2Vec trainables (used for BERTopic)\
• _d2v.model.wv.vectors.npy_: Doc2Vec word vectors (used for BERTopic)

### Evaluation
All text files contain topic coherence scores of hyperparameter tuning of each model.
### Models 
Pickle file of each model (including the different hyperparameter settings which are depicted with _X; in which X is a number. See code for exact settings.)

### Plots
Contains plots of statistics of the dataset.
### Training results
Contains a notebook containing code for masked language modelling to fine-tune RobBERT to the dataset.

## Code
All model notebooks include evaluation using topic coherence.

• _data_analysis.ipynb_: Data cleaning and statistics. Includes removal of metadata from body text \
• _Traditional Models.ipynb_: LDA & NMF, bag-of-words and TF-IDF processing\
• _Top2Vec.ipynb_: Top2Vec implementation and document semantic similarity search for annotation study\
• _BERTopic.ipynb_: BERTopic implementation using vanilla RobBERT and fine-tuned. 

• _LDASEQ.ipynb_ (unused): Code for LDA over time





## Packages

gensim       ==       4.1.2 \
latextable  \
numpy        ==       1.21.5\
pandas       ==       1.4.1\
session_info   ==     1.0.0\
spacy        ==       3.2.4\
tabulate      ==      0.8.9\
texttable     ==      1.6.4\
matplotlib    ==      3.5.1\
nltk          ==      3.5\
top2vec      ==       1.0.0\
umap         ==       0.5.2\
bertopic     ==       0.9.4\
transformers  ==      4.16.2

## License

[MIT](https://choosealicense.com/licenses/mit/)

