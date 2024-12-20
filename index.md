---
layout: page
title: "Actors & Astrology: Zodiac Trends in Movie Field"
cover-img: /assets/img/Finally_a_good_dimension_image.png
thumbnail-img: /assets/img/Finally_a_good_dimension_image.png
share-img: /assets/img/Finally_a_good_dimension_image.png
---


# 1. Introduction
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

# 2. Dataset
Our dataset is an extensive collection comprising the CMU Movies Summary Corpus, an Oscar dataset, and an additional dataset created with ChatGPT about PLEASE WRITE HERE. The features from the CMU Movies Summary Corpus are segregated into two important parts: the movie metadata and the character metadata. The movie metadata encompasses a total of 81,741 different movies from 1892 to 2013 across more than 100 different genres. It also provides data such as the movie's name, release date, box office revenue, runtime, language, and genres. For each of these films, characters from the character metadata appearing in the film are listed. After processing the data, a total of 242,096 individual actors were documented with features including their real name, character's name, age at the movie's release, gender, ethnicity, height, and date of birth. Additionally, a plot summary is sometimes included to complete the data.
The Oscar dataset features ...
And the last one ...


## don't know what it is
5pebbles Project Analysis
Summary

The analysis highlights interesting patterns in zodiac representation and genre preferences among actors. Cancer and Pisces are notably overrepresented, while Sagittarius and Capricorn are underrepresented. In terms of genre, Sagittarius prefers Thrillers, Aquarius gravitates toward Action/Adventure, and Scorpio leans toward Animation and Family Films. However, the modest effect sizes suggest these patterns are indicative rather than definitive.

# 3. Research Questions
## 3.1 Are actors uniformly distributed across zodiac signs

<!-- Is the distribution of actors across zodiac signs uniform, or are certain signs more represented than others? Which zodiac sign has the highest representation among actors? What is the distribution of some domographic factors like gender? Our project calculates the distribution and uses the Chi-Square test and Z-Score to determine whether the differences are statistically significant. -->

An intuitive question would be: **Are actors uniformly distributed across zodiac signs?** Here is the the zodiac sign distribution of actors in our CMU dataset.

![zodiac distribution](/assets/img/DistributionZodiacSigns.png)

Among all zodiac signs, **Cancerians** take the crown with 8.71% of actors, following closely are **Pisces** (8.69%) and **Leo** (8.66%). This statistic matches the theory of zodiac signs. Known for their emotional depth and intuition, Cancerians might have a gift for embodying complex characters on screen. Pisces are often described as dreamy and empathetic—traits that align well with acting. Meanwhile, fiery Leo, the "performer" of the zodiac, lives up to its reputation, bringing creativity and charisma to the industry.

On the other end, **Sagittarius** and **Capricorn** find themselves underrepresented, comprising only 7.92% and 7.89% of actors, respectively. We try to explain the inactiveness of these two zodiac signs as this: Sagittarians, known for their adventurous spirit, might be more drawn to pursuits outside the movie industry. Capricorns, with their practical and disciplined nature, could lean toward structured careers rather than the unpredictable world of acting.

**However, wait a minute, is it possible that all the differences are just a coincidence?**

To test the myth of coincidence, we have hypothesis test as the most handy tool! Our chi-square test, with **p-value (< 0.0001)**, evidently demonstrates that **actors are not uniformly distributed across zodiac signs**. This finding suggests that some astrological factors might subtly influence who ends up on the silver screen—or perhaps it reflects societal perceptions of certain traits linked to zodiac signs.

As we move forward, we’ll explore whether these zodiac differences translate to specific genre preferences or casting decisions. For now, it’s clear that the stars don’t just light up the night sky—they may also shine a subtle light on the silver screen 🌟.

**Wait a minute, is there other confounders in this distribution analysis?** For example, maybe all the the zodiac distribution of female actors are not uniform, but for male actors, the distribution is uniform? This leads to our coming question: **Are the zodiac distributions of male and female actors different from each other?**


The graph below shows the zodiac sign distribution of actors by gender. In this dataset, the number of male actors is higher than the number of female actors. Among male actors, Cancer is the most common zodiac sign, while Capricorn is the least common. Among female actors, Leo is the most common zodiac sign, and Sagittarius is the least common. 

![Gender Analysis](/assets/img/GenderAnalysis.png)

However, despite the differences in the distributions, the results of the Chi-Squared Test (p-value > 0.1) indicate that there is no significant difference between the zodiac sign distributions of male and female actors.


## 3.2 Do Zodiac Signs Influence the Number of Movies Actors Appear In?

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

## 3.3 Are there any differences in the career longevity of actors with different zodiac signs

The careers of different actors vary greatly. Some have very long careers, while others are much shorter. Some start acting in films at a very young age, while others continue acting well into old age. We aim to analyze **the length of actors' careers, as well as whether their entry age and retirement age are related to their zodiac signs**. The results are showned in the following pictures.  

![insert image of actor's career](/assets/img/EntryAge.png)
![insert image of actor's career](/assets/img/RetireAge.png)
![insert image of actor's career](/assets/img/CareerSpan.png)

Actors of all zodiac signs generally have their first film role around the age of 30 and their last film role around the age of 40, with an average career span of about 10 years. Although there are slight differences between different zodiac signs, the results of ANOVA analysis show that none of the differences is significant.

|                  | F-Statistic | P-Value |
|------------------|-------------|---------|
| Entry AGE        | 0.634       | 0.800   |
| Retire Age       | 0.366       | 0.969   |
| Career Longevity | 0.815       | 0.625   |




## 3.4 A Journey Through Cinema's Genre Galaxy: Genre Preferences by Zodiac Sign  

After exploring how zodiac signs might influence actors' careers in Section 3.3, a new question arises: could the stars also play a role in the types of movies actors are drawn to—or perhaps excel in? To answer this, we turn our gaze toward the genres of over 81,740 films, analyzing how celestial patterns align with Hollywood's diverse storytelling landscape.  

From heart-pounding Action to tear-jerking Dramas, every genre holds its own allure. But do certain zodiac signs naturally gravitate toward specific genres? And if so, how might their astrological traits shape their preferences? In this section, we dive deep into the cosmic currents to uncover these stellar connections.  

Let’s find out which signs thrive in Thrillers, who rules Romance, and why Fire signs might dominate Action while Water signs find their home in emotional storytelling.

> ### Hollywood's Genre Landscape  
> Before diving into the zodiac-specific insights, let’s take a step back and look at the bigger picture. Hollywood's genre distribution is as diverse as it is fascinating: 
> Drama reigns supreme, claiming 41.6% of all films, followed by Comedy (25.3%) and Action/Adventure (22.4%). Romance captures hearts with 16.7%, and Thrillers keep us on the edge at 10.7%.  
> But raw numbers alone don’t paint the full picture. It’s not just about which genres dominate; it’s about how specific zodiac signs connect to these genres in unexpected ways.

### How We Read the Stars: Our Methodology  

Imagine a party with snacks: if most people eat 40% chocolate and you eat 80%, it’s clear you have a sweet spot for it. Similarly, we calculated a **Base Rate** for how common each genre is, and a **Zodiac-Specific Rate** for how often actors of each sign appear in them. Dividing these gave us a **Preference Index**, where scores above 1 reveal stronger preferences and below 1, less interest—highlighting the cosmic link between zodiac traits and Hollywood genres.  

![Gender Analysis](/assets/img/genre_movie.png)  

#### :sagittarius: The Thrill Seekers  
Sagittarius shines in Thrillers, favoring suspenseful storytelling with a +12.5% preference. Their adventurous, daring nature makes them natural fits for edge-of-your-seat tales.  

#### ♒ Aquarius: Action Heroes  
Aquarians dominate Action/Adventure films, with a staggering +74% preference index. Their rebellious and innovative streak fits perfectly in high-energy, adrenaline-packed stories.  

#### ♏ Scorpio: The Genre Chameleon  
Scorpios’ versatility shows in Animation (+17.5%) and Family Films (+16.7%), where their emotional depth brings characters to life.  
<br>

### The Elements at Play  

The patterns became even clearer when we grouped signs by their elements:  

🔥 **Fire Signs** (Aries, Leo, Sagittarius) excel in high-energy genres like Action (+15%) and Thrillers (+12%), thriving on passion and intensity.  

💨 **Air Signs** (Gemini, Libra, Aquarius) gravitate toward experimental and intellectual genres, showing strong preferences for Science Fiction and boundary-pushing stories (+14%). 

🌊 **Water Signs** (Cancer, Scorpio, Pisces) bring unmatched emotional depth to Drama (+8%), Animation (+17.5%), and Family Films (+16.7%).

🌍 **Earth Signs** (Taurus, Virgo, Capricorn) ground themselves in structured genres, excelling in Drama (+22.4%) and Musicals (+17%), showcasing realism and discipline.

### What It All Means?  

Backed by solid statistics, these patterns reveal how zodiac traits align with cinematic storytelling:  

- **Sagittarius** thrives in **Thrillers** (+12.5%, Z=2.369).  
- **Aquarius** dominates **Action/Adventure** (+74%, Z=1.972).  
- **Taurus** excels in **Drama** (+22.4%, Z=2.242).  

Each sign brings unique strengths to the silver screen:  
**Fire signs** energize action, **Air signs** innovate, **Water signs** channel emotion, and **Earth signs** anchor realism. While not absolute, these patterns offer a fresh lens on the cosmic influence in art.  


As we delve deeper into how zodiac signs influence casting choices and genre alignment, the question lingers:  
**Could the stars also shape the roles actors play in these genres?**  
Let’s explore this in the next section.  





## 3.5  Do Zodiac Signs Shape Their Starring Roles in Movie Genres?

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


## 3.6. Dancing Through Genres - The Art of Versatility

In the grand theater of cinema, some actors are like chameleons, effortlessly shifting between comedic and dramatic roles, while others perfect their craft within a specific genre. But does the cosmic alignment at one's birth influence this artistic flexibility? Our Genre Diversity Index (GDI) study set out to explore this intriguing question.

<!-- ### The Celestial Dance of Versatility -->

Imagine measuring an actor's versatility like evaluating a master chef's repertoire - it's not just about how many dishes they can cook, but how well they balance their menu and execute each cuisine. Our GDI combines three essential elements in a carefully weighted formula:

**GDI = 0.3 × Raw Diversity + 0.4 × Shannon Diversity + 0.3 × Genre Balance**

Where:
- **Raw Diversity** measures the variety of genres an actor has explored
- **Shannon Diversity** evaluates how evenly performances are distributed across genres
- **Genre Balance** assesses the balance between most and least frequent genres

After analyzing over 12,000 actors' careers, we discovered a fascinating pattern. Sagittarius, the adventurous explorer of the zodiac, leads with the highest versatility score (0.733), closely followed by the adaptable Gemini (0.733) and the balanced Libra (0.732). This cosmic alignment seems to mirror these signs' traditional characteristics - Sagittarius's love for exploration, Gemini's natural duality, and Libra's inherent balance.

<!-- ### Beyond the Stars -->

However, the most revealing insight wasn't in the differences between signs, but in their similarities. All zodiac signs maintained remarkably high versatility scores (above 0.72), with minimal variation between them. This suggests that successful actors, regardless of their zodiac sign, tend to develop significant versatility throughout their careers.

Even the statistical analysis (Kruskal-Wallis test, p-value: 0.213) confirms that while the stars might whisper suggestions about an actor's path, they don't dictate it. The true story appears to be one of human adaptability and professional growth rather than celestial influence.

Perhaps the most compelling conclusion is that versatility in acting transcends astrological boundaries. Whether born under the adventurous stars of Sagittarius or the grounded sign of Taurus, successful actors find ways to expand their dramatic range and explore diverse theatrical territories.

## 3.7 Dancing with Destiny: How Zodiac Signs Light Up Leading Roles

In the dazzling constellation of Hollywood, we discovered an intriguing pattern: the stars under which actors were born might just influence their journey to center stage. Our analysis revealed some fascinating cosmic connections that would make even skeptics raise an eyebrow.

<!-- ## Fire Signs Burn Brightest -->

![Insert Lead Role Ratio Bar Chart visualization](/assets/img/Lead_Role_Ratio_by_Zodiac_Sign.png)
*Lead Role Ratio Across the Zodiac*

Like their elemental nature, Fire signs dominate the spotlight. Aries leads the charge, claiming lead roles in 33.34% of their appearances - significantly higher than any other sign. Following closely are their fellow fire sign Leo (32.57%) and the adaptable air sign Gemini (32.75%). This isn't just celestial coincidence; our statistical analysis confirms these differences are significant (p < 0.001).

> **🌟 Spotlight on Aries**
> - Lead Role Rate: 33.34%
> - Notable Genre: 35.46% more likely to lead romantic films

<!-- ## When Stars Align with Genre -->
![Insert Zodiac-Genre Interaction Heatmap](/assets/img/Zodiac-Genre_Interaction_Effect_on_Lead_Roles.png)
*Heat Map of Zodiac-Genre Interaction Effects in Lead Roles*

The plot thickens when we look at specific genres. Our analysis uncovered some remarkable correlations:

- 🎭 **The Romantic Warriors**: Aries actors shine brightest in romance films, with a stunning 35.46% higher likelihood of landing leading roles. With over 1,400 cases studied, this is no mere coincidence.
  
- 👻 **Masters of Horror**: Gemini's dual nature seems perfect for horror films, showing a 27.50% higher chance of leading these spine-chilling tales.

- 🎬 **Documentary Stars**: In an unexpected twist, Sagittarius shows a remarkable 70.49% higher likelihood of leading documentaries (though we should note the smaller sample size here).

<!-- ## The Scientific Sparkle -->

Our findings aren't just astrological musings - they're backed by robust statistics:
- ANOVA Results: F = 92.514 (p < 4.50e-192)
- Effect Size: While subtle (Cramer's V = 0.033), the pattern is consistent and significant

> **✨ Did You Know?**
> While Capricorn shows the lowest overall lead role ratio (28.36%), they tend to excel in specific genres, demonstrating that success in Hollywood isn't one-size-fits-all!

<!-- ## The Bottom Line -->

While we're not suggesting casting directors should start consulting astrology charts, our analysis reveals intriguing patterns in how different zodiac signs tend to shine in various roles. It's a reminder that in the magical world of cinema, sometimes the stars above align with the stars on screen in unexpected ways.

## 3.8 Are actors of different zodiac signs equally likely to win an Oscar?

The Academy Awards, commonly known as the Oscars, are annual awards presented by the Academy of Motion Picture Arts and Sciences (AMPAS) to honor outstanding achievements in the film industry. First held in 1929, the Oscars have become one of the most prestigious and widely recognized accolades in cinema. In this analysis, we gathered the data of the winner of best actor and best actress from 1929-2023 and calculated the awarding rate of different zodaic signs. Then we use z-score and Chi-square Test to test if the differences of awarding rate among different zodiac signs are significant.

![insert oscar picture](/assets/img/OscarAwardingRate.png)  

As shown in the graph above, Capricorn, Aries, and Taurus rank as the top three zodiac signs with the highest winning rates, while Aquarius, Gemini, and Sagittarius are the three with the lowest winning rates. Furthermore, our statistical analysis reveals that actors born under Capricorn have a significantly higher awarding rate than the average (z-score = 2.985, p-value < 0.05), whereas those born under Aquarius exhibit a significantly lower awarding rate than the average (z-score = -2.949, p-value < 0.01). For the remaining zodiac signs, the differences in awarding rates compared to the average are not statistically significant. Additionally, we performed a Chi-Square test to assess whether awarding rates are significantly associated with zodiac signs. The results (chi-square statistic = 14.177, p-value = 0.223) indicate that, while some individual zodiac signs show significant deviations from the average awarding rate, there is no overall significant correlation between zodiac signs and awarding rates.

**result of z-score**

| Zodiac Sign | Awarding Rate | Z-Score | P-Value | Significant? |  
|-------------|---------------|---------|---------|--------------|   
| Capricorn   | 6.43‰         | 2.985   | 0.003   | True         |    
| Aquarius    | 0.76‰         | -2.949  | 0.003   | True         |  
 

# 4. Conclusion
The analysis of zodiac signs in the context of cinema reveals a real interest in the influence of these astrological archetypes on characters, storylines, and even casting choices. The zodiac signs often present a reference point for shaping the personality and the traits of characters, allowing to add depth and integrity to their portrayal. This subtle connection between astrological signs and characters’ personalities encourages the audience to engage with the story on a deeper level.

For the actors themselves, some traits, associated with their astrological signs, sometimes seem to align with the roles they play. Even though this alignment might be somewhat coincidental or open to subjective interpretation, it still reinforce the idea of a hidden link between an actor’s personality and the energy they project on screen. In a world where storytelling relies heavily on archetypes, the zodiac signs bring an intuitive and universal framework that can captivate the audience's imagination and enhances the overall cinematic experience.

At the same time, it is crucial to recognize that the impact of astrology in films is subjective and largely depends on the beliefs of both viewers and creators. For some, these correspondences may appear as mere coincidences, as for others, they may regard them as a valuable creative tool for shapping narratives and building deeper connections with the audience. Ultimately, the influence of the stars is not a determining factor in the success of a film, but rather an enriching layer that adds to the richness of the storytelling.

In conclusion, Although the zodiac signs do not dictate the fate of actors nor determine the success of films, they offer an fascinating perspective for exploring the connection between human traits and fictional characters. They introduce a mythological and universal dimension to cinema, broadening our understanding of the art and offering new ways to engage with the stories. Thank you for joining us in this exploration of the cosmic influences on the cinematic world. May the stars continue to inspire and illuminate both our films and our collective imagination.

## Miscellaneous

![insert a picture](/assets/img/template.jpg)

