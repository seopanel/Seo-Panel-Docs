.. title:: SEO Panel logs manager, Crawl log manager, Proxy log manager 

.. meta::
   :description: Guide for SEO Panel logs manager, Crawl log manager, Proxy log manager with complete details. 



Logs Manager
~~~~~~~~~~~~~~~~~~

~~~~~~~~~~~~~~~~~~
Crawl Log Manager
~~~~~~~~~~~~~~~~~~

In this section we will manage all crawl logs of the system.

1) Go to **Admin Panel => Logs Manager => Crawl Log Manager**

2) Check details in following screen shot

   .. image:: ../_static/sp_crawl_log1.png
   
   **Search Filters**

   - **Search** - Enter a string to do common search through most of the log fields. `Eg:` website name or keyword name 

   - **Period** - Enter date interval to filter the logs

   - **Status** - Select status of log to filter[Success / Fail]

   - **Report Type** - You can select different reports types

      - **Keyword** - Select to get keyword logs only
      
      - **Other** - Select to get other logs excluding keywords

   - **Search Engine** - Select particular search engine to filter the logs
   
   - **Proxy** - Select particular proxy to filter the logs
   
   
   **Display Columns**

   - **Reference** - The object crawled in seo panel. `Eg:` website url, keyword name etc

   - **Subject** - The object crawled through which subject `Eg:` search engine name
   
   - **Details** - The details of the crawl log and it help us to find the root cause of errors
   
   - **Action** - Using it we can delete a particular log. Using bottom 'Delete' button we can delete 
   
   
   Using bottom 'Clear All Logs' button, we can delete all logs in the system.
    
   `Note:` Also **daily cron job** will **delete all logs before 3 months**. 
   
   
3) **Click on 'Id'** in logs reports will show more detailed report of a crawl log

   .. image:: ../_static/sp_crawl_log2.png
	
   It will show details like cookie, Referer, Post Fields, User agent etc
   
   