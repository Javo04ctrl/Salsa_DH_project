---
layout: page
title: Lyrics Analysis
author: Javier Machado
---
For the Analysis of the lyrics of the songs in the dataset, I needed a tool that worked efficiently with the spanish language. The tool that apparently worked is called SpaCy. This tool analizes text word by word and can categorize words into their own category such as nouns, verbes and adjectives as well as define the entity of each word, for example “Héctor Lavoe” PERS..
I used this tool to test Spanish text with a simple Spanish sentence about Salsa.

## Test sentence.PNG
![Test_sentence.PNG](assets/images/Test_sentence.PNG)
For this simple sentence, I noticed that some of the results were accurate, but others weren’t at all.


## Words test.PNG

![Words test.PNG](assets/images/Words_test.PNG)

Some words were noted as proper names when they weren’t; some were labelled as nouns when they were in reality verbs. this means that I couldn’t trust SpaCy with a pertinent analysis because it seemed to show some biases towards English and Spanish and mixed the meaning of the words of both languages.
That can be appreciated with words such as “era” which is a verb but is categorized as a noun, maybe referring to the word “era” as division of time. Another example is the word “un” which is an indefinite article but is recognized as a proper name, probably referring to the “UN” as United Nations.

I decided to create a word cloud with all the lyrics of the songs in the dataset. After a thoughtful reflection I decided to include the following stopwords:
## Stopwords.PNG

![Stopwords.PNG](assets/images/Stopwords.PNG)

Which are words that if not excluded, appear too often and most of them are not keywords nor contribute to a pertinent word cloud about the topic of Salsa. There was a consideration to remove words such as “La-la”, “Le-le”,“Oh-oh”,“Ay” and others but some of those interjections and onomatopeic expressions are relevant for the word cloud in my opinion because those are part of the style of performance of the singers and some of them use those as a signature singing style, so I thought it would be fair to leave them on the word cloud. This decision gives specific identity to some words in the word cloud. Such as the “La-la” and “Le-le” which are for example part of Héctor Lavoe’s style of performing or other words such as “Quimbara” which have African origin and are said by Celia Cruz.

## original_wordcloud.png 

![original_wordcloud.png](assets/images/original_wordcloud.png)

The Dataset was also analyzed on sentiment analysis. Although VADER NLTK didn’t support spanish, there is another library that supports it, called PySentimiento. With this tool I was able to sort out a percentage of positive, negative and neutral lyrics in this song.

## Overall Sentiment Bar.PNG
![Overall Sentiment Bar.PNG](assets/images/Overall_Sentiment_Bar.PNG)

We can notice in the Bar that there are around 45 songs with negative or sad lyrics, 35 with neutral lyrics and 25 with positive lyrics.

## Sentiment roportions in Salsa.PNG
![Sentiment proportions in Salsa.PNG](assets/images/Sentiment_proportions_in_Salsa.PNG)

With this information in mind, I decided to just look which artists had more songs in the playlist, who had the most sad songs, who had the most positive songs, and these were the results.

## Top 10 Artists with more songs.PNG
![Top 10 in Artists with more songs.PNG](assets/images/Top_10_Artists_with_more_songs.PNG)

Willie Colón and Héctor Lavoe being the ones with the most songs, made sense because they had songs with eachother as well as songs by themselves. An observation that surprised me is that the next one is Marc Anthony. That surprised me because it shows a shif in time, taking into account that both Willie Colón and Héctor Lavoe released their songs in the 1970s and 1980s and the Marc Anthony released his songs in the 2000s.

## Top 10 Artists with Saddest Songs.PNG
![Top 10_Artists with Saddest Songs.PNG](assets/images/Top_10_in_Artists_with_Saddest_Songs.PNG)

The Artist with the most sad songs is Gilberto Santa Rosa, followed by Héctor Lavoe, Willie Colón, Marc Anthony and Frankie Ruiz.


