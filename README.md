# data-512-homework_1

**Project Goal:** The goal of this project is to acquire page views data from Wikipedia and perform simple data processing and analyses of that data before visualizing the results.

**Source Data:** The license of the source data is the CC0 1.0 license (https://creativecommons.org/publicdomain/zero/1.0/). Here is a link to the Wikimedia Foundation REST API terms of use: https://www.mediawiki.org/wiki/REST_API#Terms_and_conditions. 

**API Documentation:** 
- https://wikimedia.org/api/rest_v1/#/Pageviews%20data
- https://www.mediawiki.org/wiki/Wikimedia_REST_API
- https://wikitech.wikimedia.org/wiki/Analytics/AQS/Pageviews
- https://wikimedia.org/api/rest_v1/#/Pageviews_data/get_metrics_pageviews_aggregate_project_access_agent_granularity_start_end

**Data Files:**
- Intermeadiary data files:
  - thank_the_academy.AUG.2023.csv - debug.xlsx
    - This file contains two columns of data. The first, called 'name'
      contains the name of each article in the list of movies, and the second, called 'url' contains the url to every page.
- Final output data files:
  - 'academy_monthly_desktop_201507-202309.json':
    - This file contains the monthly desktop page view data corresponding
      to the list of movies in 'thank_the_academy.AUG.2023.csv'. The data is 
      structured as JSON and contains a dictionary, where each key is an article name and each value is a list of elements, where each element is a dictionary representing a month of data. The month dictionary contains the following attributes: 
      {
            "project": ,
            "article": ,
            "granularity": ,
            "timestamp": ,
            "agent": ,
            "views": 
        },
  - 'academy_monthly_mobile_201507-202309.json':
    - Simillar to the desktop data file, This file contains the monthly mobile page view data corresponding to the list of movies in 'thank_the_academy.AUG.2023.csv'. The data is structured as JSON and contains a dictionary, where each key is an article name and each value is a list of elements, where each element is a dictionary representing a month of data. The month dictionary contains the following attributes: 
      {
            "project": ,
            "article": ,
            "granularity": ,
            "timestamp": ,
            "agent": ,
            "views": 
        },
  - 'academy_monthly_cumulative_201507-202309.json':
    - Simillar to the previous data files, This file contains the monthly cumulative page view data corresponding to the list of movies in 'thank_the_academy.AUG.2023.csv', where the mobile and desktop access page view counts are added together. The data is structured as JSON and contains a dictionary, where each key is an article name and each value is a list of elements, where each element is a dictionary representing a month of data. The month dictionary contains the following attributes: 
      {
            "project": ,
            "article": ,
            "granularity": ,
            "timestamp": ,
            "agent": ,
            "views": 
        },