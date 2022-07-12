
# :page_facing_up: **Paper: Expanded Lattice Embeddings for Spoken Document Retrieval on Informal Meetings**

- :point_right: Abstract:
    - In this paper, we evaluate different alternatives to process richer forms of Automatic Speech Recognition (ASR) output based on lattice expansion algorithms for Spoken Document Retrieval (SDR). Typically, SDR systems employ ASR transcripts to index and retrieve relevant documents. However, ASR errors negatively affect the retrieval performance. Multiple alternative hypotheses can also be used to augment the input to document retrieval to compensate for the erroneous one-best hypothesis. In Weighted Finite State Transducer-based ASR systems, using the n-best output (i.e. the top "n" scoring hypotheses) for the retrieval task is common, since they can easily be fed to a traditional Information Retrieval (IR) pipeline. However, the n-best hypotheses are terribly redundant, and do not sufficiently encapsulate the richness of the ASR output, which is represented as an acyclic directed graph called the lattice. In particular, we utilize the lattice's constrained minimum path cover to generate a minimum set of hypotheses that serve as input to the reranking phase of IR. The novelty of our proposed approach is the incorporation of the lattice as an input for neural reranking by considering a set of hypotheses that represents every arc in the lattice. The obtained hypotheses are encoded through sentence embeddings using BERT-based models, namely SBERT and RoBERTa, and the final ranking of the retrieved segments is obtained with a max-pooling operation over the computed scores among the input query and the hypotheses set. We present our evaluation on the publicly available AMI meeting corpus. Our results indicate that the proposed use of hypotheses from the expanded lattice improves the SDR performance significantly over the $n$-best ASR output

---
## :notebook: How to cite this work:

  - In this repo, you'll find the queries and the relevance assessments used to perform our experiments reported in the paper. If you use any of the material from this repo, the best way to refer to the work is by citing the following two works:
    - bibliography: VillatoroEtAl2022.bib
    - nocite: "@*"

  - The original paper describing how these topics were generated can be found at: Eskevich, Maria, and Gareth JF Jones. "Exploring speech retrieval from meetings using the AMI corpus." Computer Speech & Language 28.5 (2014): 1021-1044.
  

---

- :file_folder: **AMI SDR Queries**
  -These are the AMI search topics as shared by Maria Eskevich. 
  
- :file_folder: **AMI SDR Qrels**
  -These are the AMI search topics as shared by Maria Eskevich. 
