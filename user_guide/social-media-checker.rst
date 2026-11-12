.. title:: SEO Panel Social Media Checker | Facebook, Twitter & More

.. meta::
   :description: Guide for seo panel Social Media Checker for facebook, twitter, youtube, instagram, pinterest with daily reports.


Social Media Checker
~~~~~~~~~~~~~~~~~~~~~

Tracks follower/like counts for your social media profiles over time - Facebook, Twitter, Instagram, LinkedIn, Pinterest, YouTube and Reddit - by scraping each platform's public profile page on a daily schedule. No API keys or connections needed.

~~~~~~~~~~~~~~~
Report Summary
~~~~~~~~~~~~~~~

The default Social Media Checker screen. For one chosen website, compares each registered link's followers/likes between two dates, with the change highlighted.

1) Go to **Seo Tools => Social Media Checker => Report Summary**

2) Pick a **Website** and **Period** (Day/Week/Month/Year, or your own two dates), then click **Search**

   .. image:: ../_static/sp_social_summary.png

   - Day/Week/Month/Year is anchored to the latest date that actually has scraped data, not today's date
   - Needs at least one link added under **Social Media Links** below, and a day or more of scraped history


~~~~~~~~~~~~~~~~~~~
Social Media Links
~~~~~~~~~~~~~~~~~~~

Lists the social media profile links you've registered per website. A link must be created here before Report Summary, Detailed Reports or Graphical Reports have anything to show for it.

1) Go to **Seo Tools => Social Media Checker => Social Media Links**

2) Click **New Social Media Link**, pick a **Website** and **Type** (platform), and enter the profile **Link**

   .. image:: ../_static/sp_social_links.png

   - **Link** - The full profile URL, *Eg:* ``https://twitter.com/seopanel``. LinkedIn needs a numeric company ID instead of a URL
   - Activate, deactivate or delete a link from this same list
   - Link counts are capped by your account's plan


~~~~~~~~~~~~~~
Quick Checker
~~~~~~~~~~~~~~

Unlike every other tool here, this is an instant, unsaved preview - not part of the scheduled daily scrape.

1) Go to **Seo Tools => Social Media Checker => Quick Checker**

2) Pick a **Type** (platform), paste a profile **Link**, then click **Proceed**

   .. image:: ../_static/sp_social_quick_checker.png

   - Scrapes that public page right now for its current like/follower count - nothing is saved
   - Relies on reading the platform's public page HTML, not an official API, so results can break if a platform changes its page layout


~~~~~~~~~~~~~~~~
Detailed Reports
~~~~~~~~~~~~~~~~

For one chosen link, a day-by-day history table of followers/likes over a date range, with each day's change from the previous one highlighted.

1) Go to **Seo Tools => Social Media Checker => Detailed Reports**

2) Pick a **Link** and **Period**, then click **Show Records**

   .. image:: ../_static/sp_social_detailed_reports.png

   - Reads from already-saved history from the daily scheduled scrape - it doesn't check the platform live
   - Includes an optional AI summary of the trend, when **Local AI** is configured under **Settings => Local AI Settings** (see :doc:`settings`)


~~~~~~~~~~~~~~~~~~
Graphical Reports
~~~~~~~~~~~~~~~~~~

Charts followers and/or likes over time for one link and date range, instead of showing them as a table.

1) Go to **Seo Tools => Social Media Checker => Graphical Reports**

2) Pick a **Link** and **Period**, then click **Show Records**
