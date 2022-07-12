
# :page_facing_up: **Expanded Lattice Embeddings for Spoken Document Retrieval on Informal Meetings**

- :point_right: Abstract:
    - In this paper, we evaluate different alternatives to process richer forms of Automatic Speech Recognition (ASR) output based on lattice expansion algorithms for Spoken Document Retrieval (SDR). Typically, SDR systems employ ASR transcripts to index and retrieve relevant documents. However, ASR errors negatively affect the retrieval performance. Multiple alternative hypotheses can also be used to augment the input to document retrieval to compensate for the erroneous one-best hypothesis. In Weighted Finite State Transducer-based ASR systems, using the n-best output (i.e. the top "n" scoring hypotheses) for the retrieval task is common, since they can easily be fed to a traditional Information Retrieval (IR) pipeline. However, the n-best hypotheses are terribly redundant, and do not sufficiently encapsulate the richness of the ASR output, which is represented as an acyclic directed graph called the lattice. In particular, we utilize the lattice's constrained minimum path cover to generate a minimum set of hypotheses that serve as input to the reranking phase of IR. The novelty of our proposed approach is the incorporation of the lattice as an input for neural reranking by considering a set of hypotheses that represents every arc in the lattice. The obtained hypotheses are encoded through sentence embeddings using BERT-based models, namely SBERT and RoBERTa, and the final ranking of the retrieved segments is obtained with a max-pooling operation over the computed scores among the input query and the hypotheses set. We present our evaluation on the publicly available AMI meeting corpus. Our results indicate that the proposed use of hypotheses from the expanded lattice improves the SDR performance significantly over the $n$-best ASR output

---
## :notebook: How to cite this work:

  - In this repo, you'll find the queries and the relevance assessments used to perform our experiments reported in the paper. If you use any of the material from this repo, the best way to refer to the work is by citing the following two works:
    ```@inproceedings{10.1145/3477495.3531921,
    author = {Villatoro-Tello, Esa\'{u} and Madikeri, Srikanth and Motlicek, Petr and Ganapathiraju, Aravind and Ivanov, Alexei V.},
    title = {Expanded Lattice Embeddings for Spoken Document Retrieval on Informal Meetings},
    year = {2022},
    isbn = {9781450387323},
    publisher = {Association for Computing Machinery},
    address = {New York, NY, USA},
    url = {https://doi.org/10.1145/3477495.3531921},
    doi = {10.1145/3477495.3531921},
    booktitle = {Proceedings of the 45th International ACM SIGIR Conference on Research and Development in Information Retrieval},
    pages = {2669–2674},
    series = {SIGIR '22}
    }'''
    
  - The original paper describing how these topics can be found at
    
    ```@article{ESKEVICH20141021,
    title = {Exploring speech retrieval from meetings using the AMI corpus},
    journal = {Computer Speech & Language},
    volume = {28},
    number = {5},
    pages = {1021-1044},
    year = {2014},
    issn = {0885-2308},
    doi = {https://doi.org/10.1016/j.csl.2013.12.005},
    url = {https://www.sciencedirect.com/science/article/pii/S0885230813001186},
    author = {Maria Eskevich and Gareth J.F. Jones},
    }'''
  

---
## :gift:

- :file_folder: **[AMI SDR Test Queries](https://github.com/villatoroe/AMI_SDR_Queries/blob/main/queries/queries_25_AMI_testSet_TREC_format.txt)**
  
- :file_folder: **[AMI SDR Qrels](https://github.com/villatoroe/AMI_SDR_Queries/blob/main/qrels/AMI_qrels.txt)**
