## Effectiveness of STD Drugs

## Problem Statement

According to a CDC Report, over 2.4 million cases of sexually transmitted diseases (STDs) were reported in the United States of America in 2018. The report also highlighted a whopping 22% increase from 2017 to 2018 in the number of newborn deaths due to Syphilis.

In the light of upcoming World Health Day, we intend to raise awareness about various STDs and drugs used to cure them. 

A new pharmaceutical startup is recently acquired by one of the world's largest MNCs. For the acquisition process, the startup is required to tabulate all drugs that they have sold and account for each drug's effectiveness. A dedicated team has been assigned the task to analyze all the data. This data has been collected over the years and it contains data points such as the drug's name, reviews by customers, popularity and use cases of the drug, and so on. Members of this team are by the noise present in the data.

## Dataset Description

The dataset has the following columns:

 Variable Name			Description

- patient_id		->	ID of patients
- name _of_drug		->	Name of the drug prescribed
- use_case_fro_drug	->	Purpose of the drug
- review_by_patient	->	Review by patient
- drug_approved_by_UIC		Date of approval of the drug by UIC
- number_of_times_prescribed  ->	Number of times the drug is prescribed
- effectiveness_rating	    ->	Effectiveness of drug
- base_score		    ->	Generated score(Target Variable)

## Evalutaion Metric

score = {100* max(0,1-RMSE(actual\_values,predicted\_values))}

## Private Leaderboard
**Rank - 3**
