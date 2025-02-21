---
title: "STAT: Shrinking Transformers After Training"
collection: publications
category: preprint
permalink: /publication/STAT-shrinking-transformers-after-training
excerpt: 'We present STAT: a simple algorithm to prune transformer models without any fine-tuning. STAT eliminates both attention heads and neurons from the network, while preserving accuracy by calculating a correction to the weights of the next layer.'
date: 2024-05-29
venue: 'arXiv'
paperurl: 'https://arxiv.org/pdf/2406.00061'
citation: 'STAT: Shrinking Transformers After Training. M Flynn, A Wang, DE Alvarez, C De Sa, A Damle - arXiv preprint arXiv:2406.00061, 2024'
---

We present STAT: a simple algorithm to prune transformer models without any fine-tuning. STAT eliminates both attention heads and neurons from the network, while preserving accuracy by calculating a correction to the weights of the next layer. Each layer block in the network is compressed using a series of principled matrix factorizations that preserve the network structure. Our entire algorithm takes minutes to compress BERT, and less than three hours to compress models with 7B parameters using a single GPU. Using only several hundred data examples, STAT preserves the output of the network and improves upon existing gradient-free pruning methods. It is even competitive with methods that include significant fine-tuning. We demonstrate our method on both encoder and decoder architectures, including BERT, DistilBERT, and Llama-2 using benchmarks such as GLUE, Squad, WikiText2.