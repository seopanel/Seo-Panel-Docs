.. title:: SEO Panel PageSpeed Insights | Desktop & Mobile Performance

.. meta::
   :description: Guide for seo panel PageSpeed Insights checker for a website with desktop and mobile filter.


PageSpeed Insights
~~~~~~~~~~~~~~~~~~~

Tracks a website's Google PageSpeed score for both desktop and mobile over time. Generating or scheduling a check needs a **Google API Key** configured under **Admin Panel => System Settings => Google Settings** (see :doc:`settings`).

~~~~~~~~~~~~~~~~~~
PageSpeed Reports
~~~~~~~~~~~~~~~~~~

The default PageSpeed Insights screen. Shows a date-range history of a website's previously saved desktop and mobile scores, with trend-change indicators and a details panel.

1) Go to **Seo Tools => PageSpeed Insights => PageSpeed Reports**

2) Pick a **Website** and **Period**, then click **Show Records**

   .. image:: ../_static/sp_pagespeed_reports.png

   - Reads only already-saved scores - no new API call happens here
   - Needs data saved by **Generate Reports** below, or the scheduled cron, before this shows anything


~~~~~~~~~~~~~~~~~~~~~~~~
Quick PageSpeed Checker
~~~~~~~~~~~~~~~~~~~~~~~~

1) Go to **Seo Tools => PageSpeed Insights => Quick PageSpeed Checker** (only shown for admins, or when enabled for your account)

2) Paste up to 5 URLs, one per line, then click **Proceed**

   .. image:: ../_static/sp_pagespeed_quick_checker.png

   - Gets an immediate desktop and mobile score for each URL by calling Google's PageSpeed Insights API live - nothing is saved
   - Requires a Google API key configured on this server


~~~~~~~~~~~~~~~~~~
Graphical Reports
~~~~~~~~~~~~~~~~~~

Charts desktop and mobile PageSpeed scores over time for a single website, instead of showing them as a table.

1) Go to **Seo Tools => PageSpeed Insights => Graphical Reports**

2) Pick a **Website** and **Period**, then click **Show Records**

   - Reads from already-saved scores only - no new API call happens here


~~~~~~~~~~~~~~~~
Generate Reports
~~~~~~~~~~~~~~~~

Triggers an on-demand PageSpeed check-and-save (desktop + mobile) for one or all of your active websites right now, instead of waiting for the scheduled cron.

1) Go to **Seo Tools => PageSpeed Insights => Generate Reports**

2) Pick a **Website** (or all websites), then click **Proceed**

   .. image:: ../_static/sp_pagespeed_generate.png

   - Requires a Google API key configured on this server
   - If both the desktop and mobile checks fail, nothing is saved rather than storing a misleading zero score
