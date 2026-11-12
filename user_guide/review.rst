.. title:: SEO Panel Review Manager | Google, Yelp, Trustpilot & TripAdvisor

.. meta::
   :description: Guide for seo panel Review Manager - track review count and star rating for your Google My Business, Yelp, Trustpilot and TripAdvisor profiles.


Review Manager
~~~~~~~~~~~~~~~

Tracks review count and star rating for your business profiles over time - **Google My Business**, **Yelp**, **Trustpilot** and **TripAdvisor**. For Google, Trustpilot and TripAdvisor this runs through the **DataForSEO** API as an **async** job: a task is posted on one cron run and its results are fetched on the next, rather than scraping live and risking a timeout. Yelp has no such API and falls back to scraping its page directly. Needs DataForSEO configured under **Settings => DataForSEO Settings** (see :doc:`settings`) for the three DataForSEO-backed platforms - **Enable for Review Checker** specifically.

~~~~~~~~~~~~~~~
Report Summary
~~~~~~~~~~~~~~~

The default Review Manager screen. For one chosen website, compares each review link's review count and rating between two dates, with the change highlighted.

1) Go to **Seo Tools => Review Manager => Report Summary**

2) Pick a **Website** and **Period** (Day/Week/Month/Year, or your own two dates), then click **Search**

   .. image:: ../_static/sp_review_summary.png

   - Day/Week/Month/Year is anchored to the latest date that actually has saved data, not today's date
   - Needs at least one link added under **Review Links** below, and a day or more of history from the daily scheduled check


~~~~~~~~~~~~~~
Review Links
~~~~~~~~~~~~~~

Lists the review-profile links you've registered per website. A link must be created here before Report Summary, Detailed Reports or Graphical Reports have anything to show for it.

1) Go to **Seo Tools => Review Manager => Review Links**

2) Click **New Review Link**, pick a **Website** and **Type** (platform), and enter the profile **Link**

   .. image:: ../_static/sp_review_links.png

   - **Type** - **Google My Business**, **Yelp**, **Trustpilot** or **TripAdvisor**
   - **Link** - The full profile/listing URL for that platform, *Eg:* ``https://www.google.com/search?q=kfc+Damrak`` for Google
   - Activate, deactivate or delete a link from this same list
   - Link counts are capped by your account's plan


~~~~~~~~~~~~~~
Quick Checker
~~~~~~~~~~~~~~

Unlike every other tool here, this is an instant, unsaved preview - not part of the scheduled async check.

1) Go to **Seo Tools => Review Manager => Quick Checker**

2) Pick a **Type** (platform), paste a profile **Link**, then click **Proceed**

   .. image:: ../_static/sp_review_quick_checker.png

   - One-off check of a review page's current review count and star rating, without saving anything
   - For Google, Trustpilot and TripAdvisor this uses the DataForSEO API; Yelp falls back to scraping its page directly
   - DataForSEO-backed platforms need DataForSEO configured under **Settings => DataForSEO Settings** first


~~~~~~~~~~~~~~~~
Detailed Reports
~~~~~~~~~~~~~~~~

For one chosen link, a day-by-day history table of review count and rating over a date range, with each day's change from the previous one highlighted.

1) Go to **Seo Tools => Review Manager => Detailed Reports**

2) Pick a **Link** and **Period**, then click **Show Records**

   .. image:: ../_static/sp_review_detailed_reports.png

   - Reads from already-saved history from the daily scheduled check - it doesn't check the platform live
   - Includes an optional AI summary of the trend, when **Local AI** is configured under **Settings => Local AI Settings** (see :doc:`settings`)


~~~~~~~~~~~~~~~~~~
Graphical Reports
~~~~~~~~~~~~~~~~~~

Charts review count and/or rating over time for one link and date range, instead of showing them as a table.

1) Go to **Seo Tools => Review Manager => Graphical Reports**

2) Pick a **Link** and **Period**, then click **Show Records**
