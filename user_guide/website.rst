.. title:: Seo panel website Manager guide to manage seo panel websites

.. meta::
   :description: Guide for Seo panel website Manager to add, edit, import, delete, activate websites of seo panel.


Website Management
~~~~~~~~~~~~~~~~~~~~~

~~~~~~~~~~~~~~
Create Website
~~~~~~~~~~~~~~

After installation of seo panel, next step is to create website.

1) Go to **Admin Panel => Website Manager => New Website**

2) Enter details as following screen shot

   .. image:: ../_static/sp_website_add.png

   - **User** - The owner of the website  *Eg:* spadmin
   
   - **Name** - The name of the website  *Eg:* Seo Panel

   - **Url** - The url to website page   *Eg:* https://www.seopanel.org/
   
      **Click on `Crawl Meta Data`** link to get the following details of website. You can also edit this details later. 
   
   - **Title** - The title of the website
   
   - **Description** - The description of the website
   
   - **Keywords** - The keywords related to the website

   
You can also **edit, activate, deactivate and delete** websites using options available in the **Website Manager** page.

   
~~~~~~~~~~~~~~~
Import Websites
~~~~~~~~~~~~~~~

You can also **import group of websites** to seo panel using this feature. 

1) Go to **Admin Panel => Website Manager => Import Websites**

2) Enter details as following screen shot

   .. image:: ../_static/sp_website_import1.png

   - **User** - The owner of the website  *Eg:* spadmin
   
   - **Website CSV File:** - The group of websites added in csv format
   
      **CSV format:**
      
      *name, url, meta title, meta description, meta keywords, status*
            
   
      **Click on `Sample CSV File`** link to get sample csv file and create your website csv file using it.
            
   
   - **Delimiter** - The delimiter character used in the csv format(default value is coma **`,`**)
   
   - **Enclosure** - The enclosure character used in the csv format when value contains delimiter(default value is double quotes **`"`**). *Eg:* `mango,orange`
   
   - **Escape** - The escape character used in the csv format(Default value is forward backslash **`\\`**)


3) Proceed with the values in the form, you will get following window with the stats of import.

   .. image:: ../_static/sp_website_import2.png
    