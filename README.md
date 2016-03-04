# README file
# Coursera-Getting-and-Cleaning-Data

Programming assignments for the Coursera Getting and Cleaning Data Data Science Specialization

The purpose of assigment is to download, parse and clean data collected from the accelerometers from the Samsung Galaxy S smartphone. A full description, and purpose of the research, is available at the site where the data was obtained:

http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones

Run run_analysis.R, an R script which does the following:

    1. Download the .zip file with the data to analyze.
    2. Load files activity_labels.txt, features.txt
    3. Load files y_test.txt, X_test.txt, y_train.txt, X_train.txt
    4. Label y_*.txt, X_*.txt with the appropiate labels from activity_labels.txt, features.txt
    5. Merge test and activity datasets
    6. Creates a tidy dataset that consists of the average (mean) value of each variable for each subject and activity pair.

The end result is shown in the file tidy.txt.
