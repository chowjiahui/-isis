## Networks analysis and prediction on ISIS twitter network

---

This project utilizes the Kaggle dataset of pro-ISIS tweets collected in a period during 2014 to 2015. 

### Networks analysis

Visualizations were first done to understand behaviour of twitter users, followed by networks analysis to identify influential users. The visualizations are under the 'ISIS_tweets.ipynb' file, and are done with Gephi. I also made an interactive networks diagram, using Gephi's sigma-js plugin: 
<https://chowjiahui.github.io/ISISnetwork> 
More improvements can be done here as I have yet to reduce the borders of the nodes. 

### Prediction of tweets intent

I originally wanted to predict ISIS attacks with this data, but this was deemed unfeasible as the tweets' content were mainly centered on commentary on Middle East news, as well as sharing of propaganda. However, I thought it would be interesting to predict the intent of tweets based on the following categories: 

-  N: News. Informative in nature with statements on curent events or links to news.
- P: Propaganda. Links to ISIS news sources, or biased links.
- O: Opinion. Containing personal thoughts. Religious quotes were placed here as well as they constitute religious opinion.

I removed tweets that sounded similar (in particular, retweets to different users), extracted common n-grams, and POS tagging of tweets. NLP libraries used were: NLTK and spaCy.
Models were consistently better at distinguishing between opinion and the other categories. This was exepected, as the tone of propaganda-related tweets closely resembled that of news. Instead, I relied on a vocabulary of propaganda-related keywords. 
