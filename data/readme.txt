(1) all_tweets_uncertain_label_revision_share.csv

This file contains all tweets that have mentioned retracted or control papers analyzed in the paper. There are 42766 rows and 5 columns, including: 
1. tid: the Tweet ID;
2. meet_heuristic: a binary variable indicating if the tweet text is considered a candidate critical tweet (contains one of the 76 criticism words) and therefore is manually labelled in terms of whether it expresses criticism about the paper's data, approach, or findings;
3. three_labels: the three labels from three indepedent human annotators. "1" means critical and "0" means uncritical; 
4. fourth_label: tweets that do not have unanimous labels among the three experts was labeled by a fourth annotator;
5. majority_vote: a binary variable indicating the final label for each tweet. "1" means critical and "0" means uncritical. Tweets with ambiguous labels are treated as uncritical here. 

(2) label_after_ret_posts_notification.csv

This file contains after-retraction posts (on news media, blogs, and wikipedia) that did not contain the "retract" keyword and were manually labelled as either discussing the retraction or not, based on the title and summary of each post. There are 734 rows and 4 columns including, "post_url" (the url of each post), "platform" (the platform where each post comes from), "paper_doi" (the doi of the mentioned paper), "is_retraction_related" ("1" means yes, "0" means no, "-1" means no content information is available for making a decision). Note that many of the posts are no longer assessible via the url. We relied on the title and summary of the post provided in the Altmetric database.

(3) label_after_ret_tweets.csv

This file is similar to "label_after_ret_posts_notification.csv", but for tweets. There are 3193 rows and 4 columns including, "tid" (Tweet ID), "paper_doi" (the doi of the mentioned paper), "posted_on" (timestamp of each tweet), and "is_retraction_related" ("1" means yes). Note that we used the tweet text in the labelling process, which is not shared here due to the data agreement with Twitter. The tweet content can be retrieved using Twitter API with the "tid".

(4) 
