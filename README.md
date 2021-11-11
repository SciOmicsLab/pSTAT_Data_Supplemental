# pSTAT_Data_Supplemental
Data and R analysis for Simultaneous assessment of eight phosphorylated STAT residues in T-cells by flow cytometry

## System Requirements
To run the analysis R code with the existing data, you'll need Docker installed, and a user login to https://hub.docker.com.  To verify this is working correctly, type the following at a command prompt:
 
`docker help`

This should return a help menu.

`docker login`

Login succeeded…


It is recommended you increase the amount of Memory allocated to Docker.  This was tested allocating at least 6 GB if available instead of the default which is 2 GB. Docker Dashboard has this setting under Preferences -> Resources -> Memory.  
 
## Instructions 
To download and execute the code with the dataset used for this paper:

1.	After cloning this git repository, make sure you are in a Terminal window in the pSTAT_Data_Supplemental directory.
2.	Run:
`docker run -e PASSWORD=pstat --rm -p 8787:8787 -v "$(pwd):/home/rstudio" --name pstat_data_supplemental sciomicslab/pstat_data_supplemental`
3.	Open a browser window to http://localhost:8787


    Provide username: rstudio

    Password: pstat 

4. Locate the R Markdown (.Rmd) file under Files and double click to open.
5. Run or step through the code by clicking one of the Run options. Output plots produced are saved to a Figs folder and displayed interactively in the code window for review.

To replace datasets with your own, you may edit the input files to suit your own analysis needs.  You may also edit the Rmd code as you see fit.  The author(s) assume you have enough R, git, and Docker knowledge to leverage this working example, and apologize that no technical support can be offered. 


Ctl-C in the terminal will kill the web server and exit.  You can also docker container commands, or use Docker Desktop to stop the container when finished. 


## Resources:
The Docker image is FROM bioconductor/bioconductor_docker which includes Rocker's Rstudio access.  
Also installed are


| Package | Version |
| --- | --- |
| R | 4.1.1 |
| tidyverse | 1.3.1 |
| Polychrome | 1.3.1 |
| ggpubr | 0.4.0 |
| flowCore | 2.6.0 |
| kableExtra | 1.3.4 |
| knitR | 1.36 |
| Hmisc | 4.6-0 |
| igraph | 1.2.8 |


