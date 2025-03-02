Project Date: Feb 17 - March 2, 2025

This study was started with the purpose of concretely defining what "short", "medium" and, "long" mean when defining football distances. 
In the traditional sense, it is thought that there are three clusters of yards to go for a first down, with each having a lower likelihood than the next of successful conversion. 

The study aimed to do the following:
- Use data from NFLFastR datasets from 2021-2024 to identify league-wide third down conversion rates
- Using these conversion rates and Machine Learning algorithms, cluster data into 3 categories based on conversion rate

The main issue I ran into:
- The conversion rates I calculated were almost perfectly linear with respect to yards to go
- As such, a clustering model would not best model conversion rate based on distance

What I chose to do:
- I opted to create a linear regression model that models the third down conversion rate based on yards to go; this model is much more accurate and representative of NFL third down conversions than a clustering model

What I found:
- The biggest dropoff in conversion rate occurs in short yard to go situations, namely 1, 2, and 3-4 yards to go. 
- 3rd & 1 has a >60% chance of conversion
- 3rd & 2 has a ~53% chance of conversion
- 3rd & 3-4 has a ~46.5% chance of conversion
- From there the conversion rates generally followed the model until 20 yards to go
- Beyond 20  yards to go, 3rd downs are rare and have conversion rates of almost 0%. 

Beyond the regression testing, I did still cluster the distances.

Algorithms Used:
- K-Means --> Clusters data based on the average of the clusters
- Fuzzy C-means --> Clusters similar to K-means, while giving a probability of each cluster. The highest probability is chosen as the label

What I've Found, generally:
- "Short" --> 1-2 yards to go
- "Medium" --> 3-6 yards to go
- "Long" --> 7+ yards to go

There is some noise on 1st down at 2 and 6 yards to go; this can probably be attributed to a low sample size. Those down and distance occurrences are rare outside of goal-to-go situations, and would probably need a deeper analysis to really understand them. In the context of this study, I'm treating them as "Short" and "Medium" respectively. 