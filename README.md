The goal of this assingment was to investigate bias in data while exploring English Wikipedia data. The end goal is to show
* the countries with the greatest and least coverage of politicians on Wikipedia compared to their population.
* the countries with the highest and lowest proportion of high quality articles about politicians.

Original data sources
The original data sources used come from two different places. The first is from Oliver Keyes found at https://figshare.com/articles/Untitled_Item/5513449. The data of Politicians by Country from the English-language Wikipedia is released under a CC-BY-SA 4.0 license. 

The second data source is from PRB found at http://www.prb.org/DataFinder/Topic/Rankings.aspx?ind=14. The data of country population from mid-2015 is released under general copyright. 
 
Also, a Wikimedia API endpoint for a machine learning system called ORES ("Objective Revision Evaluation Service") found at https://www.mediawiki.org/wiki/ORES and documentaiton found at https://ores.wikimedia.org/v3/#!/scoring/get_v3_scores_context_revid_model. ORES estimates the quality of an article (at a particular point in time), and assigns a series of probabilities that the article is in one of 6 quality categories. The options are, from best to worst:

FA - Featured article
GA - Good article
B - B-class article
C - C-class article
Start - Start-class article
Stub - Stub-class article

The final output data file is named ‘'.csv' and contains eight fields described below. All missing or unavailable values were replaced with a numeric value of zero. 


Other files includes are: 
hcds-a1-data-curation.ipynb – the Python Jupyter notebook with all source commands
5 JSON files storing the retrieved API data locally

Limitations
The analysis and conclusions are limited to the countries with where represented in both data set and represented in the English Wikipedia.