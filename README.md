# Prediction-of-inhibitor-development-HA
Prediction of inhibitor development in previously untreated and minimally treated children with severe and moderately-severe hemophilia A using a machine-learning network  JTH (2024)

https://doi.org/10.1016/j.jtha.2024.05.017

The objective of this repository is to provide access to the trained model for use and validation in other cohorts.

The necessary files for use are available via the following link:

https://drive.google.com/file/d/1AJJ1OmYYeNQmCVLgoYRhCp5ocvxrfJdk/view?usp=drive_link

The description of the variables and the format in which they should be inputted can be found in the variables.xlsx file and the test sheet, test_file.xlsx.

All files must be extracted into the working directory to be modified in the testing.R file. This is the default directory. (required packages: igraph (version 1.2.5), readxl (version 1.3.1) and stringr (version 1.4.0)).

setwd("D:/hemofilia_github")

To test the model, simply run the testing.R file in RStudio. 

The model will then return a ‘final_results.csv’ spreadsheet in the same working directory.
F
or each patient tested, the ‘robustness’ column will measure the degree of information provided by the patient's variables. A value of 0 will indicate low confidence, while a value of 1 will indicate high confidence. A value of 0 indicates that the patient provided minimal or no relevant information, while a value of 1 signifies that the patient provided all relevant information.

The 'warning' column comprises three levels: low, medium, and high, which represent the degree of attention that the healthcare professional should pay to the patient.

Three probabilities are provided for inhibitor development (%).

"Min_probability" "Max_probability" and "True_probability".

The probability of inhibitor development for the patient is situated between the minimum and maximum values. The true probability indicates the likelihood of inhibitor development for the patient.

If you encounter any difficulties in utilizing the trained model, please contact us via email at tiagoschieber@face.ufmg.br.

