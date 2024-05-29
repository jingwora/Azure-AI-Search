# Azure-AI-Search

## Features

🗏 [Choose a service tier for Azure AI Search](https://learn.microsoft.com/en-us/azure/search/search-sku-tier)

🗏 [Azure AI Search pricing](https://azure.microsoft.com/en-us/pricing/details/search/)


## Documents

🗏 [Azure AI Search client library for Python](https://learn.microsoft.com/en-us/python/api/overview/azure/search-documents-readme?view=azure-python)

🗏 [Query type](https://learn.microsoft.com/en-us/azure/search/search-query-overview)

### Price Tier and Features


| Section     |                           Feature                           |          Free          |               Basic               |           Standard S1+            |
|-------------|:-----------------------------------------------------------:|:----------------------:|:---------------------------------:|:---------------------------------:|
| Core        | Max Indexes                                                 | 3                      | 15                                | 50+                                | 
| Core        | Max Indexers                                                | 3                      | 15                                | 50+                                | 
| Core        | Max Documents                                               | 10,000                 | 1   million                       | 10   million+                      | 
| Core        | Storage                                                     | 50   MB                | 2   GB                            | 165   GB+                           | 
| Core        | Price (monthly estimate)                                    | Free                   | Starts   at $73/month             | Starts   at $245/month           | 
| Search      | Full-text Search                                            | Supported              | Supported                         | Supported                         | 
| Search      | Language and Analyzers                                      | Basic   (English only) | Full   range (multiple languages) | Full   range (multiple languages) | 
| Search      | Geospatial Search                                           | Not   supported        | Supported                         | Supported                         | 
| Search      | Autocomplete and Suggestions                                | Not   supported        | Supported                         | Supported                         | 
| Search      | Semantic Search                                             | Not   supported        | Limited   support                 | Full   support                    | 
| Search      | Vector Search                                               | Not   supported        | Not   supported                   | Supported                         | 
| Search      | Hybrid Search (combining vector   and keyword-based search) | Not   supported        | Not   supported                   | Supported                         | 
| Search      | Semantic Ranker                                             | Not   supported        | Not   supported                   | Supported                         | 
| Search      | AI Enrichment                                               | Not   supported        | Supported                         | Supported                         | 
| Security    | Basic Encryption                                            | Supported              | Supported                         | Supported                         |
| Security    | Customer-managed Encryption Keys                            | Not   supported        | Not   supported                   | Supported                         |
| Security    | IP Firewall Access                                          | Not   supported        | Supported                         | Supported                         |
| Integration | Managed Identities for Outbound   Access                    | Not   supported        | Supported                         | Supported                         |
| Integration | Private Endpoint (Azure Private   Link)                     | Not   supported        | Supported                         | Supported                         |
| Integration | Availability Zones                                          | Not   supported        | Not   supported                   | Supported                         |
| Integration | Scale out                                                   | Not   allowed          | Allowed                           | Allowed                           |
| Integration | SLA Guaranteed                                              | No                     | Yes                               | Yes                               |


### Search Method

- Summary table of the different search methods in Azure AI Search.

|  Search   Method  |                                              Description                                              |     Query Type    |       Scoring Algorithm      |                                                        Use Cases                                                        |                                                   Example Use                                                  |    Minimal Price Tier   |
|:-----------------:|:-----------------------------------------------------------------------------------------------------:|:-----------------:|:----------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|:--------------------------------------------------------------------------------------------------------------:|:-----------------------:|
| Simple   Search   | Basic   keyword search with support for fuzzy matching, wildcards, and term boosting.                 | simple            | TF/IDF   (BM25)              | Simple   keyword searches, basic filtering, partial matches.                                                            | Searching   for documents containing specific keywords.                                                        | Free   Tier             |
| Full   Search     | Advanced   query language supporting complex expressions with logical operators and   proximity.      | full              | TF/IDF   (BM25)              | Complex   searches requiring precise control over query logic and conditions.                                           | Searching   for documents with complex boolean conditions.                                                     | Free   Tier             |
| Semantic   Search | Uses   NLP to understand context and meaning of terms, providing more relevant   results.             | semantic          | Machine   Learning Models    | Enhancing   search relevance through contextual understanding and semantic ranking.                                     | Natural   language queries, finding documents based on the intent behind the search.                           | Standard   (S1)         |
| Vector   Search   | Uses   vector representations to find similar items based on proximity in a   high-dimensional space. | Custom            | Vector   Similarity (Cosine) | Finding   semantically similar documents or items, leveraging deep learning models.                                     | Searching   for documents or items similar to a given vector representation.                                   | Custom   Implementation |
| Hybrid Search     | Combines   traditional keyword search with vector-based semantic search for   comprehensive results.  | semantic + Custom | TF/IDF   (BM25)   + Vector Similarity   | Scenarios   requiring both exact keyword matches and semantic understanding to improve   search relevance and accuracy. | Combining   keyword search and vector similarity to find the most relevant documents   based on both criteria. | Standard (S1) + Custom  |


### TF/IDF (BM25)
**Description:**
- BM25 (Best Matching 25) is an advanced form of the TF/IDF ranking function used to estimate the relevance of documents based on query terms.
- TF/IDF stands for Term Frequency-Inverse Document Frequency. It is used to score the importance of a term in a document relative to its frequency across all documents.
- BM25 improves upon TF/IDF by introducing document length normalization and saturation parameters, making it more effective for information retrieval.

**How It Works:**
- **Term Frequency (TF):** Measures how frequently a term appears in a document.
- **Inverse Document Frequency (IDF):** Measures how common or rare a term is across all documents in the collection.
- **Document Length Normalization:** Adjusts the relevance score based on the length of the document to prevent bias towards longer documents.

### Vector Similarity (Cosine)
**Description:**
- Vector similarity measures the similarity between two vectors, often used to determine the similarity between documents or between a query and documents.
- Cosine similarity is a common method that calculates the cosine of the angle between two vectors, providing a similarity score between -1 and 1.

**How It Works:**
- **Vector Representation:** Text or data is transformed into vectors using techniques such as word embeddings (e.g., Word2Vec, BERT).
- **Cosine Similarity Calculation:** Computes the cosine of the angle between two vectors, which indicates how similar the two vectors are. A value of 1 means they are identical, 0 means they are orthogonal (no similarity), and -1 means they are diametrically opposite.

### Semantic Search
**Description:**
- Uses natural language processing (NLP) to understand the context and meaning of search terms. Provides more relevant search results by interpreting the intent behind the query.
- Semantic search enhances search relevance through contextual understanding and semantic ranking.

**How It Works:**
- **Natural Language Processing:** Analyzes the query to understand its context and meaning.
- **Semantic Ranking:** Ranks documents based on the semantic similarity to the query, rather than just keyword matching.
- **Extractive Answers and Captions:** Provides precise answers and highlights relevant text passages directly from the documents.

**Commonly Used Models:**
- **BERT (Bidirectional Encoder Representations from Transformers):** A transformer-based model that excels in understanding the context of words in a sentence.
- **RoBERTa (Robustly optimized BERT approach):** An optimized version of BERT that improves performance on various NLP tasks.
- **DeBERTa (Decoding-enhanced BERT with disentangled attention):** An advanced variant of BERT that enhances performance by improving the model’s ability to understand and represent language structure.


### Hybrid Search
**Description:**
- Hybrid search combines traditional keyword-based search methods (like BM25) with vector-based semantic search to leverage both exact keyword matches and contextual understanding.
- This approach enhances the relevance and accuracy of search results by considering both the precise occurrence of keywords and the semantic meaning behind them.

**How It Works:**
- **Keyword Search (BM25):** Performs traditional keyword matching and relevance scoring using the BM25 algorithm.
- **Vector Search:** Uses vector similarity techniques to find semantically similar documents based on vector representations.
- **Result Merging:** Combines the results from both searches, often re-ranking them based on a combined relevance score to produce a comprehensive set of search results.

## Tutorials

- [search-get-started-semantic](https://learn.microsoft.com/en-us/azure/search/search-get-started-semantic?tabs=python)
- [Azure AI Search sample python](https://learn.microsoft.com/en-us/azure/search/samples-python)

