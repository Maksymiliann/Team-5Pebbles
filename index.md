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
$$
  Adjusted revenue = \frac{Movie Box Office Revenue}{CPI of movie released date}*CPI of baseyear
$$

