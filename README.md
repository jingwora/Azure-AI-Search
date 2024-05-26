# Azure-AI-Search

## Features

🗏 [Choose a service tier for Azure AI Search](https://learn.microsoft.com/en-us/azure/search/search-sku-tier)

🗏 [Azure AI Search pricing](https://azure.microsoft.com/en-us/pricing/details/search/)

### Price Tier and Features

- Summary table of the different search methods in Azure AU Search.

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
|  Search   Method  |                                              Description                                              |     Query Type    |       Scoring Algorithm      |                                                        Use Cases                                                        |                                                   Example Use                                                  |    Minimal Price Tier   |
|:-----------------:|:-----------------------------------------------------------------------------------------------------:|:-----------------:|:----------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|:--------------------------------------------------------------------------------------------------------------:|:-----------------------:|
| Simple   Search   | Basic   keyword search with support for fuzzy matching, wildcards, and term boosting.                 | simple            | TF/IDF   (BM25)              | Simple   keyword searches, basic filtering, partial matches.                                                            | Searching   for documents containing specific keywords.                                                        | Free   Tier             |
| Full   Search     | Advanced   query language supporting complex expressions with logical operators and   proximity.      | full              | TF/IDF   (BM25)              | Complex   searches requiring precise control over query logic and conditions.                                           | Searching   for documents with complex boolean conditions.                                                     | Free   Tier             |
| Semantic   Search | Uses   NLP to understand context and meaning of terms, providing more relevant   results.             | semantic          | Machine   Learning Models    | Enhancing   search relevance through contextual understanding and semantic ranking.                                     | Natural   language queries, finding documents based on the intent behind the search.                           | Standard   (S1)         |
| Vector   Search   | Uses   vector representations to find similar items based on proximity in a   high-dimensional space. | Custom            | Vector   Similarity (Cosine) | Finding   semantically similar documents or items, leveraging deep learning models.                                     | Searching   for documents or items similar to a given vector representation.                                   | Custom   Implementation |
| Hybrid Search     | Combines   traditional keyword search with vector-based semantic search for   comprehensive results.  | semantic + Custom | BM25   + Vector Similarity   | Scenarios   requiring both exact keyword matches and semantic understanding to improve   search relevance and accuracy. | Combining   keyword search and vector similarity to find the most relevant documents   based on both criteria. | Standard (S1) + Custom  |

## Documents

🗏 [Azure AI Search client library for Python](https://learn.microsoft.com/en-us/python/api/overview/azure/search-documents-readme?view=azure-python)

🗏 [Query type](https://learn.microsoft.com/en-us/azure/search/search-query-overview)

