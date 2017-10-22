The goal of this project is to demonstrate open, reproducible research with an example of gathering and graphing the page views for the English Wikipedia site (en.wikipedia.org). The included Python Jupyter notebook outlines, step by step, how to gather the data from the API calls to the MediaWiki data servers, how arrange the data into logical tables and performance basic processing such as computing sums, and how graph the time-series data. 
All source data was gathered from the Wikimedia Foundation REST API provided under a CC-BY-SA 3.0 license. See the Wikimedia Foundation terms of use for more detail at: https://wikimediafoundation.org/wiki/Terms_of_Use

The documentation for the Wikimedia Foundation REST API can be found at:
https://wikitech.wikimedia.org/wiki/Analytics/AQS/Legacy_Pagecounts
https://wikitech.wikimedia.org/wiki/Analytics/AQS/Pageviews

The final output data file is named ‘'en-wikipedia_traffic_200801-201709.csv' and contains eight fields described below. All missing or unavailable values were replaced with a numeric value of zero. 
Year – year of the observation
Month – month of the observation
pagecount_all_views – number of pages views, desktop and mobile, from the legacy Pagecount API
pagecount_desktop_views – number of page views originating from the desktop site from the legacy Pagecount API
pagecount_mobile_views – number of page views originating from the mobile site from the legacy Pagecount API
pageview_all_views – number of page views, desktop and mobile, from the Pageview API
pageview_desktop_views – number of page views originating from the desktop site from the Pageview API
pageview_mobile_views – number of page views originating from mobile devices from the Pageview API

Other files includes are: 
hcds-a1-data-curation.ipynb – the Python Jupyter notebook with all source commands
5 JSON files storing the retrieved API data locally

Limitations
The number of page views from the legacy Pagecount API differ than that of the Pageview API. The legacy Pagecount includes traffic that was a result of web crawlers, which are excluded in the results from the Pageview API.
