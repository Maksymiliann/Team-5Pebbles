---
layout: page
title: How Music Moves Movies
---

## Introduction

Hit musical numbers from the blockbuster movies ‘Dilwale Dulhania Le Jayenge’ and ‘Titanic’ continue to occupy a special place in people’s hearts even today. This might make you think: What are the secret ingredients of music that enrapture all of us and how does it add magic to movies? With this thought in mind, we will use the CMU Movie Summary Corpus and our Spotify Dataset to find out the dominant music attributes (danceability, energy, valence, etc.) in different genres of movies globally so as to possibly reveal any connections between the dominant type of music in a particular movie genre and the cultural identity of a particular country. Subsequently, we will observe the change in music features and their interplay with the changes in the emotions portrayed by movies in the top 2 countries across the years. Finally, we will connect all the dots to reveal how music moves movies towards success.

## Movie Metadata Dataset (CMU Movie Summary Corpus) 

<iframe src="assets/plot/country_piechart_CMU.html" width="750px" height="530px" frameborder="0" position="relative">Top 10 Countries</iframe>

<iframe src="assets/plot/genre_piechart_CMU.html" width="750px" height="530px" frameborder="0" position="relative">Top 10 Genres</iframe>

<iframe src="assets/plot/lang_piechart_CMU.html" width="750px" height="530px" frameborder="0" position="relative">Top 10 Languages</iframe>

## Movie Metadata Analysis and Findings
First, let's take a look at box-office revenues. Since our aim is to study the links between the music soundtrack and the film, we first need to understand the internal dynamics of movies. Box-office revenue is a good indication of a film's success. Let's see how it relates to certain features and find out why.

From our analysis, we find out that there is a little positive correlation between revenue and year of production (pearson correlation coeff of 0.18 and p-value <0.05). “Younger" films seem to earn more! However, this could be due to inflation. By adjusting revenue with the Consumer Price Index (CPI) for USD, using the formula : 
$$ Adjusted \space Revenue = \frac{Movie \space Box \space Office \space Revenue}{CPI \space of \space movie \space release \space date}*CPI \space of \space baseyear $$
We notice that there's no longer any correlation between years and revenue (p-value = 0.5 and coeff very near to zero =-0.007).

XXXXXXXXXXXXXXXGraphXXXXXXXXXXXXXXXXXXXXX
To see whether film genre, language and country of production have an impact on income, let's take a closer look at these 3 categories. Each film can belong to more than one genre, language and country of production. Let's look at the top 10 in each category. 
XXXXXXXXXXXXXXXGraphXXXXXXXXXXXXXXXXXXXXXX
The top 10 in the country and language categories includes 80% of films, 50% in the genre category. To measure the link between these categories and the revenue, we'll take into account only these top 10 to make the results easier to read. (Or even the top 3 when the results graphs are too disordered, representing 62% of films for language, 70% for country, 27% for genre).
XXXXXXXXXXXXXXXGraphXXXXXXXXXXXXXXXXXXXXX
Overall, the boxplots overlap, so we can't really draw any conclusions as to the link between genre and revenue, except that “Black and White” movies earn less than Thriller, Action and Comedy movies . Similarly, when it comes to the country of production, the boxplots overlap. However, the trend seems to be towards lower revenues for Indian films and higher revenues for German films. This trend is also reflected in the language category: Tamil-language films (and silent films) earn less than films in languages such as German, Japanese or Spanish. Note, however, that this is not true for Hindi-language films. There is also a significant difference between the length of films produced in India and those produced in the rest of the top 10. We'll be taking a closer look at the cultural aspect of the films. But first, let's take a closer look at the music dataset.

## Spotify Data Analysis and Findings
For our cultural analysis, we wanted to compare possible connections between the dominant type of music in a movie and the cultural identity of a particular country. For this, we scraped the spotify album data from all movies available, and started out by analysing the different track features. Spotify provides “audio feature information” in the form of scores between 0 and 1 representing the accousticness, danceability, energy, instrumentalness, liveness, loudness, speechiness, tempo and valence.
XXXXXXXXXXXXXXXXXXXXXXPair plotXXXXXXXXXXXXXXXXXXXX
As we could expect, these are mostly strongly correlated. They are far from all being independent, loudness being a big part of explaining energy, with a correlation coefficient close to 1. Danceability and valence also go together, as valence is a measure describing the musical positiveness conveyed by a track.

But imagining films, depending on what genre of a certain film, different music plays in our heads. Thinking about romantic movies leads our mind to a calm, slow, romantic waltz, while in our head there is maybe more heavy metal playing when thinking about action movies. We identified movie genre therefore as possible cofounder and conducted as well an analysis on them. But although we have this different melodies in mind about what music belongs to a certain genre of music, surprisingly, in statistic, non of this is clearly visible. Films of different genres present quite similar characteristics regarding the music played in them. We could therefore exclude the genres as possible cofounders. 


