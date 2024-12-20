---
layout: page
title: "Actors & Astrology: Zodiac Trends in Movie Field"
cover-img: /assets/img/Finally_a_good_dimension_image.png
thumbnail-img: /assets/img/Finally_a_good_dimension_image.png
share-img: /assets/img/Finally_a_good_dimension_image.png
---


# 1. Introduction
Astrology has fascinated humanity for centuries, weaving stories of destiny, personality, and cosmic influence. Its heart lies in the zodiac, twelve signs, each tied to celestial alignments and thought to shape our traits and behaviors. From Aries to Pisces, these signs are often seen as a way to better understand ourselves and the world around us. But astrology isn't just an ancient curiosity, it’s alive and thriving, sparking interest in everything from relationships to careers.

In the scope of film and celebrity culture, astrology has carved out its own position. Fans eagerly connect their favorite actors to zodiac traits, wondering if a Leo’s natural flair contributes to their screen presence or if a Scorpio’s intensity brings depth to their characters. Even filmmakers have drawn inspiration from astrology, creating characters whose personalities align with the stars. Could the cosmos play a role in what makes a star shine on and off the screen? Whether you’re a skeptic or a believer, the intersection of astrology and creativity is hard to ignore.

# 2. Dataset


## don't know what it is
5pebbles Project Analysis
Summary

The analysis highlights interesting patterns in zodiac representation and genre preferences among actors. Cancer and Pisces are notably overrepresented, while Sagittarius and Capricorn are underrepresented. In terms of genre, Sagittarius prefers Thrillers, Aquarius gravitates toward Action/Adventure, and Scorpio leans toward Animation and Family Films. However, the modest effect sizes suggest these patterns are indicative rather than definitive.

# 3. Zodiac Sign Distribution Among Actors  

### Key Statistics
- **Initial Dataset Size**: 450,668 records  
- **Post-Cleaning Dataset Size**: 242,096 records  

### Distribution Plot  
Generally, the zodiac sign Cancer has the highest representation, while Sagittarius has the lowest representation.

### Significance Test
The zodiac sign distribution was statistically analyzed using a chi-square test:  
- **Chi-Square Statistic**: 50.58  
- **P-Value**: 4.92e-07  

The null hypothesis of a uniform distribution is rejected, indicating that the zodiac distribution is significantly non-uniform.  

#### Significant Observations
**Overrepresented signs**:  
- Cancer (8.71%): Z-Score = 2.97, P-Value = 0.00295  
- Pisces (8.69%): Z-Score = 2.82, P-Value = 0.00476  
- Leo (8.66%): Z-Score = 2.54, P-Value = 0.01109  

**Underrepresented signs**:  
- Capricorn (7.89%): Z-Score = -3.47, P-Value = 0.00053  
- Sagittarius (7.92%): Z-Score = -3.28, P-Value = 0.00103  

**Signs with no significant differences**: Virgo, Gemini, Libra, and others showed distributions close to the expected uniform proportions (P > 0.05).  

These findings suggest that certain zodiac signs, particularly Cancer and Pisces, are disproportionately represented among actors, while others like Capricorn and Sagittarius are underrepresented. Notably, 5 out of 12 signs deviate significantly from the expected uniform proportions, providing evidence of non-random patterns.  

While Cancer has the highest representation, other signs like Gemini and Virgo appear evenly distributed, suggesting these signs may not exhibit strong astrological influences on representation. A preliminary hypothesis can thus be drawn: individuals born under Cancer, Pisces, and Leo may be more likely to become actors.

### ⭐ Astrological Context
To provide context, a brief explanation of zodiac basics and elemental dynamics is useful. The zodiac signs are categorized into four elemental groups:
- **Water** (Cancer, Pisces, Scorpio)  
- **Earth** (Taurus, Virgo, Capricorn)  
- **Fire** (Aries, Leo, Sagittarius)  
- **Air** (Gemini, Libra, Aquarius)  

Cancer and Pisces belong to the Water element, often associated with emotional depth and intuition, while Leo is a Fire sign, symbolizing passion and creativity. In zodiac interpretations, these signs are frequently described as emotionally expressive, traits that may align with the demands of acting.

Interestingly, an online search for “zodiac signs best suited to acting” frequently lists Leo first, followed by Pisces, with Cancer mentioned less often. This aligns with our findings: Leo and Pisces show strong representation among actors, with Cancer unexpectedly emerging as the most overrepresented sign. This discrepancy between popular perceptions and statistical results invites further exploration.

Further research is needed to explore potential cultural or psychological factors contributing to these trends.  

# 4. Do Zodiac Signs Influence the Number of Movies Actors Star In?

In the glitzy world of cinema, where stars of the celestial and celebrity kind align, a curious question emerged: Could an actor’s zodiac sign influence their career’s trajectory? To unravel this cosmic mystery, we embarked on an exploration of data and statistics, asking: Do actors with different zodiac signs significantly differ in the number of movies they participate in?

> code at: https://github.com/epfl-ada/ada-2024-project-5pebbles/blob/Zhichen/results.ipynb


To investigate, we turned to hypothesis test methods:

1.	Grouping by Zodiac Signs: First, actors were categorized according to their zodiac signs, creating twelve distinct groups—one for each sign.

2.	Analysis of Variance (ANOVA): Then, we conducted an ANOVA test to compare the distribution of movie counts across these zodiac groups. This statistical test measures whether differences between groups are significant or merely a result of chance.


Before diving into the results, we visualized the data. The chart above illustrates how the number of movies varies across actors belonging to each zodiac sign. Patterns began to emerge, hinting at potential differences, but could they be statistically confirmed?

Here's the distribution of movie counts across actors with different zodiac signs:
![zodiac-#movie](/assets/img/role_number-zodiac.png)


Here the verdict, ANOVA Analysis, comes to rescue!

The ANOVA test provided these key statistics (rounded to three decimal places):
```bash
	F-statistic: 1.800
	p-value: 0.048
```

At a 95% confidence level, these results are illuminating. With a p-value below the threshold of 0.05, we found that the differences in movie counts across zodiac signs are indeed significant. In other words, the data supports the hypothesis that zodiac signs are associated with variation in the number of movies actors participate in.

## Conclusion

While this analysis does not imply causation—astrological signs may not directly influence an actor’s success—it opens the door to fascinating discussions about underlying factors, whether cultural, psychological, or simply coincidental, that could align with zodiac sign traits. The stars, it seems, may have more sway over Hollywood than we once thought.

# 5. Are there any differences in the careers of actors with different zodiac signs

The careers of different actors vary greatly. Some have very long careers, while others are much shorter. Some start acting in films at a very young age, while others continue acting well into old age. We aim to analyze the length of actors' careers, as well as whether their entry age and retirement age are related to their zodiac signs. The results are showned in the following picture.  

![insert image of actor's career](/assets/img/EntryAge.png)
![insert image of actor's career](/assets/img/RetireAge.png)
![insert image of actor's career](/assets/img/CareerSpan.png)

Actors of all zodiac signs generally have their first film role around the age of 30 and their last film role around the age of 40, with an average career span of about 10 years. Although there are slight differences between different zodiac signs, the results of ANOVA analysis show that none of the difference is significant.

|                  | F-Statistic | P-Value |
|------------------|-------------|---------|
| Entry AGE        | 0.634       | 0.800   |
| Retire Age       | 0.366       | 0.969   |
| Career Longevity | 0.815       | 0.625   |



# 6. Genre Preferences by Zodiac Sign  

### Key Statistics
There are 81,740 films in the film dataset. The top 11 genres with the highest percentages are:  
- **Drama**: 41.6%  
- **Comedy**: 25.34%  
- **Action/Adventure**: 22.41%  
- **Romance Film**: 16.65%  
- **Thriller**: 10.7%  
- **Documentary**: 6.89%  
- **Animation**: 4.32%  

### Findings
The distribution of movie genres shows a dominance of Drama, Comedy, and Action/Adventure. Genres like Animation and Musical, while less common, offer insights into niche preferences.  

### Analysis Techniques
- **Normality Tests**: Most genres showed normal distribution, except Comedy (p = 0.041).  
- **ANOVA and Kruskal-Wallis**: Significant variations in genre preferences across zodiac signs were identified (ANOVA F = 8068.49, P < 0.001; Kruskal-Wallis H = 129.10, P < 0.001).  
- **Normalization**: Genre preferences were normalized against base rates to highlight deviations from expected trends.  

### Normalized Preference
For example, Aquarius's +0.74 in Action/Adventure means 74% higher preference than expected given the genre's base rate of 22.4%.

#### Specificity Test
Specificity measures how unique a zodiac sign's preference is compared to other signs:
- **Positive values**: preference stronger than other signs  
- **Negative values**: preference weaker than other signs  
- **Magnitude**: degree of preference uniqueness  

### Key Insights
- **Sagittarius**: Strong preference for Thrillers (+0.125 specificity).  
- **Aquarius**: Notable affinity for Action/Adventure (+0.097 specificity).  
- **Scorpio**: Unique preferences for Animation (+0.175) and Family Films (+0.167).  
- **Capricorn**: Preference for Musicals (+0.170) contrasts with aversion to Family Films (-0.154).  

### Pattern Analysis
- **Fire signs** (Aries, Leo, Sagittarius): Varied preferences across genres.  
- **Earth signs** (Taurus, Virgo, Capricorn): Strong contrasts.  
- **Air signs** (Gemini, Libra, Aquarius): Moderate specificity patterns.  
- **Water signs** (Cancer, Scorpio, Pisces): Tend toward creative/emotional genres.  

### Variability Analysis
The coefficient of variation (CV) quantifies the relative dispersion of genre preferences among zodiac signs:  
- Highest variability: Taurus, Gemini, and Aries (~0.85).  
- Lowest variability: Scorpio (~0.82).  

### Statistical Significance
Three statistically significant preferences emerged:  
1. **Sagittarius → Thriller** (Z=2.369)  
2. **Aquarius → Action/Adventure** (Z=1.972)  
3. **Taurus → Drama** (Z=2.242)  

While zodiac signs display distinct genre preferences, the effect sizes remain moderate. The patterns observed suggest subtle influences rather than deterministic relationships.


## Distribution Analysis
1.⁠ ⁠(1) *Distribution Analysis*: After group the actors into different zodiac signs, we will calculate the distribution. Then we will utilise chi-square to determine if the differences between the zodiac signs are significant or not.



## Genre Analysis
4.⁠ ⁠(2) *Genre Analysis* Preferences for movie genres among actors of different zodiac signs: ① Calculate the distribution of different genre ② Calculate the genre distribution of each sign ③ Divide the two proportion ④ use statstical method to test if the trends are significant.

# 7.  Do Zodiac Signs Shape Their Starring Roles in Movie Genres?

Amid the endless reels of cinematic storytelling, a fascinating question beckons: Are certain zodiac signs more likely to shine in specific movie genres? By delving into the intersection of astrology and cinema, we sought to uncover whether the distribution of zodiac signs within a given genre deviates significantly from the overall zodiac distribution across all films.


To tackle this question, we employed a structured approach:

1.	Overall Zodiac Distribution: First, we calculated the distribution of zodiac signs across all movies in the dataset, creating a benchmark.
2.	Genre-Specific Zodiac Distribution: Next, we focused on individual genres—beginning with Action films as an example—to determine their unique zodiac makeup.
3.	Chi-Squared Test: Finally, we used a chi-squared test to compare these distributions, assessing whether the genre-specific zodiac spread significantly deviates from the overall benchmark.


The chi-squared test for Action films revealed a chi-square statistic of 48.84, which is large enough to conclude—at a 95% confidence level—that the zodiac distribution within Action films significantly differs from the overall distribution.

We then drilled down to identify the zodiac signs contributing most to this divergence. Here are the top contributors:

   | Zodiac Sign | Contribution to chi-square value |
   |-------------|--------|
   | Taurus      | 14.25  |
   | Virgo       | 9.73   |
   | Scorpio     | 7.05   |

This analysis suggests that actors born under Taurus, Virgo, and Scorpio deviate most from the expected proportions in Action films.


Expanding the analysis to the top 20 most popular genres yielded intriguing results:
- Genres independent of zodiac signs: (Adventure, Romantic drama, Fantasy, Science Fiction, Crime Thriller).
- Genres showing dependency: (Drama, Comedy, Romance Film, Thriller, Action, Crime Fiction, Action/Adventure, World Cinema, Black-and-White, Indie, Family Film, Horror, Musical, Romantic Comedy, Mystery).

The findings suggest a complex relationship between zodiac traits and genre preferences, with some genres showing a strong alignment with specific zodiac patterns while others remain unaffected.


While the results are compelling, they invite both curiosity and caution. The data reveals significant zodiac-genre dependencies in many cases, but the reasons behind these patterns remain open to interpretation. Could cultural stereotypes, casting tendencies, or even intrinsic zodiac traits play a role? The cinematic zodiac story is one of intrigue, leaving room for both statistical and creative exploration.


# 8. Dancing Through Genres - The Art of Versatility
6.⁠ ⁠(7) *Type Diversity Index*: Which zodiac signs demonstrate greater versatility in genre-switching, and how successful are they in different genres throughout their careers?

### The Question of Versatility

In our continuing exploration of zodiac signs' influence on acting careers, we arrive at an intriguing question: Does an actor's zodiac sign influence their ability to navigate different film genres? To answer this, we developed a sophisticated metric called the Genre Diversity Index (GDI) to measure actors' versatility across different film genres.

Think of actors as painters with films as their canvas - some work with a broad palette of genres, while others perfect their craft within a specific style. Just as a masterful artist might move between watercolors and oils, versatile actors transition between comedy and drama, action and romance. But does the cosmic alignment at the time of their birth influence this artistic flexibility?

### Measuring Genre Diversity

To capture this artistic versatility in numerical terms, we crafted the Genre Diversity Index (GDI) - a sophisticated measure that acts like a theatrical report card. Imagine evaluating a chef's versatility not just by the number of dishes they can cook, but also by how well they balance their menu and how confidently they execute each cuisine type. Similarly, our GDI looks at three crucial aspects of an actor's genre performance:

1. **Raw Diversity Score (30% weight)**
   - Measures how many different genres an actor has explored
   - Like counting the colors in an artist's palette

2. **Shannon Diversity Index (40% weight)**
   - Measures how evenly an actor distributes their performances
   - Similar to evaluating how well an artist uses all their colors

3. **Genre Balance Score (30% weight)**
   - Measures the balance between most and least frequent genres
   - Like assessing if an artist favors certain colors too heavily

![Insert Box Plot: GDI Distribution Across Zodiac Signs](/assets/img/Genre_Diversity_Index_Distribution_by_Zodiac_Sign.png)

*Our box plot reveals the distribution of Genre Diversity Index across zodiac signs, showing median values and outliers.*

### What the Numbers Tell Us

Analyzing over 12,000 actors' careers revealed fascinating patterns:

1. **Top Performers**
   - Sagittarius leads with a GDI of 0.733379
   - Gemini follows extremely closely at 0.733362
   - Libra ranks third with 0.732426

2. **Lower Range**
   - Taurus (0.722559)
   - Aries (0.726952)
   - Capricorn (0.727069)

These numbers tell a story of subtle cosmic influence. Consider how Sagittarius, known for its adventurous spirit, shows the highest versatility - perhaps reflecting their astrological reputation for exploring new territories. Meanwhile, Gemini's close second place aligns with their dual nature, suggesting an innate ability to adapt to different theatrical demands.

The clustering of scores within such a tight range (0.722-0.733) tells us something remarkable about professional acting - regardless of zodiac sign, successful actors tend to develop significant versatility. It's as if the demands of the craft itself shape performers more than their astrological predispositions.

![Insert Violin Plot: GDI Distribution Density](/assets/img/Genre_Diversity_Index_Distribution_by_Zodiac_Sign_Violin_Plot.png)

*The violin plot shows the full distribution shape of GDI scores across zodiac signs.*

### Statistical Insights

Our statistical analysis using the Kruskal-Wallis test revealed:
- H-statistic: 14.364
- p-value: 0.213
- Effect size (η²): 0.000

These results suggest that while we observe small differences in genre diversity across zodiac signs, these differences aren't statistically significant. In other words, while the stars might whisper suggestions about an actor's path, they don't shout commands. The small differences we observe are like subtle brushstrokes in a larger masterpiece - interesting to note but not defining the overall picture.

![Insert Bar Chart](/assets/img/Mean_Genre_Diversity_Index_by_Zodiac_Sign.png)

*The bar chart displays mean GDI values with standard deviation for each zodiac sign.*

### Key Findings

1. **Minimal Variation**
   - GDI scores cluster tightly between 0.722 and 0.733
   - Very small variance between highest and lowest scores (difference of ~0.01)

2. **Consistency Across Signs**
   - High mean GDI scores (>0.72) across all signs
   - Suggests that successful actors generally maintain diverse portfolios regardless of zodiac sign

3. **Variance Patterns**
   - Aquarius shows highest variability (SD: 0.115085)
   - Libra shows most consistency (SD: 0.098141)

### Conclusion

Just as the night sky presents a complex tapestry of stars, our analysis reveals an intricate pattern of artistic versatility among actors. While zodiac signs might add a touch of celestial flavor to an actor's career journey, the true story appears to be one of human adaptability and professional growth.

Our Genre Diversity Index analysis reveals that while subtle patterns exist in how different zodiac signs approach genre diversity, these differences are minimal and not statistically significant. The consistently high GDI scores across all signs suggest that versatility in acting may be more related to career opportunities and professional choices than astrological influences.

This analysis provides a quantitative foundation for understanding how actors navigate different genres throughout their careers, while maintaining scientific rigor in our examination of potential zodiac influences.

# 9. The Stars Align: A Deep Dive into Zodiac Signs and Lead Roles in Cinema
7.⁠ ⁠(5) *Power Role Analysis*: ① Map each actor’s zodiac sign to their respective role ② Use statistical methods (e.g., chi-square tests, logistic regression) to determine if there is a significant association between zodiac signs and the likelihood of being cast in specific roles. Analyze trends and compare how often actors of certain signs are cast as heroes versus villains or sidekicks.


In the vast constellation of Hollywood, we've often wondered: do the stars that guided an actor's birth influence their path to stardom? As part of our comprehensive study exploring the relationship between zodiac signs and acting careers, we delved into one of the most intriguing questions - does an actor's zodiac sign correlate with their likelihood of landing lead roles?

### The Celestial Distribution

![Insert Lead Role Ratio Bar Chart visualization](/assets/img/Lead_Role_Ratio_by_Zodiac_Sign.png)
*Lead Role Ratio Across the Zodiac*

At first glance, our data reveals a fascinating pattern. Like the bright stars of Aries dominating the spring sky, actors born under this sign shine brightest in our analysis, securing lead roles in 33.34% of their appearances. This isn't just celestial coincidence - our statistical analysis confirms these differences are significant, with both chi-square and Kruskal-Wallis tests yielding p-values below 0.001.

The zodiac wheel seems to favor fire and air signs, with Gemini (32.75%) and Leo (32.57%) following closely behind Aries. Perhaps there's something to the ancient wisdom about fire signs' natural leadership qualities and air signs' adaptability. Meanwhile, Capricorn, traditionally associated with steady climbing, surprisingly shows the lowest lead role ratio at 28.36%.

### When Stars Meet Genre

![Insert Zodiac-Genre Interaction Heatmap](/assets/img/Zodiac-Genre_Interaction_Effect_on_Lead_Roles.png)
*Heat Map of Zodiac-Genre Interaction Effects in Lead Roles*

But the story gets even more interesting when we look at how different signs perform across various film genres. Our heatmap reveals some truly stellar connections:

Imagine a Sagittarius documentary filmmaker, capturing truth through their lens - our data shows they're 70.49% more likely to lead in documentaries! Though with a small sample size, it's like spotting a rare celestial event - fascinating but requiring careful interpretation.

The romance genre tells an equally compelling tale. Aries actors, with their passionate nature, show a remarkable 35.46% higher likelihood of leading romantic films. With over 1,400 cases in our sample, this is no shooting star - it's a consistent pattern worth noting.

![Insert Lead Role Distribution by Genre and Zodiac Sign Plot](/assets/img/Lead_Role_Distribution_by_Genre_and_Zodiac_Sign.png)
*Lead Role Distribution Patterns Across Movie Genres by Zodiac Sign*


Horror films reveal their own cosmic connections, with Gemini actors showing a 27.50% higher chance of leading these spine-chilling tales. Perhaps their dual nature makes them particularly adept at portraying complex, horror-worthy characters?

### The Dark Side of the Moon

Not every celestial alignment is favorable. Our data reveals some interesting voids - particularly in animation voice acting, where every zodiac sign shows negative correlations. It's like a cosmic eclipse affecting all signs equally, suggesting this might be more about industry practices than astrological influence.

The documentary genre also shows some interesting shadows, with certain signs showing strong negative correlations. However, like trying to spot a distant planet, our small sample sizes in this category require us to view these findings through a properly calibrated telescope.

### Statistical Constellations

Our ANOVA results add another layer to this cosmic story. With an F-statistic of 10.095 (p < 0.001) for zodiac signs and even stronger results for genre effects (F = 92.514, p < 4.50e-192), we're seeing clear evidence that these patterns aren't just random stellar noise.

The effect sizes might be subtle - like distant stars whose light is faint but measurable - with our Cramer's V of 0.033 suggesting a small but meaningful influence. It's a reminder that in both astronomy and cinema, significant patterns don't always need to be obvious to be important.

### Charting the Future

What does this celestial map mean for the film industry? While we're not suggesting casting directors should consult their ephemeris, our findings provide an interesting lens through which to view talent distribution in cinema. Like ancient astronomers finding patterns in the night sky, we've uncovered correlations that, while not definitively causal, offer fascinating insights into the relationship between birth dates and career trajectories.

Our analysis continues as part of a larger exploration of zodiac influences in cinema, but this chapter reveals that perhaps, in some small way, the stars of our birth might indeed influence our path to the stars of Hollywood.

# 10. Are actors of different zodiac signs equally likely to win an Oscar?

The Academy Awards, commonly known as the Oscars, are annual awards presented by the Academy of Motion Picture Arts and Sciences (AMPAS) to honor outstanding achievements in the film industry. First held in 1929, the Oscars have become one of the most prestigious and widely recognized accolades in cinema. In this analysis, we gathered the data of the winner of best actor and best actress from 1929-2023 and calculated the awarding rate of different zodaic signs. Then we use z-score and Chi-square Test to test if the differences of awarding rate among different zodiac signs are significant.

![insert oscar picture](/assets/img/OscarAwardingRate.png)  

As shown in the graph above, Capricorn, Aries, and Taurus rank as the top three zodiac signs with the highest winning rates, while Aquarius, Gemini, and Sagittarius are the three with the lowest winning rates. Furthermore, our statistical analysis reveals that actors born under Capricorn have a significantly higher awarding rate than the average (z-score = 2.985, p-value < 0.05), whereas those born under Aquarius exhibit a significantly lower awarding rate than the average (z-score = -2.949, p-value < 0.01). For the remaining zodiac signs, the differences in awarding rates compared to the average are not statistically significant. Additionally, we performed a Chi-Square test to assess whether awarding rates are significantly associated with zodiac signs. The results (chi-square statistic = 14.177, p-value = 0.223) indicate that, while some individual zodiac signs show significant deviations from the average awarding rate, there is no overall significant correlation between zodiac signs and awarding rates.

**result of z-score**

| Zodiac Sign | Awarding Rate | Z-Score | P-Value | Significant? |  
|-------------|---------------|---------|---------|--------------|   
| Capricorn   | 6.43‰         | 2.985   | 0.003   | True         |    
| Aquarius    | 0.76‰         | -2.949  | 0.003   | True         |  
 

# 11. Conclusion
The analysis of the zodiac signs in the context of cinema reveals a real interest in the influence of these astrological archetypes on characters, storylines, and even casting choices. The zodiac signs often present a reference point for shaping the personality and the traits of characters, allowing to enchance their integrity and depth.

For the actors themselves, some traits, associated with their astrological signs, sometimes seem to align with the role they play. Even though this correspondence is somewhat due to chance or subjective interpretation, it still reinforce the idea of a subtle link between an actor's personality and the energy they project on screen. Moreover, in a world where storytelling relies heavily on archetypes, the zodiac signs bring an intuitive and universal framework that can captivate the audience's imagination.

However, it is cruicial to recognize that the impact of astrological signs in films remains subjective and highly depends on the belief of viewers and creators. Some people see these correspondences as mere coincidence, while others see them as a powerful creative tool for shaping narratives and building deep connections with the audience.

In conclusion, the zodiac signs offer a fascinating perspective for exploring the connection between human traits and fictional characters. Although they neither dictate the fate of actors nor determine the success of films, they enrich the cinematic experience by introducing a mythological and universal dimension.

## Miscellaneous

![insert a picture](/assets/img/template.jpg)

