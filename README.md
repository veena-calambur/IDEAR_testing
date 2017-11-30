# IDEAR_testing

## Objective
This code essentially mimics how IDEAR should have worked, particularly around target leak detection but uses simpler formulas for some of the association calculations, rather than R packages to more easily tanslate to formulas that can be applied outside of the R environment 

## How to Run with your own data 
- Open up 2017_11_30_Test_IDEAR.R 
- Run the "Load Libraries" and "Define Helper Function" sections 
- Add in lines to read in your own data in the "Read Data" section 
- Go through the "Quick EDA" section to ensure your data is ready to run through IDEAR: 
  - Ensure that you don't have any missing data (fill in, or omit rows with missing data) 
  - Make sure that you have coded your data correctly (i.e. all categorical variables are factors, and all numeric variables are numerics) 
- Go to the "User Definition" section to specify the following: 
  - target: your taret variable
  - cols_to_exclude: any variables you wish to exclude fromt his analysis (i.e. ID variables, dates) 
  - data: the data set name 
- You should then run the code to define target_type which defines the data type of your target variable, and data_cln which filters out any columns you specified in cols_to_exclude 
- You are then good to go to run the idear sample with the following command: 
  ##### run_sample_idear(data_cln, target_type) #####
  
- You will find that some of the summary outputs will print to the console, but majority of these relationships will be visualized in the plot window, and when the code is done running you can click through all of the plots generated to better understand the variables in the data set, and how they relate to the target and each other 
