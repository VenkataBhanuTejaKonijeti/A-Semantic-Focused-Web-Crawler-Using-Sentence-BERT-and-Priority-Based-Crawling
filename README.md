# 🕷️ Semantic Focused Web Crawler using Sentence-BERT

## 📌 Overview
The rapid growth of web content has made it difficult to retrieve topic-specific and semantically relevant webpages using traditional keyword-based crawlers. Conventional crawlers rely on lexical matching techniques such as TF-IDF and generic traversal strategies like breadth-first search, which often result in low relevance and inefficient crawling.

This project implements a **Semantic Focused Web Crawler** that leverages **Sentence-BERT (SBERT)** and **priority-based crawling** to intelligently retrieve and rank webpages related to a user-defined topic. The crawler understands the **semantic meaning** of both the query and webpage content, enabling accurate relevance estimation and efficient crawling.

---

## 🎯 Problem Statement
Traditional web crawlers depend on keyword matching and uninformed traversal strategies, leading to the retrieval of irrelevant webpages and inefficient use of crawling resources. Existing focused crawlers lack deep contextual understanding of user intent and webpage content. Therefore, there is a need for an intelligent semantic-focused crawler that can understand user queries, evaluate webpage relevance accurately, and prioritize crawling paths to retrieve topic-specific information efficiently.

---

## 🚀 Proposed Solution
The proposed system introduces a **semantic best-first crawling approach** in which:
- The user query is converted into a semantic embedding using **Sentence-BERT**
- Webpages are evaluated using **cosine similarity** between query and page embeddings
- A **priority queue (URL frontier)** is used to crawl highly relevant pages first
- Relevant webpages guide further crawling and are ranked based on semantic relevance

---

## 🏗️ System Architecture (High-Level Flow)
1. Accept user query  
2. Generate query embedding using Sentence-BERT  
3. Initialize topic-related seed URLs  
4. Insert URLs into a priority queue  
5. Fetch and preprocess webpages  
6. Generate webpage embeddings using Sentence-BERT  
7. Compute cosine similarity  
8. Filter relevant pages using a threshold  
9. Expand crawling using semantic priority  
10. Rank and display relevant webpages  

---

## 🔄 Workflow
- The crawler starts with a set of seed URLs
- Each webpage is fetched and cleaned
- Semantic similarity between query and webpage is computed
- Relevant pages are stored and used to guide crawling
- Crawling continues until the queue is empty or a crawl limit is reached
- Final output is a ranked list of topic-specific webpages

---

## 🧠 Technologies Used
- **Python**
- **Sentence-BERT (SBERT)**
- **Transformers**
- **BeautifulSoup**
- **Requests**
- **Cosine Similarity**
- **Priority Queue (heapq)
