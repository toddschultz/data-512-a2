The goal of this assingment was to investigate bias in data while exploring English Wikipedia data. The end goal is to show
* the countries with the greatest and least coverage of politicians on Wikipedia compared to their population.
* the countries with the highest and lowest proportion of high quality articles about politicians.

# Original data sources
The original data sources used come from two different places. The first is from Oliver Keyes found at https://figshare.com/articles/Untitled_Item/5513449. The data of Politicians by Country from the English-language Wikipedia is released under a CC-BY-SA 4.0 license. 

The second data source is from PRB found at http://www.prb.org/DataFinder/Topic/Rankings.aspx?ind=14. The data of country population from mid-2015 is released under general copyright. 
 
Also, a Wikimedia API endpoint for a machine learning system called ORES ("Objective Revision Evaluation Service") found at https://www.mediawiki.org/wiki/ORES and documentaiton found at https://ores.wikimedia.org/v3/#!/scoring/get_v3_scores_context_revid_model. The ORES data is copyrighted by PRB. ORES estimates the quality of an article (at a particular point in time), and assigns a series of probabilities that the article is in one of 6 quality categories. The options are, from best to worst:

* FA - Featured article
* GA - Good article
* B - B-class article
* C - C-class article
* Start - Start-class article
* Stub - Stub-class article

The final output data file is named 'en-wikipedia_bias_2015a.csv' and contains the fields described below. All missing or unavailable values were removed via row-wise deleation. 

* country - name of the country
* article_name - name of the policitian
* revision_id - the Wikipedia identification number for the article
* article_quality - the article quality predicted by ORES
* population - the population of the country

# Included files
* hcds-a1-data-bias.ipynb – the Python Jupyter notebook outlining the entire analysis from data importing to graphing to conclusions.
* en-wikipedia_bias_2015a.csv - output csv file with country and article quality information
* countryDataCSV.csv -  output csv file with country, articles per population, and the percetage of high-quality articles
* Population Mid-2015.csv - population by country data from PRB
* PolbyCountry.csv -  csv file with the names of the policitians from each country provided by Oliver Keyes
* Bottom10ArticlesperPopulation.jpg - image of the graph of the bottom 10 countries for articles per population
* Bottom10HQArticlespercent.jpg - image of the graph of the bottom 10 countries for the percentage of high-quality articles
* Top10ArticlesperPopulation.jpg - image of the graph of the top 10 countries for articles per population
* Top10HQArticlespercent.jpg - image of the graph of the top 10 countries for the percentage of high-quality articles

Limitations
The analysis and conclusions are limited to the countries with where represented in both data set and represented in the English Wikipedia. The requirement to use only English Wikipedia articles likely will skew the results towards favoring native English language countries. 