# Dynamics of Cross-Platform Attention to Retracted Papers

A public repository hosting the code and data for the following paper:

H. Peng, D.M. Romero, E.A. Horvát </br>
[Dynamics of Cross-Platform Attention to Retracted Papers](https://www.pnas.org/doi/10.1073/pnas.2119086119) </br>

> Retracted papers often circulate widely on social media, digital news and other websites before their official retraction. The spread of potentially inaccurate or misleading results from retracted papers can harm the scientific community and the public. Here we quantify the amount and type of attention 3,851 retracted papers received over time in different online platforms. Comparing to a set of non-retracted control papers from the same journals, with similar publication year, number of co-authors and author impact, we show that retracted papers receive more attention after publication not only on social media, but also on heavily curated platforms, such as news outlets and knowledge repositories, amplifying the negative impact on the public. At the same time, we find that posts on Twitter tend to express more criticism about retracted than about control papers, suggesting that criticism-expressing tweets could contain factual information about problematic papers. Most importantly, around the time they are retracted, papers generate discussions that are primarily about the retraction incident rather than about research findings, showing that by this point papers have exhausted attention to their results and highlighting the limited effect of retractions. Our findings reveal the extent to which retracted papers are discussed on different online platforms and identify at scale audience criticism towards them. In this context, we show that retraction is not an effective tool to reduce online attention to problematic papers.

> The data and its documentation are available in the `data` folder.


## Code documentation

* `1_Link_RetractionWatch_Altmetric.ipynb`: This notebook demonstrates the process of linking retracted papers indexed in the Retraction Watch database to the Altmetric database based on (lowercased) DOIs. The Altmetric data provide all mention posts for retracted papers.
* `2_crawl_tweets.ipynb`: We use this piece of code to collect tweets for all retracted papers. It is reused for collecting tweets for matched control papers after running `4_match_control_papers.ipynb` or `4_match_control_papers_revision.ipynb`.
* `3_create_retract_dataframe.ipynb`: This notebook creates a Pandas dataframe for retracted papers, which will be used in `6_retract_vs_control_revision.ipynb` that compares retracted papers with control papers. 
* `4_match_control_papers.ipynb`: This notebook demonstrates the process of matching control papers for retracted papers based on two variables: the journal and the publication year. This matching process is used in the initial version of our manuscript.
* `4_match_control_papers_revision.ipynb`: This is the revision of the previous notebook that matches control papers for retracted papers based on four variables: journal, publication year, number of authors, and author's log citations. 
* `5_critical_tweet_label.ipynb`: We labelled critical tweets for retracted papers and control papers (identified in the initial matching process) in this notebook. Although these control papers and their labelled tweets are not used in our final version, we decided to keep this notebook because the critical tweets for retracted papers were labelled here.
* `5_critical_tweet_label_revision.ipynb`: We labelled critical tweets for control papers identified in the revised matching process. Critical tweets for retracted papers are labelled in `5_critical_tweet_label.ipynb`.
* `6_retract_vs_control_revision.ipynb`: All analyses that compare retracted papers with control papers are presented in this notebook, which can be used to produce all figures and tables shown in the manuscript and the supplementary material. This notebook creates a pandas dataframe for control papers, and a dataframe for control papers after filtering posts that contain the "retract" keyword. Note that the pandas dataframe for retracted papers after labelling/filtering retraction-discussion posts is created in `6_retract_vs_control.ipynb` in our initial version.
