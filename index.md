---
layout: page
title: "Actors & Astrology: Zodiac Trends in Movie Field"
cover-img: /assets/img/Finally_a_good_dimension_image.png
thumbnail-img: /assets/img/Finally_a_good_dimension_image.png
share-img: /assets/img/Finally_a_good_dimension_image.png
---
mathjax: true

# Introduction
Astrology has fascinated humanity for centuries, weaving stories of destiny, personality, and cosmic influence. At its heart lies the zodiac, a circle of twelve signs, each tied to celestial alignments and thought to shape our traits and behaviors. From fiery Aries to dreamy Pisces, these signs are often seen as a map to better understand ourselves and the world around us. But astrology isn't just an ancient curiosity—it’s alive and thriving, sparking interest in everything from relationships to careers.

In the realm of film and celebrity culture, astrology has carved out its own niche. Fans eagerly connect their favorite actors to zodiac traits, wondering if a Leo’s natural flair contributes to their screen presence or if a Scorpio’s intensity brings depth to their characters. Even filmmakers have drawn inspiration from astrology, creating characters whose personalities align with the stars. Could the cosmos play a role in what makes a star shine on and off the screen? Whether you’re a skeptic or a believer, the intersection of astrology and creativity is hard to ignore.
(The reformulation was done by chatgpt)

# 5pebbles Project Analysis

# Summary

The analysis highlights interesting patterns in zodiac representation and genre preferences among actors. Cancer and Pisces are notably overrepresented, while Sagittarius and Capricorn are underrepresented. In terms of genre, Sagittarius prefers Thrillers, Aquarius gravitates toward Action/Adventure, and Scorpio leans toward Animation and Family Films. However, the modest effect sizes suggest these patterns are indicative rather than definitive.

## 1. Zodiac Sign Distribution Among Actors  

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

## 2. Genre Preferences by Zodiac Sign  

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

## Movie Count

> code at: https://github.com/epfl-ada/ada-2024-project-5pebbles/blob/Zhichen/results.ipynb


Research question: Do actors with different zodiac signs have a a significant difference in the number of movies they participate.



Methodology: 
1. Group the actors by their zodiac signs.
2. Conduct an ANOVA analysis to determine whether the distribution of movie counts varies significantly across different zodiac signs.


Here's the distribution of movie counts across actors with different zodiac signs:
![zodiac-#movie](/assets/img/role_number-zodiac.png)


We use ANOVA Analysis to check if actors with different zodiac signs have a significant difference in the number of movies they participate. Here are the procedures of the ANOVA analysis:

1. **Define the variables**: Let $$\mu_i$$ represent the mean number of movies for actors with the $$i$$-th zodiac sign, where $$i = 1, 2, \dots, 12$$.

2. **Null Hypothesis (\(H_0\)):**  
   The mean number of movies for actors with different zodiac signs is the same.  
   
   $$H_0: \mu_1 = \mu_2 = \mu_3 = \cdots = \mu_{12}$$
   

3. **Alternative Hypothesis (\(H_A\)):**  
   At least one zodiac sign has a significantly different mean number of movies.  
   $$H_A: \text{At least one } \mu_i \text{ is different.}$$

4. **Hypothesis Testing**:
    
    The statistic of ANOVA analysis is as follows (rounded to 3 digits):

    ```bash
    F-statistic: 1.800
    P-value: 0.048
    ```
    With confidence level $\alpha=0.05$, we can reject the null hypothesis, indicating actors with different zodiac signs DO have a a significant difference in the number of movies they participate.



## Career Logevity
3.⁠ ⁠(6) *Career longevity*: How do zodiac signs correlate with actors' career longevity, examining the timespan from their first to last movie appearances?  

The careers of different actors vary greatly. Some have very long careers, while others are much shorter. Some start acting in films at a very young age, while others continue acting well into old age. We aim to analyze the length of actors' careers, as well as whether their entry age and retirement age are related to their zodiac signs. The results are showned in the following picture.  

![insert image of actor's career](/assets/img/Career_Longivity.png)

Actors of all zodiac signs generally have their first film role around the age of 30 and their last film role around the age of 40, with an average career span of about 10 years. Although there are slight differences between different zodiac signs, the results of ANOVA analysis show that none of the difference is significant.

|                  | F-Statistic | P-Value |
|------------------|-------------|---------|
| Entry AGE        | 0.634       | 0.800   |
| Retire Age       | 0.366       | 0.969   |
| Career Longevity | 0.815       | 0.625   |

## Genre Analysis
4.⁠ ⁠(2) *Genre Analysis* Preferences for movie genres among actors of different zodiac signs: ① Calculate the distribution of different genre ② Calculate the genre distribution of each sign ③ Divide the two proportion ④ use statstical method to test if the trends are significant.

## Casting Preferences
5.⁠ ⁠(3) *Casting preferences* :① Calculate the distribution of different genre ② Calculate the genre distribution of each sign③ Divide the two proportion ④ use statstical method to test if the trends are significant. (Ren Yi, need normalization, could refer to maskymiliann)

Research Question: Is the zodiac distribution of a certain movie genre significantly different from the overall zodiac distribution?

Methodology:
1. Calculate the overall zodiac distribution across all movies.
2. Calculate the zodia distribution of a certain movie genre (for example, Action movies)
3. Use chi-squared test to see if these two distributions are significantly different, and to see what contributes to this difference.

Chi-squared test procedures, take the Action films as the example

1. Define the null hypothesis (H0): There is no significant difference between the overall zodiac distribution across all movies and the zodiac distribution of the selected movie genre.

2. Define the alternative hypothesis (H1): There is a significant difference between the two distributions.

3. Create a contingency table that includes the observed counts of zodiac signs for the overall distribution and the selected movie genre.

| Zodiac Sign   | Aquarius  | Aries    | Cancer   | Capricorn | Gemini   | Leo      |
|---------------|-----------|----------|----------|-----------|----------|----------|
| **Total**     | 80,247.22 | 81,519.0 | 82,230.78| 73,975.72 | 86,070.14| 84,821.41|
| **Action**    | 3,294.78  | 3,347.0  | 3,376.22 | 3,037.28  | 3,533.86 | 3,482.59 |


| Zodiac Sign   | Libra     | Pisces   | Sagittarius | Scorpio   | Taurus   | Virgo    |
|---------------|-----------|----------|-------------|-----------|----------|----------|
| **Total**     | 83,219.20 | 79,885.09| 76,271.46   | 78,368.36 | 77,019.73| 81,911.87|
| **Action**    | 3,416.80  | 3,279.91 | 3,131.54    | 3,217.64  | 3,162.27 | 3,363.13 |


4. Calculate the expected counts for each zodiac sign under the null hypothesis. These can be calculated as: $\text{Expected Count} = \frac{\text{Total count in category} \times \text{Total count in group}}{\text{Grand Total}}$


| Zodiac Sign   | Aquarius  | Aries    | Cancer   | Capricorn | Gemini   | Leo      |
|---------------|-----------|----------|----------|-----------|----------|----------|
| **Total**     | 80,247.22 | 81,519.0 | 82,230.78| 73,975.72 | 86,070.14| 84,821.41|
| **Action**    | 3,294.78  | 3,347.0  | 3,376.22 | 3,037.28  | 3,533.86 | 3,482.59 |


| Zodiac Sign   | Libra    | Pisces   | Sagittarius | Scorpio   | Taurus   | Virgo    |
|---------------|----------|----------|-------------|-----------|----------|----------|
| **Total**     | 83,219.20| 79,885.09| 76,271.46   | 78,368.36 | 77,019.73| 81,911.87|
| **Action**    | 3,416.80 | 3,279.91 | 3,131.54    | 3,217.64  | 3,162.27 | 3,363.13 |



5. Compute the chi-squared statistic using the formula:
   $\chi_{i,j}^2 = \frac{(O_{i,j} - E_{i,j})^2}{E_{i,j}}, \chi^2 = \sum_i \sum_j \chi_{i,j}^2$
   Where $O$ represents the observed counts, and $E$ represents the expected counts, $i$ represents the distribution (overall distribution or the selected genre distribution), $j$ represents the zodiac sign.

| Zodiac Sign   | Aquarius | Aries | Cancer | Capricorn | Gemini | Leo   |
|---------------|----------|-------|--------|-----------|--------|-------|
| **Total**     | 0.17     | 0.07  | 0.13   | 0.02      | 0.07   | 0.05  |
| **Action**    | 4.10     | 1.77  | 3.13   | 0.41      | 1.64   | 1.27  |


| Zodiac Sign   | Libra | Pisces | Sagittarius | Scorpio | Taurus | Virgo  |
|---------------|-------|--------|-------------|---------|--------|--------|
| **Total**     | 0.01  | 0.10   | 0.03        | 0.29    | 0.58   | 0.40   |
| **Action**    | 0.23  | 2.52   | 0.85        | 7.05    | 14.25  | 9.73   |


   $\chi^2_{action}=48.84$

6. Determine the degrees of freedom (df), which is given by:
   $\text{df} = (\text{Number of rows} - 1) \times (\text{Number of columns} - 1) = 11$


7. Compare the chi-squared statistic to the critical value from the chi-squared distribution table at a chosen significance level (e.g., $\alpha = 0.05$) or compute the p-value.
   
   According to the [Chi-Square Distribution Table](https://math.arizona.edu/~jwatkins/chi-square-table.pdf), $\chi^2_{0.050}=19.675$ when the degree of freedom is 11.

8. Interpret the results:
   - If the chi-squared statistic exceeds the critical value or the p-value is less than the significance level, reject the null hypothesis.
     - In the Action films, $\chi^2_{action}=48.84 > \chi^2_{0.050}=19.675$.
     - Therefore, at the 95% confidence level, we reject the null hypothesis.
   - Otherwise, fail to reject the null hypothesis.

9. Identify which zodiac signs contribute most to the observed differences by examining the chi-squared statistic for each genre-zodiac cell, as is shown in step 5.

   Larger results indicate greater contributions to the chi-squared statistic.

   Here are the top 3 Chi-Square Statistics,

   | Zodiac Sign | Action |
   |-------------|--------|
   | Taurus      | 14.25  |
   | Virgo       | 9.73   |
   | Scorpio     | 7.05   |

   which indicates that the distributions of Taurus, Virgo, and Scorpio are the most significantly different between all films and Action films.

Chi-square tests for top 20 popular movie genres are conducted. You could find the result in [genre-zodaic-chi-square.md](./genre-zodiac-chi-square.md).

In these 20 genres 
- 5 genres (Adventure, Romantic drama, Fantasy, Science Fiction, Crime Thriller) are **independent** with zodiac signs.
- 15 genres (Drama, Comedy, Romance Film, Thriller, Action, Crime Fiction, Action/Adventure, World cinema, Black-and-white, Indie, Family Film, Horror, Musical, Romantic comedy, Mystery) illustrate **dependency** with zodiac signs.


## Type Diversity Index
6.⁠ ⁠(7) *Type Diversity Index*: Which zodiac signs demonstrate greater versatility in genre-switching, and how successful are they in different genres throughout their careers?

## Power Role Analysis
7.⁠ ⁠(5) *Power Role Analysis*: ① Map each actor’s zodiac sign to their respective role ② Use statistical methods (e.g., chi-square tests, logistic regression) to determine if there is a significant association between zodiac signs and the likelihood of being cast in specific roles. Analyze trends and compare how often actors of certain signs are cast as heroes versus villains or sidekicks.

## Oscar Analysis
8.⁠ ⁠(8) *Oscar Analysis*: Are actors of different zodiac signs equally likely to win an Oscar? Which zodiac sign has the highest probability of winning an Oscar?

The Academy Awards, commonly known as the Oscars, are annual awards presented by the Academy of Motion Picture Arts and Sciences (AMPAS) to honor outstanding achievements in the film industry. First held in 1929, the Oscars have become one of the most prestigious and widely recognized accolades in cinema. In this analysis, we gathered the data of the winner of best actor and best actress from 1929-2023 and analyzed the awarding rate of different zodaic signs.  

Methology:  
1. Calculate the zodiac distribution of Oscar winners
2. Calculate the awarding rate of different zodiac signs
3. Use z-score and Chi-square Test to test if the differences of awarding rate among different zodiac signs are significant

![insert oscar picture](/assets/img/OscarAwardingRate.png)  

Capricorn, Aries, and Taurus are the top three zodiac signs with the highest winning rates, while Aquarius, Gemini, and Sagittarius are the three zodiac signs with the lowest winning rates.  

We applied a z-score test to assess the statistical significance of these differences. Among the 12 zodiac signs, actors born under Capricorn have a significantly higher awarding rate than the average (z-score = 2.985, p-value < 0.05), while those born under Aquarius have a significantly lower awarding rate than the average (z-score = -2.949, p-value < 0.01). For other zodiac signs, the differences in awarding rates compared to the average are not statistically significant. Additionally, we conducted a Chi-Square test to examine whether awarding rates are significantly correlated with zodiac signs. The results (chi-square statistic = 14.177, p-value=0.223) indicates that although the awarding rates of some zodiac sign are significant different from the avarage, Overall, there is no significant correlation between zodiac signs and awarding rates.

**result of z-score**

| Zodiac Sign | Awarding Rate | Z-Score | P-Value | Significant? |  
|-------------|---------------|---------|---------|--------------|   
| Capricorn   | 6.43‰         | 2.985   | 0.003   | True         |    
| Aquarius    | 0.76‰         | -2.949  | 0.003   | True         |  



## Miscellaneous

![insert a picture](/assets/img/template.jpg)

