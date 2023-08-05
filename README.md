# Information Retrieval

> Information Retrieval is the process through which a computer system can respond to a user's query for text-based information
> on a specific topic. IR was one of the first and remains one of the most important problems in the domain of natural
> laguague processing (NLP) - [stanford cs276](https://web.stanford.edu/class/cs276/)

This repo contains tutorials covering the breadth of techniques available for IR currently.

Along with IR techniques, we will also cover:
- Techniques/metrics for evaluating IR models.
- Approximate Nearest Neighbor techniques used for indexing and searching dense vectors
     (used for many dense retrieval techniques).
- Vector databases and other relevant info.


## Tutorials

1. **Classic Information Retrieval aka "The Inverted Index"** [[Notebook](./1_classic_ir_inverted_index.ipynb)]

    IR in it's most basic form answers the question "how relevant is a given *query* for a *document*". The challenge is
    that we don't have just 1 document but potentially millions or billions of documents. So the key challenge is - how
    can we efficiently find this "needle in the haystack" or the "relevant *documents* for a *query*".

2. **Evaluation metrics** [[Notebook](./2_evaluation_metrics_ir.ipynb)]

    **Binary**: MRR, MAP@k; **Graded**: nDCG@k.
    The idea behind these evaluations is to quantitatively compare multiple IR models. Typically we have a labelled dataset where
    we have queries mapped to relvevant documents. The documents could either be graded or non-graded(binary). For example, a
    graded relevance score could be on a scale of 0-5 with 5 being the most relevant.

3.  **Dense representations and Finetuning BERT for IR / Semantic search** [[Notebook](./3_finetuning_bert_for_ir.ipynb)]

    Sparse represenation of texts using one-hot vectors is very limited. We look at ways to learn dense representations of text,
    from count based methods like LSA(TF_IDF+SVD) to Word2Vec to RNNs. Finally we look at how transformers are used in the IR
    setting.

4. **Finetuning Sentence BERT(SBERT) with Multiple Negative Ranking loss** [[Notebook](./4_finetuning_sbert_with_mnr.ipynb)]
    
    We look at a better way to finetune Bi-Encoders using MNR loss. We will need lesser data and training to achieve better
    results.

5. **Finetuning a Cross-Encoder** [[Notebook](./5_finetuning_cross_encoder.ipynb)]

    We will look at Cross-Encoders. How they differ from Bi-Encoders. How to train them and when to use them.

6. **Multilingual SBERT** [[Notebook](./6_multilingual_sbert.ipynb)]

    We see how knowledge distillation can be used to train a Multilingual Student sentence encoder using a Teacher model which has
    been finetuned for STS tasks.

7. **Unsupervised training of SBERT - TSDAE** [[Notebook](./7.1_unsupervised_training_tsdae.ipynb)]

    We finally shift our attention to unsupervised techniques to train encoders for STS tasks with no labeled data. Here we look
    into TSDAE - Using Transformer-based Sequential Denoising Auto-Encoder for Unsupervised Sentence Embedding Learning.

8. **Unsupervised training of SBERT - TSDAE (pytorch version)** [[Notebook](./7.2_unsupervised_training_tsdae_pytorch.ipynb)]

9. **Unsupervised training of SBERT - SimCSE** [[Notebook](./8_unsupervised_training_simcse.ipynb)]
    
    We will look into SimCSE, a simple contrastive learning framework that works with both unlabeled and labeled data.

10. **Unsupervised training of SBERT - GPL** [[Notebook](./9_unsupervised_training_gpl.ipynb)]

    We will look into GPL, Generative Pseudo Labeling for Unsupervised Domain Adaptation of Dense Retrieval.
