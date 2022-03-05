# CoreIR-Software

## Experiment1.ipynb
Contains our Pyserini BM25 baseline.

## Error Analysis of BM25.ipynb
Contains our methods used to extract the 500 training queries from the matched training to qrel file. We also provide all our MRR and RR results. The python file used to find each seperate RR is eval\msmarco_passage_eval_modified.py. We also give a quick synopsis of the documents retrieved for our 2 chosen queries and corresponding relevant passage provided by the qrel file. 

## Experiment2PyseriniFailureLog.ipynb
Contains our attempt at implementing RM3 with Pyserini. Our attempt reveals that Pyserini does not yet support the msmarco index containing extra information such as document vectors. We tried to solve this through three workarounds. The first was installing the more updated developer version of Pyserini. The second was downloading the prebuilt index directly from the uwaterloo link used by anserini and lastly we tried building the index with anserini and loading it directly into the index cache. All three resulted in the same error displayed in this notebook:

JavaException: JVM exception occurred: Format version is not supported

## Experiment2g.ipynb
Contains our Anserini method for running the built in RM3 with BM25. It contains information concerding the index built, the running of improvement one on 200 test queries plus NDCG_cut extraction and running the improvement on the 500 training queries plus extraction of MRR and RR for each query. 
