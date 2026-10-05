# Sprint 1
By Matthew Hendsch & AJ Chiaravalloti

## Mission
For amateur athletes who want to improve their athletic performance, this project is a performance predictor that will predict training outcomes based on wearable health data. Unlike mobile health apps, it uses real, diverse biometric data from wearable devices and is tailored toward amateurs.

## Target User
**Primary -** Amateur Athletes, want performance predictors and the ability to upload data and see if on track for fitness goals.

**Secondary -** Coaches, want performance predictors and more tailored suggestions for my athlete 

## User Stories 
- As an athlete, I want to be able to use data from my wearable device to inform my fitness journey. 
- As an athlete, I want to know what I can do to improve my athletic performance.
- As an athlete, I want to know why I’ve been given certain suggestions, and see projections for what happens if I do or don’t follow them.
- As a coach, I want to offer tailored suggestions to my athletes.
- As a coach, I want to be able to offer my own suggestions to my athletes, without relying completely on AI.

## Feasibility

## Tooling
Google Colab - Offers GPUs with generous compute time for training a model
Python - Easy to use programming language, already has libraries dedicated to machine learning (see below)
Pytorch - Existing machine learning library that lets one design their own model, will be useful for making our model

## Demo Sentence
At the end of two weeks, we will show a program predicting user training outcomes based on test data working end to end.

## Riskiest Assumption
1. (**RISKIEST**) Can find data from wearable devices that has athletic performance as one of the features
2. Model will be better able to predict performance than the user will
3. Can train a model that can predict performance based on this data
4. Normal people who wear smart devices want to improve their athletic performance

We change direction if we cannot find the necessary datasets.

## Evaluation
Our system will first be able to find a pattern between recordable health data and athletic performance. From there, it will detect and record health data within 5% of the values currently recorded by products on the market. It will also predict training outcomes within 10% of the actual measured outcomes. If these previous evaluations are met, then of amateur athletes who test the product, at least 90% will find the data that the product provides "understandable." 

## Related Work
[1] Alkasasbeh, Walaa Jumah et al. “Artificial intelligence and wearables in sport: performance, injury risk, and wellbeing.” Frontiers in artificial intelligence vol. 9 1838507. 29 May. 2026, doi:10.3389/frai.2026.1838507. [https://pmc.ncbi.nlm.nih.gov/articles/PMC13260332/](https://pmc.ncbi.nlm.nih.gov/articles/PMC13260332/)

Literature review of 57 articles on the use of AI in sports wearables, a good starting point for seeing what work has already been done.

[2] Claudino, J.G., Capanema, D.d., de Souza, T.V. et al. Current Approaches to the Use of Artificial Intelligence for Injury Risk Assessment and Performance Prediction in Team Sports: a Systematic Review. Sports Med - Open 5, 28 (2019). [https://doi.org/10.1186/s40798-019-0202-3](https://doi.org/10.1186/s40798-019-0202-3)

Discusses the use of AI for team sports, leaves a gap in both wearables and individual athletes. 

[3] Migliaccio, G. M., Padulo, J., & Russo, L. (2024). The Impact of Wearable Technologies on Marginal Gains in Sports Performance: An Integrative Overview on Advances in Sports, Exercise, and Health. Applied Sciences, 14(15), 6649. [https://doi.org/10.3390/app14156649](https://doi.org/10.3390/app14156649)

Talks about how wearables can be used to measure athletic performance, leaves a gap in AI, mentions it as a promising future research.

[4] Seshadri DR, Thom ML, Harlow ER, Gabbett TJ, Geletka BJ, Hsu JJ, Drummond CK, Phelan DM and Voos JE (2021) Wearable Technology and Analytics as a Complementary Toolkit to Optimize Workload and to Reduce Injury Burden. Front. Sports Act. Living 2:630576. doi: 10.3389/fspor.2020.630576. [https://www.frontiersin.org/journals/sports-and-active-living/articles/10.3389/fspor.2020.630576/full](https://www.frontiersin.org/journals/sports-and-active-living/articles/10.3389/fspor.2020.630576/full)

Discusses the use of wearables to reduce injury, leaves a gap in both AI and athletic performance.

## On Harm
If the system is wrong, meaning it inaccurately predicts training outcomes and athletic performance, then the amateur athletes (and to a lesser extent the coaches) will be the most hurt. Athletes will have their athletic journey derailed, and will be behind on their goals. In the absolute worst case, the predictions could push users in the wrong direction, resulting in injuries common due to over exertion (such as shin splints from running, or pulling muscles from weight lifting). 
