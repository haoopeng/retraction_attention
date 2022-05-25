(1) all_tweets_uncertain_label_revision_share.csv

This data contain all tweets that have mentioned retracted or control papers analyzed in the paper. There are 42766 rows and 5 columns, including: 
1. tid: the Tweet ID;
2. meet_heuristic: a binary variable indicating if the tweet text is considered a candidate critical tweet (contains one of the 76 criticism words) and therefore is manually labelled in terms of whether it expresses criticism about the paper's data, approach, or findings;
3. three_labels: the three labels from three indepedent human annotators. "1" means critical and "0" means uncritical; 
4. fourth_label: tweets that do not have unanimous labels among the three experts was labeled by a fourth annotator;
5. majority_vote: a binary variable indicating the final label for each tweet. "1" means critical and "0" means uncritical. Tweets with ambiguous labels are labelled as "0" here. 

(2) 
