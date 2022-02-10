### INFT COURSEWORK ###

Please note, I used AWS to generate my data because my laptop was simply too slow.
Specifically, I uploaded a set of files to AWS SageMaker Jupyter-Lab nodes, and used these to generate simulation data. 
I then transferred the simulation data from the SageMaker nodes to S3, and from there to my laptop. 
From there, I performed data analysis using R, because I've become very familiar with the TidyVerse package during the SCEM module. 

The sub-folders you will find are:
1. k_scripts
2. m_scripts

k_scripts contains the files uploaded to AWS to run the simulations for the first experiment (changing k):
    a) BSE.py
    b) upload_files_s3: for uploading the generated simulation CSV files to an S3 bucket
    c) k_generate_data: for defining the market conditions and running the simulations
    
m_scripts contains the files uploaded to AWS to run the simulations for the second experiment (changing the mutation function):
    a) BSE.py (with all of the custom mutation functions added, which have different names to the default)
    b) upload_files_s3: same as above
    c) m_generate_data: for defining the market conditions and running the simulations

There is also an R-markdown file, PRSH_statistical_analysis.Rmd, which I used for data analysis on the generated data.