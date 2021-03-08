# The Inner Workings of the Models

## Partyembed

The partyembed model was designed by Rheault and Cochrane, effectively finding the ideological placement of congressional documents. It was very effective in identifying the political slant of congressional documents, and so we decided to explore whether or not we could apply this to Wikipedia. The way we made use of this model was by making use of the .issue() function— this function essentially gives similarity rankings to different years and parties within some corpora (for this purpose, we used US House data). With this, we were able to give each individual word a rating, and use the entirety of these ratings to get overall scores for Wikipedia articles.

As for the aggregate function for these ratings, we used mean. When exploring other aggregates, the distribution of the ratings on the ideological books corpus was often oddly shaped, whereas mean was relatively normally distributed.

## Gentzkow, Shapiro, and Taddy

Gentzkow, Shapiro, and Taddy writeup:
The Gentzkow, Shapiro, and Taddy model basically measures how likely it is that the speaker is a democrat/republican based on a two-word phrase (bigram) input. In order to calculate these probabilities the authors look at the comparative frequency of use of certain common bigrams in congress speeches by democratic versus republican speakers. There is a lot of nuance in the inner workings of their model, it is built on the basis of previous NLP research by one of the authors, Matt Taddy. Overall, their research is incredibly thorough and data-driven so we had high expectations for this model’s performance. The results of their model are available as a dictionary of bigram/bias score key/value pairs, which we use to generate the mean aggregate score as mentioned above. Link to their paper: https://www.brown.edu/Research/Shapiro/pdfs/politext.pdf

