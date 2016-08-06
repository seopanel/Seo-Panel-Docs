~~~~~~~~~~~~~~
Create Project
~~~~~~~~~~~~~~

This section will help you to audit your website to know the stats related to SEO

1) Go to **Seo Tools => Site Auditor => Auditor Projects**

2) **Click on 'New Project' button**

3) Enter details as following screen shot

   .. image:: _static/sp_create_auditor_project.png

   - **Website** - Select a website needs to be audited

   - **Maximum number of pages to be checked** - Maximum number of pages needs to be audited(default value is `500`, it can be changed from `Auditor Settings`)  

   - **Exclude links** - Insert links separated with comma needs to be excluded to prevent infinite links in reports. **Eg:** /plugin/l/, &lang_code=

   - **Check pagerank of pages** - Check pagerank of pages(**Note:** it will increase the execution time of a project)

   - **Check backlinks of pages** - Check backlinks of pages(**Note:** it will increase the execution time of a project)

   - **Check pages indexed or not** - Check index status of pages(**Note:** it will increase the execution time of a project)

   - **Store all links found in a page** - Store links found in pages for more detailed reports

   - **Check broken links in a page** - Check brocken links in pages(**Note:** it will increase the execution time of a project)

   - **Execute with cron** - Execute report generation with cron job. We recommened to **select 'Yes'** for better report generation.
   
   
You can also **edit, activate, deactivate and delete** projects using options available in the **Auditor Projects** page.


~~~~~~~~~~~~~~~~
Generate Reports
~~~~~~~~~~~~~~~~

This section help you to generate reports of site auditor projects.

We have 2 methods to generate reports, we **recommend to use cron job** method for report generation.

   - Cron Job
   
   1) Go to **Seo Tools => Site Auditor => Cron Command**
   
   2) Add following command to your cron tab

      .. code-block:: bash

         */15 * * * * php /opt/lampp/htdocs/seopanel/siteauditorcron.php
    
   
   - Manual Report Generation
   
   1) Go to **Seo Tools => Site Auditor => Auditor Projects**
   
   2) **Select 'Run Project'** from `Action` select box of corresponding project and proceed.
   
      You will get a window like following screen shot with stats.
   
    .. image:: _static/sp_auditor_report_generation.png
   
 
 
~~~~~~~~~~~~~~~
Auditor Reports
~~~~~~~~~~~~~~~

This section will help you to understand different types of site auditor reports

1) Go to **Seo Tools => Site Auditor => Auditor Reports**

2) Reports
    .. image:: _static/sp_auditor_reports.png