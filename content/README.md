# 5pebbles Project Analysis

## Distribution Analysis
1.⁠ ⁠(1) *Distribution Analysis*: After group the actors into different zodiac signs, we will calculate the distribution. Then we will utilise chi-square to determine if the differences between the zodiac signs are significant or not.

## Movie Count

> code at: https://github.com/epfl-ada/ada-2024-project-5pebbles/blob/Zhichen/results.ipynb


Research question: Do actors with different zodiac signs have a a significant difference in the number of movies they participate.



Methodology: 
1. Group the actors by their zodiac signs.
2. Conduct an ANOVA analysis to determine whether the distribution of movie counts varies significantly across different zodiac signs.


Here's the distribution of movie counts across actors with different zodiac signs:
![zodiac-#movie](img/role_number-zodiac.png)


We use ANOVA Analysis to check if actors with different zodiac signs have a significant difference in the number of movies they participate. Here are the procedures of the ANOVA analysis:

1. **Define the variables**: Let $\mu_i$ represent the mean number of movies for actors with the $i$-th zodiac sign, where $i = 1, 2, \dots, 12$.

2. **Null Hypothesis (\(H_0\)):**  
   The mean number of movies for actors with different zodiac signs is the same.  
   
   $H_0: \mu_1 = \mu_2 = \mu_3 = \cdots = \mu_{12}$
   

3. **Alternative Hypothesis (\(H_A\)):**  
   At least one zodiac sign has a significantly different mean number of movies.  
   $H_A: \text{At least one } \mu_i \text{ is different.}$

4. **Hypothesis Testing**:
    
    The statistic of ANOVA analysis is as follows (rounded to 3 digits):

    ```bash
    F-statistic: 1.800
    P-value: 0.048
    ```
    With confidence level $\alpha=0.05$, we can reject the null hypothesis, indicating actors with different zodiac signs DO have a a significant difference in the number of movies they participate.



## Career Logevity
3.⁠ ⁠(6) *Career longevity*: How do zodiac signs correlate with actors' career longevity, examining the timespan from their first to last movie appearances?

## Genre Analysis
4.⁠ ⁠(2) *Genre Analysis* Preferences for movie genres among actors of different zodiac signs: ① Calculate the distribution of different genre ② Calculate the genre distribution of each sign ③ Divide the two proportion ④ use statstical method to test if the trends are significant.

## Casting Preferences
5.⁠ ⁠(3) *Casting preferences* :① Calculate the distribution of different genre ② Calculate the genre distribution of each sign③ Divide the two proportion ④ use statstical method to test if the trends are significant. (Ren Yi, need normalization, could refer to maskymiliann)

## Type Diversity Index
6.⁠ ⁠(7) *Type Diversity Index*: Which zodiac signs demonstrate greater versatility in genre-switching, and how successful are they in different genres throughout their careers?

## Power Role Analysis
7.⁠ ⁠(5) *Power Role Analysis*: ① Map each actor’s zodiac sign to their respective role ② Use statistical methods (e.g., chi-square tests, logistic regression) to determine if there is a significant association between zodiac signs and the likelihood of being cast in specific roles. Analyze trends and compare how often actors of certain signs are cast as heroes versus villains or sidekicks.

## Oscar Analysis
8.⁠ ⁠(8) *Oscar Analysis*:


## Miscellaneous

![insert a picture](img/template.jpeg "women looking at man")
