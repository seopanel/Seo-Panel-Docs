.. title:: Blog Commenter Plugin for SEO Panel | Automated Blog Comment Submission

.. meta::
   :description: Blog Commenter plugin for SEO Panel automatically finds blogs by keyword and submits comments with backlinks — build traffic and links through automated blog outreach with 10 comment templates per project.
   :keywords: blog commenter plugin, seo panel blog commenter, automated blog commenting, blog comment backlinks, keyword blog search, seo panel comment submission


Blog Commenter
~~~~~~~~~~~~~~

.. raw:: html

   <div style="background: linear-gradient(135deg, #1e40af 0%, #2563eb 50%, #1d4ed8 100%); border-radius: 10px; padding: 18px 24px; margin: 16px 0 28px 0; display: flex; align-items: center; justify-content: space-between; flex-wrap: wrap; gap: 14px; box-shadow: 0 4px 14px rgba(30,64,175,0.35);">
     <div style="display: flex; align-items: center; gap: 16px;">
       <div style="background: rgba(255,255,255,0.15); border-radius: 8px; width: 48px; height: 48px; display: flex; align-items: center; justify-content: center; flex-shrink: 0;">
         <i class="fa fa-comments" style="color: #fff; font-size: 22px;"></i>
       </div>
       <div>
         <div style="display: flex; align-items: center; gap: 8px; margin-bottom: 4px;">
           <span style="color: #fff; font-size: 16px; font-weight: 700; line-height: 1;">Blog Commenter Plugin</span>
           <span style="background: rgba(255,255,255,0.2); color: #fff; font-size: 11px; font-weight: 600; padding: 2px 8px; border-radius: 20px; line-height: 1.5;">v2.4.0</span>
         </div>
         <div style="color: rgba(255,255,255,0.82); font-size: 13px; line-height: 1.4;">Auto-submit comments to <strong style="color:#fff;">blogs &amp; websites</strong> using keyword search &mdash; build links on autopilot.</div>
       </div>
     </div>
     <a href="https://www.seopanel.org/plugin/l/12/blog-commentor/" target="_blank"
        style="display: inline-flex; align-items: center; gap: 8px; background: #fff; color: #1e40af; padding: 10px 22px; border-radius: 7px; font-weight: 700; font-size: 14px; text-decoration: none; box-shadow: 0 2px 8px rgba(0,0,0,0.18); white-space: nowrap; transition: opacity .2s;"
        onmouseover="this.style.opacity='.88'" onmouseout="this.style.opacity='1'">
       <i class="fa fa-download"></i> Download
     </a>
   </div>

Blog Commenter automatically searches for blogs using a target keyword, collects blog URLs from search engine results, and submits comments with your backlink to those blogs. Each project stores up to 10 comment templates that are rotated during submission, and you can track which comments have been submitted and approved.

The plugin menu provides the following sections:

- **Projects Manager** – Create and manage blog commenting campaigns per website
- **View Reports** – Browse discovered blog links and submit or check comments
- **Import Project Links** – Manually add blog URLs to an existing project
- **Cron Command** – Set up automated comment submission (admin only)
- **Plugin Settings** – Configure user access and submission limits (admin only)

~~~~~~~~~~~~~~~~
Projects Manager
~~~~~~~~~~~~~~~~

Projects Manager lists all blog commenter campaigns. Each project shows its keyword, website, language, maximum links limit, crawled links count, and status.

Filter the list by **Website** to focus on a specific site.

**Creating a New Project**

1. Click **New Project**
2. Enter the project **Name**
3. Enter the **Keyword** — used to search for relevant blogs via the search engine (e.g. ``seo tips``, ``wordpress tutorials``)
4. Select the **Website** the backlinks will point to
5. Enter the **Link Title** — the anchor text used when your link is inserted into the comment. Multiple title variations can be separated by pipe ``|`` (e.g. ``SEO Panel|SEO Tool|Free SEO Software``)
6. Enter the **Comment Email** — the email address submitted with each comment
7. Select the **Language** for the blog search
8. Enter the **Maximum Blog Links** — how many blog URLs to discover and store (max set in Plugin Settings)
9. Enter up to **10 comment templates** (Comment 1 through Comment 10). Comment 1 is required; the rest are optional. The plugin rotates through these during submission for variety
10. Click **Proceed** to save

**Project Actions**

- **Run Project** – Start the keyword search to discover blog URLs
- **View Reports** – Open the report view for this project to submit and track comments
- **Import Links** – Manually add blog URLs to this project
- **Copy Project** – Duplicate this project (useful for creating variations)
- **Activate / Inactivate** – Toggle the project's status
- **Edit** – Modify project settings
- **Delete** – Remove the project

~~~~~~~~~~~
Run Project
~~~~~~~~~~~

Running a project starts the keyword crawl. SEO Panel searches the configured search engine using the project's keyword, collects matching blog URLs, and saves them into the project's link list.

The Run Project view shows a live summary:

- **Pages Found** – Total blog URLs discovered so far
- **Checked Links** – Links verified as accessible
- **Active Links** – Links confirmed as live
- **Inactive Links** – Links that returned an error

The crawl proceeds automatically, loading a batch of results, then waiting a delay before the next batch. Click the **Click Here to run project** link to restart or continue the crawl manually. Press **Escape** to stop.

Once the crawl completes, a success message confirms the number of links saved and directs you to View Reports to begin submitting comments.

~~~~~~~~~~~~
View Reports
~~~~~~~~~~~~

View Reports is where you submit comments and track their status. Filter the link list by:

- **Website** and **Project**
- **Status** – Active or Inactive links
- **Submitted** – Yes / No (whether a comment has been submitted)
- **Approved** – Yes / No (whether the submitted comment was approved by the blog)

Each link entry shows the blog title, description, URL, submission status, approval status, and active status.

**Link Actions**

- **Submit Comment** – Submit a comment to this blog (only available for links not yet submitted, if permission is granted)
- **Check Submission** – Re-check the approval status of a previously submitted comment
- **Check Status** – Verify the link is still live
- **Activate / Inactivate** – Include or exclude this link from submissions
- **Delete** – Remove the link from the project

~~~~~~~~~~~~~~~~~~~~
Import Project Links
~~~~~~~~~~~~~~~~~~~~

Import Project Links lets you manually add known blog URLs to an existing project — useful when you already have a list of target blogs.

1. Select the **Project**
2. Paste the blog URLs into the **URLs** field, separated by commas

   *Example:* ``https://www.example-blog.com/post-1, https://www.another-blog.com/article``

3. Click **Proceed**

The imported links are added to the project's link list and are immediately available in View Reports for comment submission.

~~~~~~~~~~~~
Cron Command
~~~~~~~~~~~~

The Cron Command section (admin only) provides the server command to automate blog link discovery and comment submission on a schedule. Access via **Admin Panel → Blog Commenter → Cron Command** for the pre-filled command for your installation.

~~~~~~~~~~~~~~~
Plugin Settings
~~~~~~~~~~~~~~~

- **Allow user to access project manager** – When enabled, non-admin users can create and manage projects, run projects, view reports and import links
- **Allow user to submit comment to blog** – When enabled, non-admin users can submit comments from the View Reports section
- **Allow user to submit comment to a blog more than one time** – When enabled, the same blog URL can receive multiple comment submissions from the same project
- **Maximum number of blog links per project** – The maximum number of blog URLs that can be collected per project (default: 100)
