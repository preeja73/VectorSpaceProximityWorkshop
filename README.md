# 🧠 Vector Space Proximity Workshop

## 📚 Overview

This workshop introduces foundational Natural Language Processing (NLP)
concepts and builds toward **Vector Space Proximity** and **Information
Retrieval (IR) evaluation**.

Students implement:

-   Term-Document Incidence Matrix\
-   Term Frequency (TF)\
-   Log Frequency Weighting\
-   Document Frequency (DF)\
-   Inverse Document Frequency (IDF)\
-   TF-IDF\
-   Cosine Similarity

These are then used to:

-   Retrieve documents based on similarity\
-   Evaluate retrieval systems using IR metrics

------------------------------------------------------------------------

## 🎯 Learning Objectives

By the end of this workshop, students will be able to:

-   Represent text as vectors using TF-IDF\
-   Compute similarity using cosine similarity\
-   Build a basic retrieval system\
-   Evaluate IR systems using:
    -   Precision, Recall, F1\
    -   Precision@K\
    -   Average Precision (AP)\
    -   Mean Reciprocal Rank (MRR)\
-   Understand relevance vs keyword matching\
-   Connect classical IR to modern AI systems

------------------------------------------------------------------------

## 🧪 Hands-On Components

Students will:

-   Build a preprocessing pipeline:
    -   Tokenization\
    -   Normalization\
    -   Stop-word removal\
    -   Stemming
-   Implement from scratch:
    -   Incidence Matrix\
    -   TF and Log TF\
    -   DF and IDF\
    -   TF-IDF
-   Compute:
    -   Cosine similarity\
    -   Ranked retrieval
-   Evaluate:
    -   Confusion matrix\
    -   Precision, Recall, F1\
    -   Precision@K\
    -   Average Precision (AP)\
    -   Mean Reciprocal Rank (MRR)\
    -   Kappa (inter-judge agreement)

------------------------------------------------------------------------

## 📁 Dataset Description

This project uses the **20 Newsgroups** corpus (via `scikit-learn`) for
large-scale text retrieval experiments. The dataset contains thousands of
documents across multiple categories, making it suitable for building and
evaluating TF-IDF + cosine similarity retrieval pipelines.

## 👥 Team Members

-   Preeja Anilal
-   Anthony Izevbokun
-   Minh Thuan

## 🔗 Dataset Link and License

-   Dataset source: [20 Newsgroups
    Dataset](https://scikit-learn.org/stable/datasets/real_world.html#newsgroups-dataset)
-   Access method: `sklearn.datasets.fetch_20newsgroups`
-   License/terms: Refer to the dataset notes in scikit-learn documentation and
    original source notices linked there.

## 🧭 Retrieval Approach Summary

The retrieval system follows a classical vector-space workflow:

1.  Preprocess text (tokenization, normalization, stop-word removal, optional
    stemming/lemmatization).
2.  Build representations (binary incidence, TF, DF, IDF, TF-IDF).
3.  Convert queries to vectors and rank documents using **cosine similarity**.
4.  Evaluate relevance using **Precision, Recall, F1, Precision@K, AP, and
    MRR**, with emphasis on information need rather than simple keyword overlap.

------------------------------------------------------------------------

## 🔍 Relevance to RAG (Retrieval-Augmented Generation)

This workshop focuses on the **retrieval layer** of modern AI systems.

### Classical IR → Modern AI

  Classical IR         Modern Systems
  -------------------- ----------------
  TF-IDF               Embeddings
  Cosine Similarity    Vector Search
  Document Retrieval   RAG

### RAG Pipeline Connection

1.  Represent documents as vectors\
2.  Represent query as vector\
3.  Compute similarity (vector proximity)\
4.  Retrieve top-k documents\
5.  Pass to LLM for generation

This workshop focuses on steps **1--4**.

------------------------------------------------------------------------

## 🏗️ Example Use Case

Travel Information Retrieval System:

-   Query: *"Is there an evening bus to Toronto?"*\
-   System:
    -   Convert query to vector\
    -   Compare with document vectors\
    -   Retrieve most relevant schedules

------------------------------------------------------------------------

## ⚖️ Key Takeaways

-   Vector space proximity is the **foundation of retrieval systems**\
-   TF-IDF balances **local importance** and **global rarity**\
-   Cosine similarity enables **semantic matching**\
-   Evaluation must be based on **information need**, not keywords

------------------------------------------------------------------------

## 🚀 Next Steps

-   Replace TF-IDF with embeddings\
-   Use vector databases (FAISS, Chroma)\
-   Build full RAG pipelines\
-   Integrate with LLMs

------------------------------------------------------------------------

## 👨‍🏫 Instructor Notes

This workshop is designed for:

-   Entry-level ML/NLP students\
-   Hands-on, code-first learning\
-   Progression from math → implementation → evaluation

Emphasis is placed on:

> Understanding **why retrieval works** before moving to modern AI
> systems.
