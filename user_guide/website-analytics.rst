.. title:: SEO Panel Website Analytics | Google Analytics Integration

.. meta::
   :description: Guide for Seo panel google analytics integration and reports generation. Website clicks and sources are stored and displyed in reports.


Website Analytics
~~~~~~~~~~~~~~~~~~

Reads Google Analytics (GA4) data for your websites, broken down by traffic source - users, new users, sessions, bounce rate, average session duration and goal completions. Needs Google Analytics connected first under **Admin Panel => My Account => Connections** (see :doc:`google_connection`) with a GA4 property configured for the website; every report below except Quick Checker also needs the daily sync to have run before it shows anything.

~~~~~~~~~~~~~~~~~
Report Summary
~~~~~~~~~~~~~~~~~

The default Website Analytics screen. For one chosen website, compares each traffic source's metrics between two dates, with the change highlighted.

1) Go to **Seo Tools => Website Analytics => Report Summary**

2) Pick a **Website** and **Period** (Day/Week/Month/Year, or your own two dates), then click **Search**

   .. image:: ../_static/sp_analytics_summary.png

   - Day/Week/Month/Year is anchored to the latest date that actually has synced data, not today's date


~~~~~~~~~~~~~~
Quick Checker
~~~~~~~~~~~~~~

Unlike every other report on this page, this calls the Google Analytics API **live** - nothing is saved.

1) Go to **Seo Tools => Website Analytics => Quick Checker** (only shown when enabled for your account)

2) Pick a **Website** and date range, then click **Proceed**

   .. image:: ../_static/sp_analytics_quick_checker.png


~~~~~~~~~~~~~~~~
Detailed Reports
~~~~~~~~~~~~~~~~

A day-by-day table of one website's metrics for one traffic source over a date range, from already-synced GA4 data, with day-over-day change highlighted.

1) Go to **Seo Tools => Website Analytics => Detailed Reports**

2) Pick a **Website**, traffic **Source** and **Period**, then click **Show Records**

   .. image:: ../_static/sp_analytics_reports.png


~~~~~~~~~~~~~~~~~~
Graphical Reports
~~~~~~~~~~~~~~~~~~

Charts a per-source Google Analytics metric over time for one website, instead of showing it as a table. Bounce rate is excluded from the combined chart by default, since it's an inverse metric.

1) Go to **Seo Tools => Website Analytics => Graphical Reports**

2) Pick a **Website**, traffic **Source**, metric and **Period**, then click **Show Records**
