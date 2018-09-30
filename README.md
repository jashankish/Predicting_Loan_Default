
***CLean P2P lending data, identify useful features in data, define a machine learning model, and apply models to data***

I wanted to design my code such that I could improve the logistic regressions for the “true predictions” (1/1) as much as possible.

**Improvement #1:**
My first improvement was focused on better use of the “emp_title” feature provided by those looking for a loan.
I then appended the existing DataFrame with this new list using “df['noJobProvided'] = noJobListed” and incorporated it into my model as a feature accordingly. With this additional code, the confidence matrices experienced the following marginal improvements:

**Improvement #2:**
My second major improvement was focused on the “title” data provided. The idea being that if there were suspicious or “risky” words in the reasoning for the loan, they may be more likely to “charge-off”. Despite being a relatively simple implementation of this concept with just a handful of key words, the logistic regression for “True” values improved significantly while the random forest classifier still exhibited a greater degree of accuracy relative to the original.

**Suggestions for Additional Improvements:**
When thinking of ways to improve the model, several ideas come to mind but I still believe the “title” information is highly under-utilized. I would suggest creating a list of the most commonly used words in loan requests that have eventually charged-off. Depending on their significance, each word could be given a score and used to improve the model for future loan requests. Furthermore, a list containing every word in a standard dictionary could be used to identify spelling errors used in loan requests. Though my elementary implementation leveraging the “title” information significantly improved the model, I believe there is still a lot of value in parsing and analyzing the reasoning behind each loan request.
