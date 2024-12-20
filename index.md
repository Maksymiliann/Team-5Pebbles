---
layout: page
title: "Actors & Astrology"
subtitle: "Zodiac Trends in Movie Field"
cover-img: /assets/img/Finally_a_good_dimension_image.png
thumbnail-img: /assets/img/Finally_a_good_dimension_image.png
share-img: /assets/img/Finally_a_good_dimension_image.png
---


## 1. Introduction
Astrology has fascinated humanity for centuries, weaving stories of destiny, personality, and cosmic influence. In its core lies the zodiac, twelve signs, each tied to celestial alignments and thought to shape our traits and behaviors. From Aries to Pisces, these signs are often seen as a way to better understand ourselves and the world around us. But astrology isn't just an ancient curiosity, it’s alive and thriving, stirring interest in everything from relationships to careers.

In the scope of film and celebrity culture, astrology has carved out its own position. Fans eagerly connect their favorite actors to zodiac traits, wondering if a Leo’s natural flair contributes to their screen presence or if a Scorpio’s intensity brings depth to their characters. Even filmmakers have drawn inspiration from astrology, creating characters whose personalities align with the stars. Could the cosmos play a role in what makes a star shine on and off the screen? Whether you’re a skeptic or a believer, the intersection of astrology and creativity is hard to ignore.

> Hey, before we get into the specifics, how well do you know the **twelve zodiac signs**? It’s helpful to provide a bit of context on the zodiac itself.  
> **⭐ Zodiac Basics ⭐**  
> To understand the traits linked to different signs, let’s first look at the basic elemental groups of the zodiac:  
> - **Water** (Cancer, Pisces, Scorpio)  
> - **Earth** (Taurus, Virgo, Capricorn)  
> - **Fire** (Aries, Leo, Sagittarius)  
> - **Air** (Gemini, Libra, Aquarius)  
>  
> Each element is associated with specific characteristics: Water signs like Cancer and Pisces are often seen as emotional and intuitive, Earth signs are practical and grounded, Fire signs are passionate and dynamic, and Air signs are intellectual and communicative. These elemental qualities often serve as the foundation for astrological interpretations.  

## 2. Dataset
Our dataset is an extensive collection comprising the CMU Movies Summary Corpus, an Oscar dataset, and an additional dataset generated with ChatGPT and Claude about the leading role in movies. The features from the CMU Movies Summary Corpus are segregated into two important parts: the movie metadata and the character metadata. The movie metadata encompasses a total of 81,741 different movies across more than 100 different genres. It also provides data such as the movie's name, release date, box office revenue, runtime, language, and genres. For each of these films, characters from the character metadata appearing in the film are listed. After processing the data, a total of 51,390 individual actors were documented with features including their real name, character's name, age at the movie's release, gender, ethnicity, height, and date of birth. Additionally, a plot summary is sometimes included to complete the data.

The second data is the Oscar data from Data World, which includes the birthdates of all the winners of the Best Actor and Best Actress awards from 1928 to 2023.


Finally, our last dataset is an AI-generated dataset used to complete the CMU Movies Summary Corpus by adding the feature from the leading role for every character, allowing us to have a better understanding of the role played by the actors


## 3. Research Questions
### 3.1 Are actors uniformly distributed across zodiac signs

<!-- Is the distribution of actors across zodiac signs uniform, or are certain signs more represented than others? Which zodiac sign has the highest representation among actors? What is the distribution of some domographic factors like gender? Our project calculates the distribution and uses the Chi-Square test and Z-Score to determine whether the differences are statistically significant. -->

An intuitive question would be: **Are actors uniformly distributed across zodiac signs?** Here is the the zodiac sign distribution of actors in our CMU dataset.

![zodiac distribution](/assets/img/DistributionZodiacSigns.png)

Among all zodiac signs, **Cancerians** take the crown with 8.71% of actors, following closely are **Pisces** (8.69%) and **Leo** (8.66%). This statistic matches the theory of zodiac signs. Known for their emotional depth and intuition, Cancerians might have a gift for embodying complex characters on screen. Pisces are often described as dreamy and empathetic—traits that align well with acting. Meanwhile, fiery Leo, the "performer" of the zodiac, lives up to its reputation, bringing creativity and charisma to the industry.

On the other end, **Sagittarius** and **Capricorn** find themselves underrepresented, comprising only 7.92% and 7.89% of actors, respectively. We try to explain the inactiveness of these two zodiac signs as this: Sagittarians, known for their adventurous spirit, might be more drawn to pursuits outside the movie industry. Capricorns, with their practical and disciplined nature, could lean toward structured careers rather than the unpredictable world of acting.

**However, is it possible that all the differences are just a coincidence?**

To test the myth of coincidence, we have hypothesis test as the most handy tool! Our chi-square test, with **p-value (< 0.0001)**, evidently demonstrates that **actors are not uniformly distributed across zodiac signs**. This finding suggests that some astrological factors might subtly influence who ends up on the silver screen—or perhaps it reflects societal perceptions of certain traits linked to zodiac signs.

As we move forward, we’ll explore whether these zodiac differences translate to specific genre preferences or casting decisions. For now, it’s clear that the stars don’t just light up the night sky—they may also shine a subtle light on the silver screen 🌟.

**Wait a minute, is there other confounders in this distribution analysis?** For example, maybe all the the zodiac distribution of female actors are not uniform, but for male actors, the distribution is uniform? This leads to our coming question: **Are the zodiac distributions of male and female actors different from each other?**


The graph below shows the zodiac sign distribution of actors by gender. In this dataset, the number of male actors is higher than the number of female actors. Among male actors, Cancer is the most common zodiac sign, while Capricorn is the least common. Among female actors, Leo is the most common zodiac sign, and Sagittarius is the least common. 

![Gender Analysis](/assets/img/GenderAnalysis.png)

However, despite the differences in the distributions, the results of the Chi-Squared Test (p-value > 0.1) indicate that there is no significant difference between the zodiac sign distributions of male and female actors.


### 3.2 Do Zodiac Signs Influence the Number of Movies Actors Appear In?

In the fancy world of cinema, a curious question emerged: **Do actors with different zodiac signs significantly differ in the number of movies they participate in?**


To investigate, we turned to hypothesis test methods:

1.	Grouping by Zodiac Signs: First, actors were categorized according to their zodiac signs, creating twelve distinct groups, one for each zodiac sign.

2.	Analysis of Variance (ANOVA): Then, we conducted an ANOVA test to compare the distribution of movie counts across these zodiac groups. This statistical test measures whether differences between groups are significant or merely a result of chance.


Before diving into the results, we visualized the data. The chart here illustrates how the number of movies varies across actors belonging to each zodiac sign. Patterns began to emerge, hinting that actors of different zodiac signs may differ in the frequency of screen appearance, but could it be statistically confirmed?

![zodiac-#movie](/assets/img/role_number-zodiac.png)


Here the verdict, ANOVA Analysis, comes to rescue!

The ANOVA test provided these key statistics (rounded to three decimal places):
```bash
	F-statistic: 1.800
	p-value: 0.048
```

With a p-value below the threshold of 0.05, we found that **the differences in movie counts across zodiac signs are indeed significant**. In other words, the data supports the hypothesis that zodiac signs are associated with variation in the number of movies actors participate in.


While this analysis does not imply causation—astrological signs may not directly influence an actor’s success, it opens the door to fascinating discussions about underlying factors, whether cultural, psychological, or simply coincidental, that could align with zodiac sign traits. The stars, it seems, may have more sway over Hollywood than we once thought :)

### 3.3 Are there any differences in the career longevity of actors with different zodiac signs

The careers of different actors vary greatly. Some have very long careers, while others are much shorter. Some start acting in films at a very young age, while others continue acting well into old age. We aim to analyze **the length of actors' careers, as well as whether their entry age and retirement age are related to their zodiac signs**. The results are showned in the following pictures.  

![insert image of actor's career](/assets/img/EntryAge.png)
![insert image of actor's career](/assets/img/RetireAge.png)
![insert image of actor's career](/assets/img/CareerSpan.png)

Actors of all zodiac signs generally have their first film role around the age of 30 and their last film role around the age of 40, with an average career span of about 10 years. Although there are slight differences between different zodiac signs, the results of ANOVA analysis show that **none of the differences is significant**.

|                  | F-Statistic | P-Value |
|------------------|-------------|---------|
| Entry AGE        | 0.634       | 0.800   |
| Retire Age       | 0.366       | 0.969   |
| Career Longevity | 0.815       | 0.625   |




### 3.4 Do Genre Distributions Differ Across Zodiac Signs?

Do certain zodiac signs naturally gravitate toward specific genres? For example, is it possible that Sagittarius has a huge preference for thrillers, while Scorpio prefers Animations?  In this section, we dive deep into genre distribution of different zodiac signs.  

<!-- Let’s find out which signs thrive in Thrillers, who rules Romance, and why Fire signs might dominate Action while Water signs find their home in emotional storytelling. -->

> **🎬 The Big Picture**
> - Drama dominates with 41.6% of all films
> - Comedy brings joy to 25.3%
> - Action/Adventure thrills in 22.4%
> - Romance captures 16.7%
> - Thrillers keep us on edge at 10.7%

<!-- ### How We Read the Stars: Our Methodology -->

Imagine your daily food: if meat takes up 40% of most people's diet, and you eat 80% meat in your food, it’s clear you have a sweet spot for meat. Similarly, we want to see the genre distribution in different zodiac signs. We defined several concept here: **Base Rate**  for how common each genre is, **Zodiac-Specific Genre Rate** for the the popularity of the genre in a specific zodiac sign. Dividing these gave us a **Preference Index** , where scores above 1 reveal stronger preferences in the zodiac towards the genre and scores below 1 show weaker preference

Finally, we normalize the Preference Index to z-scores, and plot the following heatmap:

![Gender Analysis](/assets/img/genre_movie.png)  

Here we have some significant star-genre alignments:

**Capricorn:** Our data reveals Capricorns as the surprising champions of musicals, showing a remarkable +17.0% specificity for the genre. Yet in a fascinating twist, these same stage-loving Capricorns strongly shy away from family films (-15.4%), painting a picture of a sign that prefers Broadway sophistication to Disney animation.

**Scorpio:** While some might expect Scorpios to gravitate toward darker themes, our analysis reveals an unexpected truth: they show the strongest affinity for animation (+17.5%) and family films (+16.7%) among all signs. Perhaps these mysterious water signs channel their legendary intensity into appreciating the boundless creativity of animated storytelling.

**Sagittarius:** True to their adventurous nature, Sagittarians show a distinct preference for keeping audiences on the edge of their seats, with a +12.5% specificity for thrillers and +8.3% for crime fiction. These celestial archers seem to aim their arrows straight at the heart of suspenseful storytelling.

Other zodiac signs also reveal some positive tendencies: 
- Virgos bring their analytical nature to family films (+11.8%)
- Libras balance their way into musicals (+11.0%)
- Aquarians channel their revolutionary spirit into action/adventure (+9.7%)
- Cancer's emotional depth finds expression in crime fiction (+8.6%).

However, there're some negative associations between zodiac signs and genre:
- Geminis and Capricorns both seem to flee from family films (-15.5% and -15.4% respectively)
-  Sagittarius stay away from animation (-14.7%)
-  Taurus lacks interest in musicals (-14.9%)


If we group the zodiac signs by their type, we could have further perspectives:

**🔥 Fire Signs (Aries, Leo, Sagittarius)**: Like their ruling element, fire signs burn bright across varied genres, refusing to be boxed into any single category. Sagittarius leads the pack with their passion for thrillers (+12.5%), while their fellow fire signs show dynamic preferences across action and adventure genres. This diversity perfectly reflects their naturally energetic and multifaceted personalities.

**💨 Air Signs (Gemini, Libra, Aquarius)**: True to their intellectual nature, air signs float through genres that challenge the mind. Aquarius particularly flourishes in action/adventure (+9.7%), perhaps drawn to the strategic complexity these films offer. Meanwhile, Libra's preference for harmony finds its expression in musicals (+11.0%), where story and song create perfect balance.

**🌊 Water Signs (Cancer, Scorpio, Pisces)**: In a delightful surprise, these emotionally deep signs don't just swim in dramatic waters. Scorpio leads with an unexpected love for animation (+17.5%) and family content (+16.7%), while Cancer navigates toward crime fiction (+8.6%). These preferences suggest water signs might use different genres as channels for their characteristic emotional depth.

**🌍 Earth Signs (Taurus, Virgo, Capricorn)**: Earth signs display perhaps the most fascinating contrasts in our analysis. Capricorn scales the heights of musical theater (+17.0%), Virgo nurtures a connection with family films (+11.8%), while Taurus shows their steadfast nature by maintaining consistent, if moderate, preferences across most genres. Their grounded nature apparently doesn't prevent them from reaching for the stars.

As we delve deeper into how zodiac signs influence casting choices and genre alignment, the question lingers:  **Could the stars also shape the roles actors play in these genres?**  

Let’s explore this in the next section.  





### 3.5  Do Zodiac Sign Distributions Differ Across Movie Genres?

Are certain zodiac signs more likely to shine in specific movie genres? By delving into the intersection of astrology and cinema, we sought to uncover **whether the distribution of zodiac signs within a given genre deviates significantly from the overall zodiac distribution across all films**.


To tackle this question, we employed a structured approach:

1.	Overall Zodiac Distribution: First, we calculated the distribution of zodiac signs across all movies in the dataset, creating a benchmark.
2.	Genre-Specific Zodiac Distribution: Next, we focused on individual genres to determine their unique zodiac distribution.
3.	Chi-Squared Test: Finally, we used a chi-squared test to compare these distributions, assessing whether the genre-specific zodiac distribution significantly deviates from the overall benchmark.


The chi-squared test for Action films revealed a chi-square statistic of 48.84, which is large enough to conclude—at a 95% confidence level—that the zodiac distribution within Action films significantly differs from the overall distribution.

We then drilled down to identify the zodiac signs contributing most to this divergence in Action films. Here are the top contributors:

   | Zodiac Sign | Contribution to chi-square value |
   |-------------|--------|
   | Taurus      | 14.25  |
   | Virgo       | 9.73   |
   | Scorpio     | 7.05   |

This analysis suggests that actors born under Taurus, Virgo, and Scorpio deviate most from the expected proportions in Action films.


Expanding the analysis to the top 20 most popular genres yielded intriguing results:
- Genres independent of zodiac signs: Adventure, Romantic drama, Fantasy, Science Fiction, Crime Thriller.
- Genres showing dependency: Drama, Comedy, Romance Film, Thriller, Action, Crime Fiction, Action/Adventure, World Cinema, Black-and-White, Indie, Family Film, Horror, Musical, Romantic Comedy, Mystery.

The findings suggest a complex relationship between zodiac traits and genre preferences, with some genres showing a strong alignment with specific zodiac patterns while others remain unaffected.


While the results are compelling, they invite both curiosity and caution. The data reveals significant zodiac-genre dependencies in many cases, but the reasons behind these patterns remain open to interpretation. Could cultural stereotypes, casting tendencies, or even intrinsic zodiac traits play a role? The cinematic zodiac story is one of intrigue, leaving room for both statistical and creative exploration.


### 3.6. Do Versatility (i.e. diversity) Differ Across Zodiac Signs?

In the grand theater of cinema, some actors are like chameleons, effortlessly shifting between comedic and dramatic roles, while others perfect their craft within a specific genre. But **does zodiac sign influence this artistic flexibility**? Our versatility study set out to explore this intriguing question.


Imagine measuring an actor's versatility like evaluating a master chef's repertoire - it's not just about how many dishes they can cook, but how well they balance their menu and execute each cuisine. Our versatility combines three essential elements in a carefully weighted formula:

**versatility = 0.3 × Raw Diversity + 0.4 × Shannon Diversity + 0.3 × Genre Balance**

Where:
- **Raw Diversity** = Number of unique genres / Total possible genres measures the variety of genres an actor has explored
- **Shannon Diversity** = -Σ(p_i * ln(p_i)), where p_i is the proportion of movies in genre i, evaluates how evenly performances are distributed across genres
- **Genre Balance** = 1 - (max_genre_proportion - min_genre_proportion), assesses the balance between most and least frequent genres

After analyzing over 12,000 actors' careers, we discovered a fascinating pattern. Sagittarius, the adventurous explorer of the zodiac, leads with the highest versatility score (0.733379), closely followed by the adaptable Gemini (0.733362) and the balanced Libra (0.732). This cosmic alignment seems to mirror these signs' traditional characteristics - Sagittarius's love for exploration, Gemini's natural duality, and Libra's inherent balance.


However, the most revealing insight wasn't in the differences between signs, but in their similarities. All zodiac signs maintained remarkably high versatility scores (above 0.72), with minimal variation between them. This suggests that successful actors, regardless of their zodiac sign, tend to develop significant versatility throughout their careers.

Even the statistical analysis (Kruskal-Wallis test, p-value: 0.213) confirms that while zodiac signs might whisper suggestions about an actor's path, they don't dictate it. The true story appears to be the human adaptability rather than celestial influence.

Perhaps the most compelling conclusion is that versatility in acting transcends zodiac signs boundaries. Whether born under the adventurous stars of Sagittarius or the grounded sign of Taurus, successful actors find ways to expand their dramatic range and explore diverse theatrical territories.

### 3.7 Do Leading Role Ratios Differ Across Zodiac Signs?

In the dazzling constellation of Hollywood, we discovered an intriguing pattern: the stars under which actors were born might just influence their appearance as a leading role. Here we have the chart for leading role ratio across the zodiac signs.

![Insert Lead Role Ratio Bar Chart visualization](/assets/img/Lead_Role_Ratio_by_Zodiac_Sign.png)

Like their elemental nature, Fire signs dominate the spotlight. Aries leads the charge, claiming lead roles in 33.34% of their appearances - significantly higher than any other sign. Following closely are their fellow fire sign Leo (32.57%) and the adaptable air sign Gemini (32.75%). This isn't just celestial coincidence; our statistical analysis confirms these differences are significant (p < 0.001).

More specifically, we have the heatmap of leading role ratios (normalized to z-scores) on the dimensions of zodiac signs and genres.

<!-- ## When Stars Align with Genre -->
![Insert Zodiac-Genre Interaction Heatmap](/assets/img/Zodiac-Genre_Interaction_Effect_on_Lead_Roles.png)

Our analysis uncovered some remarkable correlations:

- 🎭 **The Romantic Warriors**: Aries actors shine brightest in romance films, with a stunning 35.46% higher likelihood of landing leading roles. With over 1,400 cases studied, this is no mere coincidence.
  
- 👻 **Masters of Horror**: Gemini's dual nature seems perfect for horror films, showing a 27.50% higher chance of leading these spine-chilling tales.

- 🎬 **Documentary Stars**: In an unexpected twist, Sagittarius shows a remarkable 70.49% higher likelihood of leading documentaries (though we should note the smaller sample size here).

<!-- ## The Scientific Sparkle -->

We conducted ANOVA analysis on the leading role distribution on genres across different zodiac signs.

- ANOVA Results: F = 92.514 (p < 4.50e-192)
- Effect Size: While subtle (Cramer's V = 0.033), the pattern is consistent and significant

As a result, the tiny p-value indicates that the leading role distribution on genres are not consistent across different zodiac signs.

<!-- > **✨ Did You Know?**
> While Capricorn shows the lowest overall lead role ratio (28.36%), they tend to excel in specific genres, demonstrating that success in Hollywood isn't one-size-fits-all! -->

<!-- ## The Bottom Line -->

While we're not suggesting casting directors should start consulting zodiac signs for casting, our analysis reveals intriguing patterns in how different zodiac signs tend to shine in various roles. It's a reminder that in the magical world of cinema, sometimes the stars above align with the stars on screen in unexpected ways.

### 3.8 Are actors of different zodiac signs equally likely to win an Oscar?

The Academy Awards, commonly known as the Oscars, are annual awards presented by the Academy of Motion Picture Arts and Sciences (AMPAS) to honor outstanding achievements in the film industry. First held in 1929, the Oscars have become one of the most prestigious and widely recognized accolades in cinema. 

In this analysis, we gathered the data of the winner of best actor and best actress from 1929-2023 and calculated the awarding rate of different zodaic signs. Then we use z-score and Chi-square Test to test **if the differences of awarding rate among different zodiac signs are significant**.

![insert oscar picture](/assets/img/OscarAwardingRate.png)  

> **🌟 Spotlight on Capricorn**
> - Oscar Awarding Rate: The highest awarding rate (6.42‰)
> - Z-score results: Z-score = 2.985, p-value < 0.05


> **✨ Did You Know?**
> While Capricorn has the lowest overall lead role ratio, they actually have the highest Oscar-winning rate.

As shown in the graph above, Capricorn, Aries, and Taurus rank as the top three zodiac signs with the highest winning rates, while Aquarius, Gemini, and Sagittarius are the three with the lowest winning rates. Furthermore, our statistical analysis reveals that actors born under Capricorn (6.43‰) have a significantly higher awarding rate than the average (z-score = 2.985, p-value < 0.05), whereas those born under Aquarius exhibit a significantly lower awarding rate (0.76‰ ) than the average (z-score = -2.949, p-value < 0.05). For the remaining zodiac signs, the differences in awarding rates compared to the average are not statistically significant. 

Additionally, we performed a Chi-Square test to assess whether awarding rates are significantly associated with zodiac signs. The results (chi-square statistic = 14.177, p-value = 0.223) indicate that, while some individual zodiac signs show significant deviations from the average awarding rate, there is no overall significant correlation between zodiac signs and awarding rates.

 

## 4. Conclusion

The analysis of zodiac signs in cinema reveals a real connection between astrological archetypes and the development of characters, storylines, and even casting choices. These signs often serve as a reference for shaping the characters' personalities, adding depth and integrity to their portrayal and encouraging the audience to engage with the story on a deeper level. 

For actors, some traits associated with their zodiac signs, sometimes appear to align with the roles they play, reinforcing the idea of a hidden link between their personalities and the energy they project on screen. Even though this connection may be coincidental or open to interpretation, it still highlights how zodiac signs can offer a universal framework that captivates the audience’s imagination, enhancing the cinematic experience. However, it is crucial to recognize that the impact of astrology in films is subjective, some viewing it as a creative tool for narrative building, while others see it as mere coincidence. Ultimately, astrology adds an enriching layer to the storytelling, but its influence on a film's success remains secondary to the strength of the narrative itself.

In conclusion, although the zodiac signs do not dictate the fate of actors nor determine the success of films, they offer an fascinating perspective for exploring the connection between human traits and fictional characters. They introduce a mythological and universal dimension to cinema, broadening our understanding of the art and offering new ways to engage with the stories. Thank you for joining us in this exploration of the cosmic influences on the cinematic world. May the stars continue to inspire and illuminate both our films and our collective imagination.


