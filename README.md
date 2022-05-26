# Information Retrieval

> Information Retrieval is the process through which a computer system can respond to a user's query for text-based information
> on a specific topic. IR was one of the first and remains one of the most important problems in the domain of natural
> laguague processing (NLP) - [stanford cs276](https://web.stanford.edu/class/cs276/)

This repo contains tutorials covering the breadth of techniques available for IR.

Along with IR techniques, we will also cover:
- Techniques/metrics for evaluating IR models.
- Approximate Nearest Neighbor techniques used for indexing and searching dense vectors
     (used for many dense retrieval techniques).
- Other relevant info ...


## Tutorials

* 1 - Classic Information Retrieval aka "The Inverted Index"

    IR in it's most basic form answers the question "how relevant is a given *query* for a *document*". The challenge is
    that we don't have just 1 document but potentially millions or billions of documents. So the key challenge is - how
    can we efficiently find this "needle in the haystack" or the "relevant *documents* for a *query*".

* 2 - Evaluation metrics

    **Binary**: MRR, MAP@k; **Graded**: nDCG@k.
    The idea behind these evaluations is to quantitatively compare multiple IR models. Typically we have a labelled dataset where we have queries mapped to relvevant documents. The documents could either be graded or non-graded(binary). For example, a graded relevance score could be on a scale of 0-5 with 5 being the most relevant.

* 3 - Dense representation of words and sentences

    Sparse represenation of texts using one-hot vectors is very limited. We look at ways to learn dense representations of text, from count based methods like LSA(TF_IDF+SVD) to Word2Vec to RNNs. Finally we look at how transformers are used in the IR setting.

* 4 - Dense IR
