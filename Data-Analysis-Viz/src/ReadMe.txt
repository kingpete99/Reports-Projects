Order of execution for the Jupyter Notebooks is important, as the output 
of one notebook will often be a CSV file that a follow-on notebook will need.
This is a consequence of our workflow as a distributed team working on 
separate notebooks.

Also, the first notebook (0--Install_Libraries.ipynb) installs several libraries
that may not be present by default in a typical Jupyter environment.
PLEASE RUN THIS NOTEBOOK FIRST!  (Although we're told using requirements.txt 
will make this unnecessary).

Run notebooks in this order:

0--Install_Libraries
1-A-BRFSS_Download
2-K-Fetch_daylight_data
3-A-BRFSS_EDA
4-K-Daylight_EDA
5-V-Merge_datasets
6-A-Depression_Index_Analysis
7-K-Combined_Analysis
8-V-Combined_Visualizations

Finally, a couple notes on acquiring the datasets:

1. The code used to download the BRFSS dataset may take several minutes to run.

2. The code used to fetch 'daylight' data from the USNO API also takes several 
minutes to run.  It failed one time due to a server timeout on the USNO end, 
but has otherwise run without incident.  The 'daylight.csv' file that it 
ultimately produces is included in full in the 'src/data' folder of the 
ZIP file.