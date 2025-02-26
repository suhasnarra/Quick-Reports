Project Date: Feb 17, 2025

This study was started with the purpose of concretely defining what "short", "medium" and, "long" mean when defining football distances. 
In the traditional sense, it is thought that there are three clusters of yards to go for a first down, with each having a lower likelihood than the next of successful conversion. 

The study aimed to do the following:
- Use data from NFLFastR datasets from 2021-2024 to identify league-wide third down conversion rates
- Using these conversion rates and Machine Learning algorithms, cluster data into 3 categories based on conversion rate

The main issue I ran into:
- The conversion rates I calculated were almost perfectly linear with respect to yards to go
- As such, a clustering model would not be able to accurately model distance ranges

What I chose to do:
- I opted to create a linear regression model that models the third down conversion rate based on yards to go; this model is much more accurate and representative of NFL third down conversions than a clustering model

What I found:
- The biggest dropoff in conversion rate occurs in short yard to go situations, namely 1, 2, and 3-4 yards to go. 
- 3rd & 1 has a >60% chance of conversion
- 3rd & 2 has a ~53% chance of conversion
- 3rd & 3-4 has a ~46.5% chance of conversion
- From there the conversion rates generally followed the model until 20 yards to go
- Beyond 20  yards to go, 3rd downs are rare and have conversion rates of almost 0%. 
