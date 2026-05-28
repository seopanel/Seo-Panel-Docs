.. title:: Social Media Manager Plugin for SEO Panel | Auto Post to Facebook, LinkedIn & Twitter

.. meta::
   :description: Social Media Manager plugin for SEO Panel lets you schedule and auto-post status updates to Facebook, LinkedIn and Twitter from a single dashboard with cron automation and submission reports.
   :keywords: social media manager plugin, seo panel social media, auto post facebook linkedin twitter, social media scheduler seo panel, social media automation


Social Media Manager
~~~~~~~~~~~~~~~~~~~~

.. raw:: html

   <div style="background: linear-gradient(135deg, #1d4ed8 0%, #2563eb 50%, #3b82f6 100%); border-radius: 10px; padding: 18px 24px; margin: 16px 0 28px 0; display: flex; align-items: center; justify-content: space-between; flex-wrap: wrap; gap: 14px; box-shadow: 0 4px 14px rgba(29,78,216,0.35);">
     <div style="display: flex; align-items: center; gap: 16px;">
       <div style="background: rgba(255,255,255,0.15); border-radius: 8px; width: 48px; height: 48px; display: flex; align-items: center; justify-content: center; flex-shrink: 0;">
         <i class="fa fa-share-alt" style="color: #fff; font-size: 22px;"></i>
       </div>
       <div>
         <div style="display: flex; align-items: center; gap: 8px; margin-bottom: 4px;">
           <span style="color: #fff; font-size: 16px; font-weight: 700; line-height: 1;">Social Media Manager Plugin</span>
           <span style="background: rgba(255,255,255,0.2); color: #fff; font-size: 11px; font-weight: 600; padding: 2px 8px; border-radius: 20px; line-height: 1.5;">v4.0.0</span>
         </div>
         <div style="color: rgba(255,255,255,0.82); font-size: 13px; line-height: 1.4;">Schedule &amp; auto-post to <strong style="color:#fff;">Facebook, LinkedIn &amp; Twitter</strong> — manage all social updates from SEO Panel.</div>
       </div>
     </div>
     <a href="https://www.seopanel.org/plugin/l/23/social-media-manager/" target="_blank"
        style="display: inline-flex; align-items: center; gap: 8px; background: #fff; color: #1d4ed8; padding: 10px 22px; border-radius: 7px; font-weight: 700; font-size: 14px; text-decoration: none; box-shadow: 0 2px 8px rgba(0,0,0,0.18); white-space: nowrap; transition: opacity .2s;"
        onmouseover="this.style.opacity='.88'" onmouseout="this.style.opacity='1'">
       <i class="fa fa-download"></i> Download
     </a>
   </div>

Social Media Manager automates the scheduling and posting of status updates to major social networks — Facebook, LinkedIn and Twitter — directly from SEO Panel. Organise posts into projects, schedule them with a date and time, run them via cron, and track submission results.

The plugin menu provides the following sections:

- **Projects Manager** – Organise social media campaigns by website
- **Post Manager** – Create and manage scheduled social media posts
- **Connection Manager** – Connect social media accounts (Facebook, LinkedIn, Twitter)
- **Submission Reports** – View posting results and delivery status
- **Social Media Manager** – Manage available social platforms (admin only)
- **Cron Command** – Set up automated posting (admin only)
- **Plugin Settings** – Configure user access (admin only)

~~~~~~~~~~~~~~~~
Projects Manager
~~~~~~~~~~~~~~~~

Projects Manager organises your social media campaigns. Each project is linked to a website and contains a collection of posts. Filter by website and status.

**Creating a New Project**

1. Click **New Project**
2. Select the **Website**
3. Enter the project **Name**
4. Enter a **Description**
5. Click **Proceed** to save

**Project Actions**

- **Post Manager** – View and manage posts within this project
- **Activate / Inactivate** – Toggle project status
- **Edit** – Modify project details
- **Delete** – Remove the project

~~~~~~~~~~~~
Post Manager
~~~~~~~~~~~~

Post Manager is where individual social media posts are created and scheduled. Filter posts by website, project, status, keywords and date range.

**Creating a New Post**

1. Click **New Post**
2. Select the **Project**
3. Enter the target **URL** to share
4. Enter the post **Title** (max ~200 chars, with character counter)
5. Enter the **Description** (with character counter)
6. Enter **Tags** (optional, with character counter)
7. Enter an **Image URL** or upload an image for the post
8. Set the **Schedule Time** — date and hour/minute for when the post should be published
9. Click **Proceed** to save

**Post Actions**

- **Post Now** – Immediately submit the post to connected social accounts
- **Activate / Inactivate** – Include or exclude from cron scheduling
- **Edit** – Modify the post
- **Delete** – Remove the post

~~~~~~~~~~~~~~~~~~
Connection Manager
~~~~~~~~~~~~~~~~~~

Connection Manager handles the OAuth connections between SEO Panel and your social media accounts. Each user can connect their own accounts.

**Supported Platforms**

- **LinkedIn** — requires Client ID and Client Secret from a LinkedIn Developer App
- **Twitter / X** — requires Consumer Key and Consumer Secret from a Twitter Developer App
- **Facebook** — requires App ID and App Secret from a Facebook Developer App

**Connecting an Account**

1. Select the **Social Platform** from the filter
2. Click the connect button for the desired platform
3. You will be redirected to the platform's OAuth authorisation page
4. Approve the connection and you will be redirected back to SEO Panel

Once connected, the account appears in the Connection Manager with status **Active** and can be used for post submission.

**Connection Actions**

- **Activate / Inactivate** – Enable or disable the connection
- **Delete** – Remove the connection

~~~~~~~~~~~~~~~~~~~~
Submission Reports
~~~~~~~~~~~~~~~~~~~~

Submission Reports shows the result of each post submission attempt. Filter by project, post and status. Each report entry shows the social platform, post title, submission status (Success / Failed) and timestamp.

~~~~~~~~~~~~~~~~~~~~~
Social Media Manager
~~~~~~~~~~~~~~~~~~~~~

Social Media Manager (admin only) lists the social platforms registered in the plugin (LinkedIn, Twitter, Facebook) and allows admins to activate or inactivate platforms globally.

~~~~~~~~~~~~
Cron Command
~~~~~~~~~~~~

The Cron Command section (admin only) provides the command to automate post scheduling. Add it to your server crontab to publish scheduled posts without manual triggering.

Access via **Admin Panel → Social Media Manager → Cron Command** to get the exact pre-filled command for your installation.

~~~~~~~~~~~~~~~
Plugin Settings
~~~~~~~~~~~~~~~

- **Allow user to access project manager** – When enabled, non-admin users can access Projects Manager, Post Manager, Connection Manager and Submission Reports
