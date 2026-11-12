.. title:: SEO Panel Keyword Checker | SERP Tracker & Position Reports

.. meta::
   :description: Guide for seo panel Keyword position checker, SERP Tracker, Import keywords,  Keyword Management in google, yahoo, bing etc 


Keyword Management
~~~~~~~~~~~~~~~~~~~~~

~~~~~~~~~~~~~~
Create Keyword
~~~~~~~~~~~~~~

Next step is to create keywords under websites

1) Go to **Seo Tools => Keyword Position Checker => New Keyword**

2) Enter details as following screen shot

   .. image:: ../_static/sp_keyword_add.png

   - **Name** - Add keyword to search in search engine 
   
   - **Website** - The website needs to be checked with keyword search results

   - **Language** - The language in which keyword search to be done. If you are using **localized search engines like google.de**, no need to select language.
   
   - **Country** - The country in which keyword search to be done. If you are using **localized search engines like google.de**, no need to select language.
   
   - **Search Engine** - Select the search engines in which keyword needs to checked. **Click on 'Select All'** to select all or use **`CTRL`** key to select multiple entries.
   
   
You can also **edit, activate, deactivate and delete** keywords using options available in the **Keyword Manager** page.

~~~~~~~~~~~~~~~
Import Keywords
~~~~~~~~~~~~~~~

You can also **import group of keywords** to seo panel using this feature. 

1) Go to **Seo Tools => Keyword Position Checker => Import Keywords**

2) Enter details as following screen shot

   .. image:: ../_static/sp_keyword_import1.png
   
   - **Website** - The website needs to be checked with keyword search results
   
      **Click on `Crawl Meta Data`** link to get keywords of website. You can also edit this details before proceed. 

   - **Language** - The language in which keyword search to be done. If you are using **localized search engines like google.de**, no need to select language.
   
   - **Country** - The country in which keyword search to be done. If you are using **localized search engines like google.de**, no need to select language.
   
   - **Search Engine** - Select the search engines in which keyword needs to checked. **Click on 'Select All'** to select all or use **`CTRL`** key to select multiple entries.
   
   - **Keywords** - Add keywords to be imported to seo panel separated with comma *Eg:* google seo tools,seo tools,seo

3) Proceed with the values in the form, you will get following window with the stats of import.

   .. image:: ../_static/sp_keyword_import2.png


~~~~~~~~~~~~~~~~~~~~~~
Quick Position Checker
~~~~~~~~~~~~~~~~~~~~~~

This feature used to find the **rank of a website** in keyword search results by **with out storing any data** in database. 

1) Go to **Seo Tools => Keyword Position Checker => Quick Position Checker**

2) Enter details as following screen shot

   .. image:: ../_static/sp_keyword_quick_position.png
   
   - **Search Engine** - Select the search engines in which keyword needs to checked 

   - **Language** - The language in which keyword search to be done. If you are using **localized search engines like google.de**, no need to select language.
   
   - **Country** - The country in which keyword search to be done. If you are using **localized search engines like google.de**, no need to select language.
   
   - **Website** - The website needs to be checked in keyword search results
   
   - **Keyword** - Add keyword to search in search engine
   
   - **Show All results** - Checked to see all results in of keyword search in search engine


.. _keyword-position-summary:

~~~~~~~~~~~~~~~~~~~~~~~~~
Keyword Position Summary
~~~~~~~~~~~~~~~~~~~~~~~~~

A sortable table comparing every active keyword's rank on a "from" and a "to" date, across all your websites or one chosen website. Two columns here are new in Seo Panel 7.0.0: **AI Overview** and **Search Volume**.

1) Go to **Seo Tools => Keyword Position Checker => Keyword Position Summary**

2) Filter by **Name**, **Website** and **Period** (Day/Week/Month/Year, or your own two dates), then click **Search**

   .. image:: ../_static/sp_report_search_volume.png

   - **AI Overview (Google)** - Whether that keyword currently triggers a Google AI Overview, and whether you're **Cited** inside it (with your citation position, *Eg:* ``Cited (#2)``) - needs SERP Checker enabled under **DataForSEO Settings** or **Seo Panel API Settings**

   - **Search Volume (Google)** - Monthly search volume for that keyword - needs **Enable for Search Volume** turned on under **DataForSEO Settings** or **Seo Panel API Settings**

   - Either column shows **-** for a keyword that hasn't been checked yet, not zero - don't read a dash as "no searches"

   - Period is anchored to the latest date that actually has saved data for that keyword, not today's date, so results stay populated even if a cron run is behind schedule


~~~~~~~~~~~~~~~~~~~~
SERP Results Archive
~~~~~~~~~~~~~~~~~~~~

For a chosen website and keyword, shows the full organic result list from the most recent saved search-engine results page, one tab per search engine. Your own website's result is highlighted when it appears, and - new in 7.0.0 - Google's AI Overview presence/citation data is shown when available.

1) Go to **Seo Tools => Keyword Position Checker => SERP Results Archive**

2) Pick a **Website** and **Keyword**, then click **Go**

   .. image:: ../_static/sp_report_serparchive_aio.png

   - This fills in automatically from your regular Keyword Position Checker runs - no separate setup needed, beyond enabling SERP Checker under **DataForSEO Settings** or **Seo Panel API Settings** if you want the AI Overview block to appear at all

   - The **AI Overview** card shows **Present/Not present**, whether you're **Cited** and at what position, how many **Sources** were cited, and which provider (DataForSEO or Seo Panel API) and date the check ran

   - A keyword only appears here once it has a saved snapshot for at least one search engine
