# Dynamics of Cross-Platform Attention to Retracted Papers

A public repository hosting the code and data for the following paper:

H. Peng, D.M. Romero, E.A. Horvát </br>
[Dynamics of Cross-Platform Attention to Retracted Papers](https://arxiv.org/abs/2110.07798) </br>

## Code documentation

* `1_Link_RetractionWatch_Altmetric.ipynb`: This notebook demonstrates the process of linking retracted papers to the Altmetric database based on (lowercased) DOIs. The Altmetric data provides all mention posts for retracted papers.
* `2_crawl_tweets.ipynb`: We use this code to collect tweets for all retracted papers. It is reused for collecting tweets for matched control papers after running `4_match_control_papers.ipynb`.
* `3_create_retract_dataframe.ipynb`: This notebook creates a Pandas dataframe for retracted papers, which will be used in `6_retract_vs_control_revision.ipynb` that compares retracted papers with control papers. 
* `4_match_control_papers.ipynb`: This notebook demonstrates the process of matching control papers for retracted papers based on two variables: the journal and publication year. This matching process is used in the initial version of our manuscript.
* `4_match_control_papers_revision.ipynb`: This is the revision of the previous code that matches control papers for retracted papers based on four variables: journal, publication year, number of authors, and author's log citations. 
* `5_critical_tweet_label.ipynb`: We labelled critical tweets for retracted papers and control papers (our initial matching scheme).
* `5_critical_tweet_label_revision.ipynb`: We labelled critical tweets for control papers identified in the revised matching process. Critical tweets for retracted papers are labelled in `5_critical_tweet_label.ipynb`.
* `6_retract_vs_control_revision.ipynb`: All analyses that compare retracted papers with control papers are presented in this notebook, which can be used to produce all figures and tables shown in the manuscript and the supplementary material. This notebook creates a pandas dataframe for control papers, and a dataframe for control papers after filtering posts that contain the "retract" keyword. The pandas dataframe for retracted papers after labelling/filtering retraction-discussion posts is created in `6_retract_vs_control.ipynb`.
