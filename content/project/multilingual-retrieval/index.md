---
title: "Multilingual Dense Retrieval with Mixed-Language Queries"

summary: "Understanding when mixing query embeddings improves multilingual search."
abstract: "We study how multilingual dense retrieval responds to queries that combine languages. By interpolating embeddings of parallel query translations, we control the mixing ratio across 35 language pairs and three document-language settings on mMARCO. With BGE-M3, the best tested mixture improves over both monolingual endpoints in 88 of 105 settings. The results reveal an asymmetry around English and show how document language and linguistic distance shape the benefits of mixing."

tags: ["Information Retrieval", "Multilingual NLP", "Dense Retrieval"]
year: 2026
date: '2026-07-01'
all_day: true
featured: true
image:
  caption: 'Encode parallel query translations, interpolate and normalize their embeddings, then retrieve from a shared document index.'
  focal_point: Center
url_pdf: 'https://aclanthology.org/2026.acl-long.1455.pdf'
url_code: 'https://github.com/tongyao-zhu/query-embedding-mix'
authors: ["tongyao", "chaoming", "min"]

---
Multilingual users often combine languages when searching, yet retrieval models are usually evaluated with queries written in a single language. In this project, we investigate when combining languages helps dense retrieval. Our ACL 2026 oral paper, [When Does Mixing Help?](https://aclanthology.org/2026.acl-long.1455/), introduces a controlled study that interpolates the embeddings of parallel query translations. Across 35 language pairs and three document-language settings on mMARCO, the best tested mixture outperforms both monolingual endpoints in 88 of 105 BGE-M3 settings. English plays an asymmetric role: it is a strong mixing partner for retrieving non-English documents, while collections containing English generally favor pure English queries. We also find that mixing gains decrease with typological distance after accounting for English dominance. These findings help explain how query and document languages interact in multilingual search.

This project brings together Tongyao Zhu, a WING doctoral student studying information retrieval and language models, Chao-Ming Huang, whose final-year project examined information retrieval in code-mixed contexts, and Prof. Min-Yen Kan. Tongyao and Chao-Ming contributed equally to the paper. Their collaboration turns the practical challenge of multilingual search into a reproducible study of query representations, with released code, results, and analysis tools supporting further investigation.
