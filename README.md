# Information Retrieval System for Crypto-NFT 
**Crypto-NFT** - A *NFT-related* Information Retrieval Project  

The search indexer is a crucial component of a search engine, enabling efficient retrieval of relevant information based on user queries. Key components of a typical search indexer include:

1. **Crawling Engine:**
   - Function: Fetches information from databases, data structures, file systems, and websites by discovering links connecting different documents or resources.
   - Manages a URL queue, handles duplicate URLs.

2. **Document Processing:**
   - Function: Indexes retrieval information, extracts text, converts documents, and removes irrelevant content.
   - Identifies and eliminates duplicate content.

3. **Tokenization:**
   - Function: Breaks text or sequences into smaller chunks called tokens (words, phrases, or subwords).
   - Aids in understanding the text structure, analyzes and converts text into tokens for further processing.

4. **Inverted Index:**
   - Function: Data structure mapping tokens to the documents in which they appear.
   - Stores word frequency and position, facilitating fast information retrieval.

5. **Ranking and Scoring:**
   - Function: Ranks web pages based on their relevance to user queries.
   - Utilizes algorithms (e.g., TF-IDF, PageRank) to assign a score to web pages, determining their ranking in search results.
   

## Data Collection
**'1_crawling' folder**
1. scrape_tweets.ipynb
2. explore_data.ipynb  

## Data Preprocessing
**'2_preprocesing' folder**
1. preprocess_tweets.ipynb
2. prepare_files.ipynb
3. preprocessing_experiments.ipynb  

## Data Augmentation
**'3_augmentation' folder**
1. augmentation_experiments.ipynb
2. augment_train.ipynb  

## Sentiment Analysis
**'4_classification" folder**
Choosing Best-Model for Sentiment Analysis Classification
1. unsupervised_classifiers.ipynb
2. xgboost_classifier.ipynb
3. lightgbm_classifier.ipynb
4. knn_classifier.ipynb
5. svm_classifier.ipynb
6. decisiontree_classifier.ipynb
7. naivebayes_classifier.ipynb
8. majority_voting.ipynb
9. lstm_classifier.ipynb
10. bert_classifier.ipynb  

## User Interface
**'5_interface_ui' folder**  
Using Streamlit Interface to search for NFT 
*How To Install Elasticsearch*
* download and unzip `elasticsearch-8.7.0`
* in `/config/elasticsearch.yml` change lines 98 and 103 to `false`
* in `/config/roles.yml` add  
```
admins:
  cluster:
    - all
  indices:
    - names:
        - "*"
      privileges:
        - all
devs:
  cluster:
    - manage
  indices:
    - names:
        - "*"
      privileges:
        - write
        - delete
        - create_index
```
* add `\bin` folder to PATH environment variable
* open Command Prompt, `elasticsearch`
* check `localhost:9200`  
 
## Datasets
**'datasets' folder**
1. label_dataset_final.csv
2. full_dataset_final.csv
3. train_aug.csv
4. test.csv