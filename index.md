---
layout: page
title: How Music Moves Movies
---

## Introduction

Hit musical numbers from the blockbuster movies ‘Dilwale Dulhania Le Jayenge’ and ‘Titanic’ continue to occupy a special place in people’s hearts even today. This might make you think: What are the secret ingredients of music that enrapture all of us and how does it add magic to movies? With this thought in mind, we will use the CMU Movie Summary Corpus and our Spotify Dataset to find out the dominant music attributes (danceability, energy, valence, etc.) in different genres of movies globally so as to possibly reveal any connections between the dominant type of music in a particular movie genre and the cultural identity of a particular country. Subsequently, we will observe the change in music features and their interplay with the changes in the emotions portrayed by movies in the top 2 countries across the years. Finally, we will connect all the dots to reveal how music moves movies towards success.

## Movie Metadata Dataset (CMU Movie Summary Corpus) 

<iframe src="assets/plot/genre_piechart_CMU.html" width="750px" height="530px" frameborder="0" position="relative">Top 10 Genres</iframe>

<iframe src="assets/plot/country_piechart_CMU.html" width="750px" height="530px" frameborder="0" position="relative">Top 10 Countries</iframe>

<iframe src="assets/plot/lang_piechart_CMU.html" width="750px" height="530px" frameborder="0" position="relative">Top 10 Languages</iframe>

<iframe src="assets/plot/runtime_boxplot_top10countries_CMU.html" width="750px" height="530px" frameborder="0" position="relative">RBTC</iframe>

<iframe src="assets/plot/runtime_boxplot_top10languages_CMU.html" width="750px" height="530px" frameborder="0" position="relative">RBTL</iframe>

<iframe src="assets/plot/runtime_lineplot_top10countries_CMU.html" width="750px" height="530px" frameborder="0" position="relative">RLTC</iframe>

<iframe src="assets/plot/runtime_lineplot_top10languages_CMU.html" width="750px" height="530px" frameborder="0" position="relative">RLTL</iframe>

<iframe src="assets/plot/scatterplotmatrix_spotify_final.png" width="750px" height="530px" frameborder="0" position="relative">SMSp</iframe>

<iframe src="assets/plot/genre_pie_spotify.html" width="750px" height="530px" frameborder="0" position="relative">GPieSp</iframe>

<iframe src="assets/plot/country_pie_spotify.html" width="750px" height="530px" frameborder="0" position="relative">CPieSp</iframe>

<iframe src="assets/plot/lang_pie_spotify.html" width="750px" height="530px" frameborder="0" position="relative">LPieSp</iframe>





## Movie Metadata Analysis and Findings
First, let's take a look at box-office revenues. Since our aim is to study the links between the music soundtrack and the film, we first need to understand the internal dynamics of movies. Box-office revenue is a good indication of a film's success. Let's see how it relates to certain features and find out why.

From our analysis, we find out that there is a little positive correlation between revenue and year of production (pearson correlation coeff of 0.18 and p-value <0.05). “Younger" films seem to earn more! However, this could be due to inflation. By adjusting revenue with the Consumer Price Index (CPI) for USD, using the formula : 

$$Adjusted \space Revenue = \frac{Movie \space Box \space Office \space Revenue}{CPI \space of \space movie \space release \space date}*CPI \space of \space baseyear$$

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

####################GRAPHIC GENRES AND MUSIC##########################

Visualising the different features of the music with regard to the different countries the movies were produced in, and the different languages the movie is in, divers differences could have been observed. As features we took the difference music features: Album popularity, track acousticness, danceability, energy, instrumentalness, liveness, loudness, speechiness, tempo, valence. 

Overall the observations could be made that music in films produced in India differ often from the films produced in other countries (Europe, US). The same applies for music in films provided in Hindi, Tamil and Malayalam language. We will quickly state the features below, where we discovered a significant difference. 

#######BOXPLOT WHERE WE CAN CLIC ON THE DIFFERENT COUNTRIES########
#######LINEGRAPH WHERE WE CAN CLIC ON THE DIFFERENT LANGUAGES#######

Let’s dance! [(Dance monkey)](https://open.spotify.com/intl-fr/track/2XU0oxnq2qxCpomAAuJY8K?si=27dff2c069fa4379): 
The outcomes of our graphs show an elevated danceability in films produced in India, as well as for films produced in the languages Tamil and Malayalam. Only looking at the top three countries/languages, this is true throughout the years (only spanish music varies a lot). 

Its all about energy [(Saari Duniya Jalaa Denge)](https://open.spotify.com/intl-fr/track/0YxKKO272sacGBJKjf6FnB?si=73fd450f952c400c):
Music in films produced in India seem to have a higher track energy than music in films produced in countries such as Argentina, Italy, France and UK. This is true especially for the period after 1950. 

Instrumentalness [(Die Zauberflöte)](https://open.spotify.com/intl-fr/track/3aHCqW7Usbfg4jdxkrX1rV?si=32fbdf9718fb4d3e):
In the film music of India, the instrumentalness is significantly lower than the one of the other countries. This can be applied as well to music of films in the languages Tamil and Hindi. Again, it is especially true for movies produced after 1950. 

Turn it up![(Mama Laudaa)](https://open.spotify.com/intl-fr/track/1RcWWgnw5fVm3wcNq11zBu?si=4b8cc16e75e74156):
Regarding the Loudness of the music in movies, the one in films from India is generally louder than the one in the films from Italy, France, Germany and UK. This applies as well to the music in films in the languages Malayalam, Hindi, Tamil. This differences are especially significant after 1950. 

Think positive![(Bien-être)](https://open.spotify.com/intl-fr/track/5VleylW0kyuf4VBDACeUSa?si=62f316c90f82441a):
As well regarding positivity, music in Indian movies has a higher track valence than movies produced in other countries. Same can be applied to films produced in the languages Malayalam, Hindi and Tamil. This is true throughout our timeline. 

Thats taking sooo long… [(Symphony of the Crown, Pt.1)](https://open.spotify.com/intl-fr/track/2KHOwjO9oqYK3zfx7YuuLg?si=59dfe875500c4969):
As a last feature where we found differences, the track duration of indian movies is normally higher compared to films produced elsewhere. Again, this can be applied as well for Tamil, Hindi, Malayalam languages. This is especially the case for the years after 1960.

But there are also indifferent music features… 
For the features album popularity, acousticness, liveness and tempo, no clear distinctions could be seen in the boxplots. The line graphs show for liveness a distinction after 1950, for tempo there is still no visible difference. For acousticness, the film in India have a higher acousticness before 1990, but this changes after this year. Same applies for the Music in Indian language. 

## RQ1: What are the connections (if any) between the dominant type of music in a particular movie genre and the cultural identity of a particular country?
To a certain part we already saw that in the analysis of our different music features in the previous part. But lets take a closer look on our top three countries...

**USA:** The results of the t-tests comparing various track features between the United States and the rest of the world reveals evidence of differences in musical styles. The remarkably low p-values across all features, such as album popularity, track duration, acousticness, danceability, energy, instrumentalness, liveness, loudness, speechiness, tempo, and valence, strongly reject the null hypothesis that there is no distinction between the two groups. These findings suggest that not only do geographical differences exist in terms of album and track popularity, but specific musical attributes vary significantly between the United States and the rest of the world. American movie albums are significantly more popular than the rest of the world, which is not surprising as the US music market is the largest music market in the world, particularly on spotify: 70% of the songs on Spotify's Global Top-50 playlist were recorded by US-based artists. However, while they are much more instrumental than other countries’ music, American movie music is shorter and has a lower score of all other traits.

**India:** Duration, Acousticness, Danceability, Energy, Liveness, Loudness, Speechiness, Tempo and Valence are significantly greater in the music of Indian movies than for movies of other countries. This directly corresponds to the large number of festivals, dance, theatre, folk traditions which are intangible aspects of India’s cultural heritage. In exact contrast, instrumentalness is significantly lower than for movies of other countries, it corresponds to Indian film industry traditions to include songs sung by people rather than simply played by instruments: depicts moods and emotions of people better (actors dance to music and songs). Album Popularity is significantly lower and expected because the Spotify user base is predominantly the Americas and Europe.

**United Kingdom:** The results of our previous study shows the similarity of the musical culture of US and UK. Lots of their music styles are overlapping: American blues, jazz, rock and roll were influencing the music of UK, just like british, irish, scottish music influencing the american music. For this reason, the overlaps between British and American music are no surprise, as they have a common history, a lot of their features are similar. (source: Music of the United Kingdom - Wikipedia !!Attention: Biased source!!)

## RQ2: How has the overall attribute mix of music (in movies) changed (if so) across the years? What is its interplay (if any) with the change in the overall genre and emotions portrayed by the movies across the years?
“Where words fail, music speaks!”
 
This famous quote by Hans Christian Andersen captures the very essence of music: soulful emotions! 
Ever wonder how powerful music in movies is and how it occupies a significant amount of space? Even with eyes closed, one might feel the plot of a movie and receive the emotions transmitted by the movie.
This research embarks on a journey into the heart of this dynamic interplay between the nuanced language of emotions embedded within movie plot summaries. In this exploration, we leverage the power of BERT, a cutting-edge transformer model. BERT allows us to decode the sentiment of love, sadness, joy, anger, fear or also surprise that lie beneath the surface of plot summaries.

*Analysis:*
To begin with, since some movies are classified as many different genres, we aim to extract the mean scores for all of the mentioned emotions. These scores captured the nuanced sentiments in the plot summaries and thus in movies. After that, we were able to visualise the results in a scatter plot matrix and their Pearson correlation coefficients and corresponding p-values. We observed p-values greater than 0.05 only in specific pairings: love-joy, love-surprise, and surprise-fear. Thus we cannot reject the null hypothesis that there are no correlation between theses emotions
ADD scatter plot matrix 

*Time series analysis:*
Regarding the time series analysis, we strategically zoom in on two cinematic powerhouses: USA and India. These nations, representing more than 70% of the total countries in our movie dataset, serve as the focal points for our in-depth time series analysis. As we could see previously in the first research question, USA and India having two different cultures, it will be interesting to see if these differences would also be present in the connection of music with emotions.

*India:*
An analysis of the emotions portrayed by all the Indian movies in our dataset revealed interesting insights. As can be seen from the violin plots above, most of the movies pertaining to all the different genres have negligible sadness while a slightly significant fraction of drama, comedy and romance movies have a moderate level of sadness. 
Love and Surprise content remained quite negligible for all the different genres of movies and this can be linked to the fact that in general, movies often have a greater content of joy and/or anger and/or fear to build up the entire story and elements of love and surprise are interspersed here and there in between to connect the dots. As expected, a substantially larger fraction of comedy movies convey moderately high levels of joy as compared to movies of other genres. Anger remains the highest amongst movies of all the genres with action movies emerging at the top of the ‘anger’ leaderboard. A substantially larger fraction of thriller movies convey moderately high levels of fear as compared to movies of other genres. This is because such movies typically build up the suspense by creating an atmosphere of fear. 
The evolution of Indian film music was right before our eyes!
A particular trend emerges quite clearly from the line plots of the movies pertaining to all the genres. The period of time from the 50s to the 80s is popularly referred to as the golden era of Indian film music. India had just become an independent nation in 1945 and so, Indian cinema was heavily influenced by patriotic fervor and centered on exhibiting the cultural ethos of India. Singers like Lata Mangeshkar and Kishore Kumar won the hearts of many people and sang remarkable songs that touch people’s hearts even today since they captured the essence of Indian culture, traditions and heritage. Classical and folk music (ragas, tanas, etc.) accompanied with classical instruments such as tabla, sitar, dholak, etc. was deeply intertwined with the issues (societal, historical, political, etc.) portrayed by the movies. This was the pre-digital age and music directors would spend hours on end with lyricists, singers, instrumentalists for each and every song in a film to ensure perfect coordination between them and craft a melodious masterpiece. The focus was more on completely immersing the people into the movie so that they could be one with the actors and experience everything which the actors would feel. Consequently, the liveness, energy, instrumentalness and acousticness in the music was high during this period. In contrast, the danceability in the music decreased during this period. This was in particular because of the fact that singers were more concerned about making people understand and feel the content of their songs rather than simply dancing to the beats without any understanding of the lyrics at all. 
The period from the 80s-90s onwards saw a marked shift in this trend.  Danceability suddenly started to pickup again and has only continued to increase ever since. At the same time, while the energy content of the music increased, liveness, instrumentalness and acousticness of the music only decreased. This dramatic shift can be directly attributed to globalization: the time when India opened its doors to the world and consequently, got influenced with the Western music and film culture. New Indian singers (e.g., Alisha Chinai) started singing songs which were fusions of Indian and Western music with groovy beats and the Indian masses started dancing to their tunes. The focus of the film industry shifted increasingly towards the Western pop music culture and this led to the birth of Indian pop music which was centered on high danceability more than anything else. Over the years from 1990s till date, Indian music has followed the growth trajectory guided by danceability. Lyrics and classical instruments which were hallmarks of Indian music during the golden era are gradually fading away with music becoming digitized and revolving around the western focal point of high danceability. Bollywood in India is increasingly becoming more focused on the American philosophy of making money rather than imparting the holistic, immersive experience to people to enrich their understanding. 
As Acton rightly said, “History is not a burden on the memory but an illumination of the soul”. The Indian movie industry must introspect and harness its true strengths: the commitment and vitality of the past, which make India a truly unique country and set it apart from others.
 
The fact that all (except 2) of the emotion and music feature time series are cointegrated for India reveals the fact that over the years, music, which even today forms an integral part of all Indian movies, effectively captures the emotions over the years through an interplay of various features.   

*USA:*
Analysing the violin plot above, we observe a higher fraction of Sadness in romance, drama and comedy genres. This could be attributed to the genres’ focus on more emotional depth than action and thriller genres tending to prioritise excitement and suspense. Then, as expected, Joy in comedy and romance movies is more present due tho the genres’ emphasis on humour and positive relationships than the other three genres of action, thriller and drama. Love and Surprise have very small fraction for all movies genres analysed because these genres often emphasise other emotions. Thus, the fraction of Love in romance movies is slightly higher than for other genres which could be due to the relationship and emotional intimacy of Love in this movie genre. The fraction of Anger is notably higher and uniformly distributed across genres. Finally, Fear is also well present in all these genres with the higher fraction found in thriller movies followed by action movies, indicating their emphasis on suspenseful and more intense storytelling.

The time series analysis for US movies enhance distinctive trend in musical attributes across genres, yet notably, it remains less pronounced than the trends we could observe in Indian movie production. The most perceptible one is the decay of acousticness across genres since 1970 could be reflected from the new era of digital and electronic movie production methods. Furthermore, since 1980, converging speechiness trends suggest a shared emphasis on intelligible and explicit lyrics. Also, since the 90s an increase in instrumentalness scores is notably higher for thriller and action genres indicating the presence and will to heighten suspense and intensity than for other genres. The trends for energy and tempo attributes see a slight increase in their scores suggesting the movie industry favouring more dynamic compositions. 

*Lack of cointegration USA:* 
Regarding the lack of cointegration for music features in thriller movies, this could be due to its shift in style for thematic elements influencing the tempo or instrumental of the associated music. On the other hand, if we focus on sadness as an emotional theme, it might experience changes in expression. Thus, emotional portrayal can result in non-stationary relationships, preventing the establishment of a stable long-run connection between thriller music features and sadness emotions. The same case with anger with the absence of cointegration over time may stem from the dynamic evolution of the thriller genre, leading to variations in the utilisation of music features associated with anger.

For romance movies, the lack of cointegration with joy suggests that the temporal evolution of romantic movies and their musical components may not exhibit consistent patterns with the emotion of joy. For example, modern romantic comedies like “La La Land” (2016) enhance diverse musical styles than its predecessors as “Casablanca”(1942) contributing to the absence of a stable long-run connection between these two. 

Finally focusing on comedy and its absence of cointegration with fear may be attributed to the inherent nature and purpose of comedy. Comedy movies are primarily intended to evoke laughter and amusement employing humour to entertain the audience with for example movies such as “Dumb and Dumber”(1994) or “Superbad”(2007) which can be classified as very lighthearted. On the other hand, the emotion of fear typically involves a sense of threat, danger or suspense which contrasts with comedic intent such as the very famous Alfred Hitchcock’s “Psycho”.

## RQ3: Can a certain music style move a movie towards success? If so, how?

Music moves us. The songs of ‘Pirates of the Caribbean’ or ‘Titanic’ are played at parties, interpreted by orchestras or the background music in some shops. Their music accompanies our daily lives. But is the success of certain film scores also reflected in the success of the films themselves? Is there a secret recipe for film music that leads to film success? That's the third question we've tried to answer.

*Analysis:*
For the sake of simplicity, we defined success in our analysis as the box-office receipts of the films. We wanted to compare it with different musical characteristics and see if there was a correlation between them. A naive analysis would indicate that 'Album_Popularity', 'Track_Duration', 'Track_Acousticness', 'Track_Danceability', 'Track_Energy', 'Track_Instrumentalness', 'Track_Liveness' and 'Track_Tempo' are correlated with a film's revenue. 

However, to establish any causality, we need to neutralize the effect of potential cofounders (runtime, number of language and country (we've seen that genre has no influence on music characteristics and year of release has no influence on movie revenue)). To do this, for each correlated music feature, we divide the dataset into two samples where the distribution of the cofounder factors is similar. The first sample, called treatment, corresponds to high music feature values. The second sample is made up of movies with lower music feature values. We set the thresholds (to define which music feature values are high) so as to maximize the difference in average income between control and treated samples. 

XXXXXXXXXXXXXXXXXXXXXXX histogramm for album popularity, energy and liveness XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

Satisfactory results were obtained for only 3 music features, the rest not being significantly different enough (for instrumentalness, acousticness, and danceability) or pair macthing was not possible (for duration and tempo).

Firstly, our results confirm that the success of a piece of music is correlated with the success of its film, because if the popularity of the music album is high, the revenue from the film is statistically higher. However, for the moment, there's nothing to tell us whether it's the music that makes the film successful or whether it's the film that makes the music successful. It's a bit of a chicken-or-egg question.

As there are only two other music features that are significantly correlated with a film's success (low liveness and high energy is linked with higher revenue), it's difficult to give a recipe for a successful film score. It doesn't give any more clues to our chicken-or-egg question.

Finally, it's rather reassuring to say that it doesn't have simple criteria for making successful music. We still need musicians! We can still say that spectators are not insensitive to the music of a film, far from it! What would 2001: A Space Odyssey be without music? Viewers prefer a soundtrack with high energy and low liveness : listen only to The Lord of the Rings soundtrack ! 

## Conclusion
In conclusion, yes! Music is essential in films, and although we sometimes forget it, it plays an essential role. Watch a film with your eyes closed, and you'll see! Or rather, you'll hear...

It'll take you on board, it'll tell you about a culture! If the film is produced in India, it will take you on a journey through Indian festivals, dance and folk traditions, with higher acousticness, danceability and liveness. If the film is produced in the UK, you'll hear the whisper of the Beatles, you will hear the blues, jazz and rock 'n' roll of British culture.

But that's not all! Like a friend with whom you watch the film, it will accompany your emotions. You're shivering? It will shiver with you! Falling in love? It will be your confidante! Better than that, sometimes it will be the one to provoke your emotions.
XXXXXXXXXXXXXXXXXXXXXXXXX{insert here conclusion of RQ2, i'm not sure to understand well}XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

In the end, it's the one that will stick in your head if you like the film. Because a successful film means a successful soundtrack! But what is a hit soundtrack? Unfortunately or fortunately, we can't give you a recipe... Ask the musicians!



