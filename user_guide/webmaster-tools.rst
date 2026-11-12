.. title:: SEO Panel Webmaster Tools | Google Integration & Reports

.. meta::
   :description: Guide for Seo panel google webmaster tools integration and reports generation. Website clicks and impressions are stored and displyed in reports.


Webmaster Tools
~~~~~~~~~~~~~~~~

Reads Google Search Console data for your websites - clicks, impressions, CTR and average position, at both the website and keyword level. Needs Google Search Console connected first under **Admin Panel => My Account => Connections** (see :doc:`google_connection`); every report below except Quick Checker also needs at least one daily sync to have run before it shows anything.

~~~~~~~~~~~~~~~~~~~~~~
Keyword Search Summary
~~~~~~~~~~~~~~~~~~~~~~

The default Webmaster Tools screen. For one chosen website, compares each tracked keyword's clicks, impressions, CTR and average position between two dates, with the change highlighted.

1) Go to **Seo Tools => Webmaster Tools => Keyword Search Summary**

2) Pick a **Website** and **Period** (Day/Week/Month/Year, or your own two dates), then click **Search**

   .. image:: ../_static/sp_webmaster_keyword_summary.png

   - Reads already-saved Search Console data, so it needs the daily sync to have run before this shows anything
   - Day/Week/Month/Year is anchored to the latest date that actually has synced data, not today's date


~~~~~~~~~~~~~~
Quick Checker
~~~~~~~~~~~~~~

Unlike every other report on this page, this queries Google Search Console **live** - nothing is saved.

1) Go to **Seo Tools => Webmaster Tools => Quick Checker** (only shown when the Quick Checker feature is enabled)

2) Pick a **Website** and date range, optionally a specific **Keyword**, then click **Proceed**

   .. image:: ../_static/sp_webmaster_quick_checker.png

   - Shows overall clicks/impressions/CTR/average position, plus a per-keyword breakdown, right now
   - Since this calls the Google API live rather than reading saved data, it works even before a daily sync has ever run


~~~~~~~~~~~~~~~~~~~~~~
Keyword Search Reports
~~~~~~~~~~~~~~~~~~~~~~

A day-by-day table of clicks/impressions/CTR/average position for one keyword (or every keyword of a website) over a date range, from already-synced Search Console data.

1) Go to **Seo Tools => Webmaster Tools => Keyword Search Reports**

2) Pick a **Website**, **Period**, and optionally a **Keyword**, then click **Show Records**

   .. image:: ../_static/sp_webmaster_keyword_reports.png


~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Graphical Reports (Keyword)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Charts one or more Search Console metrics (clicks, impressions, CTR, average position) over time for a keyword, instead of a table.

1) Go to **Seo Tools => Webmaster Tools => Graphical Reports (Keyword)**

2) Pick a **Website**, **Keyword**, **Period** and **Report Type**, then click **Show Records**


~~~~~~~~~~~~~~~~~~~~~~
Website Search Summary
~~~~~~~~~~~~~~~~~~~~~~

Compares a website's overall Search Console metrics between two saved dates, with the change highlighted.

1) Go to **Seo Tools => Webmaster Tools => Website Search Summary**

2) Pick a **Website** and **Period**, then click **Search**

   .. image:: ../_static/sp_webmaster_website_summary.png


~~~~~~~~~~~~~~~~~~~~~~
Website Search Reports
~~~~~~~~~~~~~~~~~~~~~~

A day-by-day table of a website's overall Search Console metrics, with day-over-day differences highlighted.

1) Go to **Seo Tools => Webmaster Tools => Website Search Reports**

2) Pick a **Website** and **Period**, then click **Show Records**

   .. image:: ../_static/sp_webmaster_website_reports.png


~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Graphical Reports (Website)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Charts a website's overall Search Console metrics over time, instead of a table.

1) Go to **Seo Tools => Webmaster Tools => Graphical Reports (Website)**

2) Pick a **Website**, **Period** and **Report Type**, then click **Show Records**


~~~~~~~~~
Sitemaps
~~~~~~~~~

A separate, lighter-weight tool also reached from this menu group: lets you generate and manage an XML sitemap for a website without needing Search Console connected at all.

1) Go to **Seo Tools => Webmaster Tools => Sitemaps**
