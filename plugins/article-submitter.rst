.. title:: Article Submitter & Spinner Plugin for SEO Panel | Content Creation & Submission

.. meta::
   :description: Article Submitter & Spinner plugin for SEO Panel creates unique articles from keyword search results, spins content for variation, and submits to article directories and blogs automatically.
   :keywords: article submitter plugin, article spinner seo panel, content submission plugin, article directory submitter, seo panel article spinner


Article Submitter & Spinner
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. raw:: html

   <div style="background: linear-gradient(135deg, #134e4a 0%, #0f766e 50%, #0d9488 100%); border-radius: 10px; padding: 18px 24px; margin: 16px 0 28px 0; display: flex; align-items: center; justify-content: space-between; flex-wrap: wrap; gap: 14px; box-shadow: 0 4px 14px rgba(19,78,74,0.35);">
     <div style="display: flex; align-items: center; gap: 16px;">
       <div style="background: rgba(255,255,255,0.15); border-radius: 8px; width: 48px; height: 48px; display: flex; align-items: center; justify-content: center; flex-shrink: 0;">
         <i class="fa fa-pencil-square-o" style="color: #fff; font-size: 22px;"></i>
       </div>
       <div>
         <div style="display: flex; align-items: center; gap: 8px; margin-bottom: 4px;">
           <span style="color: #fff; font-size: 16px; font-weight: 700; line-height: 1;">Article Submitter &amp; Spinner Plugin</span>
           <span style="background: rgba(255,255,255,0.2); color: #fff; font-size: 11px; font-weight: 600; padding: 2px 8px; border-radius: 20px; line-height: 1.5;">v2.0.0</span>
         </div>
         <div style="color: rgba(255,255,255,0.82); font-size: 13px; line-height: 1.4;">Create &amp; spin articles from search results, then <strong style="color:#fff;">submit to directories &amp; blogs</strong> automatically.</div>
       </div>
     </div>
     <a href="https://www.seopanel.org/plugin/l/119/article-submitter-and-spinner/" target="_blank"
        style="display: inline-flex; align-items: center; gap: 8px; background: #fff; color: #134e4a; padding: 10px 22px; border-radius: 7px; font-weight: 700; font-size: 14px; text-decoration: none; box-shadow: 0 2px 8px rgba(0,0,0,0.18); white-space: nowrap; transition: opacity .2s;"
        onmouseover="this.style.opacity='.88'" onmouseout="this.style.opacity='1'">
       <i class="fa fa-download"></i> Download
     </a>
   </div>

Article Submitter & Spinner combines content creation and automated submission into one workflow. Search any keyword to pull snippets from search engine results, assemble them into an article draft, spin the content to create unique variations, and then submit the article to configured article directories and blogs — building backlinks at scale.

The plugin menu provides the following sections:

- **Project Manager** – Organise article creation by website
- **Article Manager** – Create and manage article drafts
- **Article Spinner** – Generate article content from keyword searches and spin for uniqueness
- **Article Submitter** – Submit saved articles to directories and blogs
- **Skipped Submissions** – View submissions that were skipped during the process
- **Submission Reports** – Track submission results per article
- **Article Directory Manager** – Manage the list of target directories (admin only)
- **Plugin Settings** – Configure user access (admin only)

~~~~~~~~~~~~~~~
Project Manager
~~~~~~~~~~~~~~~

Projects Manager organises articles by website. Filter by website to see the relevant projects.

**Creating a New Project**

1. Click **New Project**
2. Select the **Website**
3. Enter the **Project Name**
4. Click **Proceed** to save

**Project Actions**

- **Article Manager** – View articles within this project
- **Activate / Inactivate** – Toggle project status
- **Edit** – Rename the project
- **Delete** – Remove the project

~~~~~~~~~~~~~~~
Article Manager
~~~~~~~~~~~~~~~

Article Manager lists all article drafts created under each project. Each article shows its title, project, user and status.

**Creating a New Article**

Articles are typically created via the Article Spinner. You can also create one manually by clicking **New Article** and entering the title and content directly.

**Article Actions**

- **Edit** – Modify title and content
- **Submit** – Send this article to the Article Submitter
- **Delete** – Remove the article

~~~~~~~~~~~~~~~
Article Spinner
~~~~~~~~~~~~~~~

The Article Spinner is the content generation engine. It searches a keyword against a selected search engine, fetches result snippets, and assembles them into a draft article which you can edit and spin.

**To generate and spin an article:**

1. Enter a **Keyword** to search
2. Select the **Search Engine** to pull results from
3. Click **Search**
4. Review and edit the generated article draft in the text area
5. Click **Spin Article** to generate a unique variation using spin syntax (e.g. ``{word1|word2|word3}``)
6. Review the spun result
7. Click **Save Article** to save it to the Article Manager for submission

~~~~~~~~~~~~~~~~~
Article Submitter
~~~~~~~~~~~~~~~~~

The Article Submitter sends a saved article to the configured article directories and blogs.

**To submit an article:**

1. Select the **Article** from the dropdown
2. Click **Proceed**

The submission process runs automatically, opening each directory in sequence and submitting the article content. The results are recorded in Submission Reports.

~~~~~~~~~~~~~~~~~~~~
Skipped Submissions
~~~~~~~~~~~~~~~~~~~~

Skipped Submissions lists directories that were bypassed during a submission run — for example, those that were inactive or returned an error. Review this list to identify directories that need attention.

~~~~~~~~~~~~~~~~~~~~
Submission Reports
~~~~~~~~~~~~~~~~~~~~

Submission Reports shows the outcome of each article submission. Filter by project, article and submission status (Success / Failed / Skipped). Each entry shows the directory name, submission time and result.

~~~~~~~~~~~~~~~~~~~~~~~~~~
Article Directory Manager
~~~~~~~~~~~~~~~~~~~~~~~~~~

Article Directory Manager (admin only) lists all configured article directories and blogs available for submission. Each directory entry includes its URL, submission script type, status and other configuration details.

**Actions:**

- **Activate / Inactivate** – Include or exclude a directory from submission runs
- **Edit** – Modify the directory's submission settings
- **Delete** – Remove a directory

~~~~~~~~~~~~~~~
Plugin Settings
~~~~~~~~~~~~~~~

- **Allow user to access project manager** – When enabled, non-admin users can create projects, manage articles, use the spinner and submitter, and view reports
- **Allow user to access article directory manager** – When enabled, non-admin users can manage the article directory list
