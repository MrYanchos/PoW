# Politics on Wikipedia
_An exploration of political bias in Wikipedia articles_


## Background

The ubiquity of Wikipedia and the current salience of politics encouraged us to study their impact on Wikipedia. Pew research has found that in the United States, political division is [increasing, and is most present among the most politically active](https://www.pewresearch.org/politics/2014/06/12/section-1-growing-ideological-consistency/). 

With Wikipedia being the default source for most people, this could bode poorly for the articles.

Researchers have dug into this topic before, using a variety of strategies to analyze bias. Here, we decided to take a look at a few of these strategies and compare their results, in an effort to find out the strengths of these different strategies and perhaps find locations where one strategy is more effective than another.

## Models

### _Data_

Both of our models are initially trained on congressional data. The speeches are readily associated with their political stance, and there is plenty of data to be used.

After training, our models were then validated on the Ideological Books Corpus (Sim et al., 2013) with sub-sentential annotations (Iyyer et al., 2014). This set is much smaller, but its strength comes in that it is clearly labeled with ideological position, and is *not* congressional in nature (instead sourced from books and magazines).

In doing this, we can find that the models are not limited to detecting bias in congressional material, but can generalize to broader ranges of text documents.

With these models in hand, we downloaded current pages and revision histories of political articles from Wikipedia, as it is on these documents that we intend to run these models.

### _Partyembed Model_

The partyembed model was designed by Rheault and Cochrane, effectively finding the ideological placement of congressional documents. The full paper is linked below:

Ludovic Rheault and Christopher Cochrane. 2020. [Word Embeddings for the Analysis of Ideological Placement in Parliamentary Corpora](https://ludovicrheault.weebly.com/uploads/3/9/4/0/39408253/rheaultcochrane2019_pa.pdf). Political Analysis 28(1): 112-133.

From their pre-trained models, we used one trained on United States House data. There, for any given word in the model's vocabulary, we were able to discover its overal political leanings with respect to any particular congressional year/party combination.

### _Gentzkow and Shapiro Model_

Description of G&S

### Further details of the models

[Click here to learn more](further-details.md)

## Results

### _Model Comparisons_

If we find anything interesting when comparing the models

### _Wikipedia Restuls and Their Validity_

The validity of the results on WP based on comparisons and IBC results







