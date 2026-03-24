I am working with Faroese data on HbA1c measurements. We have every HbA1c measurement taken in the entire population. We want to estimate the prevalence of prediabetes (HbA1c 42-47) in people aged 30-79. The way we'll do that is to take every measurement in the last 24 months in that range; if an individual has a such a measurement and never HbA1c ≥48 or T1D / T2D diagnosis, they are classified as prediabetes. However, not everyone has had a test -- approx. 40% of the population has. We do presume that every case of T1D or T2D *has* had a test in that period, though. Therefore we don't need to make assumptions about the true diabetes prevalence.

So far, I have just taken a prevalence of 1) tested positive divided by tested, and 2) tested positive divided by population size.

My supervisor has sent an e-mail asking me to estimate the true prediabetes prevalence; they have written that I should look at the age- and sex-group level probabilities of having been tested and use those to weight by inverse probability, after which they want me to standardize to the background population by age- and sex-group.

I want you to look at the Faroese statistics body's website and find the numbers (they exist) of number of people alive in each 5-year age group for males and females, respectively. Use these to do the weighting and the standardization.

I then want you to write an R quarto doc that 

1) simulates data that fit the description I gave you. Here, I want you to use probabilites of testing that are dependend on age, sex and diabetes status (remember, P(test|diabetes=1)=1, otherwise P(test|diabetes=0, sex, age) = ??). Males and older people should have higher probabilities, averaging to ~40% for the entire population.

2) Estimate that population-prevalence of prediabetes, using only the simulated pop_tested sample and the population-level summary group sizes you retrieved (this should be downloaded from the Faroese statistics body's website).

3) Compare the estimated values to the "true" (simulation-informing) values.

I am personally having trouble understanding what exactly they mean by first inverse probability weight and then standardize. In my mind, these two end up being the very same step, but I may be missing something. I am hoping your solution will help clarify this for me.