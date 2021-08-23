# University of Rochester Biomedical Data Science Hackathon Summer 2021

[**Final scores!**](https://rochester-biomedical-ds.github.io/Hackathon-Summer-2021/Leaderboard.html) See below for a list of prize winners.


# Logistics

<!-- 0.   Registration is open until 5PM Sunday 8/15.  Teams can consist of up to 4 people. Register by using the google form. -->
0.   Each team must have a github handle associated with it in order to participate.  Make sure you edit your registration or email the organizers to provide this, if you haven't yet.
1.   You may add team members up
to noon EDT on 8/19 by editing your response to the google form or emailing the organizers.
2.  Teams of entirely undergraduates will be in the undergraduate
division, else they will be in the open division.
3.  Predictions on test data set are submitted by pushing to
    github.  A repository with the name `Hackathon-Summer-2021`,
    owned by the team captain, will
    be queried for a file named [prediction/prediction.csv](prediction/prediction.csv).  **If the team captain forks this
    repository and writes predictions there everything should work
    (as long as the predictions are formatted correctly).**
2.  Predictions will be scored at least once daily, starting 8/18, with
    scores posted by noon.  At
    the organizers' option, predictions may be scored more frequently
    than this.
2.  General questions/problems can be directed to [issues](https://github.com/Rochester-Biomedical-DS/Hackathon-Summer-2021/issues) page.  We encourage other hackathon participants to respond to issues.
3.  The scoreboard will be located
    [here](https://rochester-biomedical-ds.github.io/Hackathon-Summer-2021/Leaderboard.html), and will be updated starting noon on 8/18.
    We  cannot provide support
    beyond the diagnostic output included on the scoreboard if an error is
    encountered in scoring your predictions.
5.  Interim scoring may employ forms of randomization (e.g. bootstrapping) from the test data set.  The final scores will use all the data and not be randomized.
4.  Competition runs through 11:59 PM EDT 22-August-2021.  The predictions each team has committed to their repository at that time will be used to determine their final score.

# Data

*  Training data are [here](train_data/).  The label you are to predict is `age` and is available in [train_data/train_labels.csv](train_data/train_labels.csv).  The `group` covariate indicates what cohort (study) the `sample_id` was from.  The features available for prediction are in [train_data/train_expression.csv.gz](train_data/train_expression.csv.gz)--rows are samples and are in the same order as train_labels.csv.  Columns are features.   [train_data/train_features_names.csv](train_data/train_features_names.csv) contain gene symbol names for all the features.  The data are also available as an R [SummarizedExperiment](https://bioconductor.org/packages/release/bioc/vignettes/SummarizedExperiment/inst/doc/SummarizedExperiment.html), [train_data/train_summarized_experiment.rds](train_data/train_summarized_experiment.rds).
*  Test data are [here](test_data/), and are the same format as train data.  
*  Your predictions should be in the order of the `sample_id`s [listed here](prediction/prediction.csv).  The first column will be examined, regardless of column name.  No join is performed on the `sample_id` column.

# Data Description

The data are unnormalized counts of various genes from RNASeq performed on various patients.  The goal is to predict the patient's age at sampling from their RNAseq profile.


# Prizes
1.  First place in each division: $300 + $75*(team size)
2.  Second place in each division: 0 + $50*(team size)
1.  Predictions will be scored based on mean square error, lower
values are better.
1.  In order to claim your prize, you will need to fill out a post-competition survey.

In addition, winning teams will have the opportunity to present their solutions at a meeting of participants and faculty this fall.

# Winners!
**Congratulations to the winning teams:**
 * 1st place Undergraduate division- Bigcitybois
 * 2nd place Undergraduate division- 21_techfacts
 * 1st place Open division - Supergene 
 * 2nd place Open division- The missile knows where it is at all times.

If your team's final MSE was <172.15, your prediction beat random guessing and you will receive a prize! 
* All individuals in the following teams will receive a prize: Supergene, BigCityBois, 21_techfacts, The missile knows where it is at all times, Yangxin, VIStA H., abhnv123, Ayo, Always Last, haoyunlai, elongan, Andrew Dettor, Team AF.
* In order to claim your prize, you will need to **fill out two forms**: a post-competition [survey](https://forms.gle/7dKqhc7eVjQRWpZg7) and the following information [form](https://forms.gle/nuEriNzLUB54VBeS9). Your responses to the survey are anonymous.

# Feedback and post-event information
Thank you for participating in this competition! We hope that you enjoyed the event. Please give us feedback so that we can improve future events.
* **Fill out the post-competition [survey](https://forms.gle/7dKqhc7eVjQRWpZg7).** 
* If your team submitted predictions and you would like to receive a certificate of participation, please e-mail alarracu@bio.rochester.edu. 
* Some of the winning teams will present their approach to the hackathon in an upcoming meeting of the GIDS working group in life and biomedical data science. You are all invited. Details about the meeting will come via e-mail once it is scheduled.
