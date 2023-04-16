# Search-Engine
ISNA News Search Engine is an information retrieval project implemented on the [ISNA](https://www.isna.ir/) news collected in 2021. This project is implemented in two different sections:
1. Simple Indexing
2. Vector space and tf-idf ranked based retrieval

## Simple Indexing
In this section, the documents are indexed using an inverted index. When a client enters a query, the engine searches in the index and retrieves the documents containing all the words in the query by applying an intersection on the results.

### This part of the project includes the following:
* **Document preprocessing**
  *  Normalization
  * Extracting Tokens
  * Stemming
  * Removing Stopwordswords
 
* **Positional index construction**
* **Query processing**  
Search results for:
  * Common Normal Queries
  * Boolean Queries (NOT)
  * Phrase Queries
  * Complex Combination of All Types of Queries
  * Rare Queries


* **Checking Heaps' law and Zipf's law before and after stemming and eliminating stop words**


## Indexing using vector space and tf-idf
This is a more advanced search engine that leverages the cosine similarity and vector spaces for better retrieval. The vectors for each of the documents in the dataset are created using the tf-idf calculations. The formula in depicted bellow.
<br>
![img](https://github.com/mahvash-siavashpour/mahvash-siavashpour.github.io/blob/main/assets/img/tf-idf.png?raw=true)
<br>
To reduce memory usage index elimination was applied. Moreover, for faster retrieval of the documents a champion list was used for each of the elemenets in the inverted index. The score of the relevance of each of the documents with a given query is calculated using the cosine similarity function.
<br>
![img](https://github.com/mahvash-siavashpour/mahvash-siavashpour.github.io/blob/main/assets/img/cosine.png?raw=true)
<br>

### This part of the project includes the following steps:
* **tf–idf weighting**
* **Ranking documents based on cosine similarity**
* **Speeding cosine computation by pruning**
  * Using champion list
