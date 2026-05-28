.. title:: Bulk Keyword Rank Checker Plugin for SEO Panel | Multi-URL Position Tracker

.. meta::
   :description: Bulk Keyword Rank Checker plugin for SEO Panel tracks keyword rankings for multiple URLs and search engines simultaneously, with PDF/CSV/HTML reports, SERP viewer, graphical charts and email delivery.
   :keywords: bulk keyword rank checker, seo panel bulk rank checker, keyword position tracker, multi url rank checker, serp results viewer, seo panel rank reports


Bulk Keyword Rank Checker
~~~~~~~~~~~~~~~~~~~~~~~~~~

.. raw:: html

   <div style="background: linear-gradient(135deg, #1e3a5f 0%, #1a5276 50%, #1976d2 100%); border-radius: 10px; padding: 18px 24px; margin: 16px 0 28px 0; display: flex; align-items: center; justify-content: space-between; flex-wrap: wrap; gap: 14px; box-shadow: 0 4px 14px rgba(30,58,95,0.35);">
     <div style="display: flex; align-items: center; gap: 16px;">
       <div style="background: rgba(255,255,255,0.15); border-radius: 8px; width: 48px; height: 48px; display: flex; align-items: center; justify-content: center; flex-shrink: 0;">
         <i class="fa fa-bar-chart" style="color: #fff; font-size: 22px;"></i>
       </div>
       <div>
         <div style="display: flex; align-items: center; gap: 8px; margin-bottom: 4px;">
           <span style="color: #fff; font-size: 16px; font-weight: 700; line-height: 1;">Bulk Keyword Rank Checker Plugin</span>
           <span style="background: rgba(255,255,255,0.2); color: #fff; font-size: 11px; font-weight: 600; padding: 2px 8px; border-radius: 20px; line-height: 1.5;">v3.0.0</span>
         </div>
         <div style="color: rgba(255,255,255,0.82); font-size: 13px; line-height: 1.4;">Track rankings for <strong style="color:#fff;">multiple keywords &amp; URLs</strong> simultaneously — PDF, CSV &amp; HTML reports with SERP viewer.</div>
       </div>
     </div>
     <a href="https://www.seopanel.org/plugin/l/49/bulk-keyword-rank-checker/" target="_blank"
        style="display: inline-flex; align-items: center; gap: 8px; background: #fff; color: #1e3a5f; padding: 10px 22px; border-radius: 7px; font-weight: 700; font-size: 14px; text-decoration: none; box-shadow: 0 2px 8px rgba(0,0,0,0.18); white-space: nowrap; transition: opacity .2s;"
        onmouseover="this.style.opacity='.88'" onmouseout="this.style.opacity='1'">
       <i class="fa fa-download"></i> Download
     </a>
   </div>

Bulk Keyword Rank Checker tracks the search engine position of multiple keywords across multiple URLs and search engines simultaneously — within a single campaign. It generates detailed HTML, PDF and CSV reports, provides a SERP results popup viewer, supports graphical trend charts, and delivers reports via email on a schedule.

.. image:: ../_static/sp_brc_report_summary.png
   :alt: Bulk Keyword Rank Checker report summary showing keyword positions across multiple URLs

The plugin menu provides the following sections:

- **Report Summary** – Dashboard overview of all campaign ranking results
- **Campaign Manager** – Create and manage bulk rank checking campaigns
- **Detailed Position Reports** – Per-keyword, per-URL position data with filtering
- **Graphical Position Reports** – Visual ranking trend charts
- **Generate Reports** – Manually trigger report generation (admin, if enabled)
- **Cron Command** – Set up automated report generation (admin only)
- **Plugin Settings** – Configure access and cron behaviour (admin only)
- **User Type Settings** – Per-user-type keyword and link limits (admin only)

~~~~~~~~~~~~~~
Report Summary
~~~~~~~~~~~~~~

The Report Summary dashboard gives an at-a-glance view of all campaign performance. It shows ranking trends, keyword movement (up/down), top-ranked keywords and position distribution across all active campaigns.

.. image:: ../_static/sp_brc_report_generation.png
   :alt: Bulk Keyword Rank Checker report generation progress showing crawled keywords and campaign status

~~~~~~~~~~~~~~~~
Campaign Manager
~~~~~~~~~~~~~~~~

Campaign Manager is where bulk rank checking campaigns are created. Each campaign defines the target website, language, country, search engines, keywords and URLs to track.

**Creating a New Campaign**

1. Click **New Campaign**
2. Select the **Website**
3. Enter the campaign **Name**
4. Select the **Language**
5. Select the **Country**
6. Select one or more **Search Engines** (use Select All to check all active engines)
7. Paste the **Keywords** to track (one per line)
8. Paste the **Links** (URLs) to check rankings for (one per line)
9. Set **Execute with cron** to Yes to include this campaign in automated runs
10. Set the **Reports generation interval** (Daily, Weekly, etc.)
11. Click **Proceed** to save

**Campaign Actions**

- **Run** – Start crawling ranks immediately for this campaign
- **Reports** – View detailed position results for this campaign
- **Activate / Inactivate** – Toggle campaign status
- **Edit** – Modify campaign settings
- **Delete** – Remove the campaign

~~~~~~~~~~~~
Run Campaign
~~~~~~~~~~~~

The Run Campaign view shows a progress bar as keywords are being crawled, displaying the number of crawled keywords vs. total and the percentage complete. Once finished, results are available in the report views.

~~~~~~~~~~~~~~~~~~~~~~~~~
Detailed Position Reports
~~~~~~~~~~~~~~~~~~~~~~~~~

Detailed Position Reports shows the exact rank position for each keyword–URL–search engine combination. Use the filters to drill down by campaign, keyword, link and date range.

.. image:: ../_static/sp_brc_serp_results.png
   :alt: Bulk Keyword Rank Checker SERP results popup showing top search results for a keyword

Click any result row to open the **SERP Results** popup, which displays the actual top search results returned for that keyword on that search engine — useful for competitive analysis.

Export options include HTML, PDF and CSV formats.

~~~~~~~~~~~~~~~~~~~~~~~~~~
Graphical Position Reports
~~~~~~~~~~~~~~~~~~~~~~~~~~

Graphical Position Reports renders ranking trend charts over time for each keyword and URL combination. Visualise position movement, identify trends, and spot drops or improvements at a glance.

~~~~~~~~~~~~~~~~
Generate Reports
~~~~~~~~~~~~~~~~

The Generate Reports section (admin only, if enabled via settings) lets you manually trigger report generation for one or all campaigns directly from the user interface, without requiring cron access.

~~~~~~~~~~~~
Cron Command
~~~~~~~~~~~~

The Cron Command section provides the server crontab command to automate report generation on a schedule. Access it via **Admin Panel → Bulk Keyword Rank Checker → Cron Command** for the pre-filled command with your installation path.

~~~~~~~~~~~~~~~
Plugin Settings
~~~~~~~~~~~~~~~

- **Allow user to access the campaign manager** – When enabled, non-admin users can create and manage campaigns and view reports
- **Number of keywords in cron job** – How many keywords are processed per cron execution (default: 1)
- **Enable reports generation from user interface** – When enabled, the Generate Reports menu item is shown to admins

~~~~~~~~~~~~~~~~~~
User Type Settings
~~~~~~~~~~~~~~~~~~

User Type Settings (admin only) defines per-user-type limits on the number of keywords and links allowed per campaign, enabling tiered access for different subscription levels.
