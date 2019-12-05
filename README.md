# HealthRecSys datasets
This repository has been created to store open datasets in the field of health recommender systems (HealthRecSystem)/health information systems. All data is produced and provided by members of the Food Information Behaviour Collective (see https://ai.ur.de/fibc/).

## Nudging Healthier Choices (prediction study)

[Dataset: final_study_nudging_healthier_choices.csv](final_study_nudging_healthier_choices.csv)

This dataset was collected as part of research work on helping people to make healthier food choices by nudging. 

There were two algorithms, top10 and images, that used different features of online recipes to predict which of a given pair or recipes, A and B, a random user would likely choose. These recipes pairs were chosen such that the two recipes are similar in terms of their constituent ingredient but have a large percentage difference in their fat content per 100g. Research shows that, other things kept fixed, people typically choose fattier foods and so the idea was to choose similar pairs where we predicted that, despite this tendency, users would more frequently choose the healthier (i.e. less fatty) option.

For more information on this research, you can download the related SIGIR paper here: https://dl.acm.org/citation.cfm?id=3080826
To cite this work, please use the following citation:

Elsweiler, D., Trattner, C. and Harvey, M., 2017, August. Exploiting food choice biases for healthier recipe recommendation. In Proceedings of the 40th international acm sigir conference on research and development in information retrieval (pp. 575-584). ACM.

The data is strcutured as follows:

id - internal ID number for this specific trial

pair_id - internal ID number for the recipe pair

user_id - anonimised participant ID

q1 - the recipe the participant chose

algorithm - the algorithm used to generated the pairs and predictions (see the paper for details)

diff_fat - the difference in fat between the two recipes (fat_recipe1 - fat_recipe2)

correct_answer - the "correct" response (i.e. the least fatty recipe)

answer - the recipe the participant chose

gain - 1 when the algorithm correctly predicted the chosen recipe, 0 otherwise
