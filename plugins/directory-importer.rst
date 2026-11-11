.. title:: Directory Importer Plugin for SEO Panel | Import Directories for Link Building

.. meta::
   :description: Directory Importer plugin for SEO Panel lets you import new web directories into SEO Panel's Directory Submission tool — with 100+ pre-loaded directories, multi-language support, status checking and cron automation.
   :keywords: directory importer plugin, seo panel directory importer, import directories seo panel, web directory submission, directory link building, seo panel directory manager


Directory Importer
~~~~~~~~~~~~~~~~~~

.. raw:: html

   <div style="background: linear-gradient(135deg, #c2410c 0%, #ea580c 50%, #9a3412 100%); border-radius: 10px; padding: 18px 24px; margin: 16px 0 28px 0; display: flex; align-items: center; justify-content: space-between; flex-wrap: wrap; gap: 14px; box-shadow: 0 4px 14px rgba(194,65,12,0.35);">
     <div style="display: flex; align-items: center; gap: 16px;">
       <div style="background: rgba(255,255,255,0.15); border-radius: 8px; width: 48px; height: 48px; display: flex; align-items: center; justify-content: center; flex-shrink: 0;">
         <i class="fa fa-upload" style="color: #fff; font-size: 22px;"></i>
       </div>
       <div>
         <div style="display: flex; align-items: center; gap: 8px; margin-bottom: 4px;">
           <span style="color: #fff; font-size: 16px; font-weight: 700; line-height: 1;">Directory Importer Plugin</span>
           <span style="background: rgba(255,255,255,0.2); color: #fff; font-size: 11px; font-weight: 600; padding: 2px 8px; border-radius: 20px; line-height: 1.5;">v1.3.2</span>
         </div>
         <div style="color: rgba(255,255,255,0.82); font-size: 13px; line-height: 1.4;">Import new directories into SEO Panel's submission tool &mdash; expand your <strong style="color:#fff;">link building database</strong> instantly.</div>
       </div>
     </div>
     <a href="https://www.seopanel.org/plugin/l/10/directory-importer/" target="_blank"
        style="display: inline-flex; align-items: center; gap: 8px; background: #fff; color: #c2410c; padding: 10px 22px; border-radius: 7px; font-weight: 700; font-size: 14px; text-decoration: none; box-shadow: 0 2px 8px rgba(0,0,0,0.18); white-space: nowrap; transition: opacity .2s;"
        onmouseover="this.style.opacity='.88'" onmouseout="this.style.opacity='1'">
       <i class="fa fa-download"></i> Download
     </a>
   </div>

Directory Importer extends SEO Panel's built-in Directory Submission tool by letting you add new web directories to the database. It comes pre-loaded with over 100 active directories across multiple languages, and allows you to import additional directories in bulk by pasting their URLs. Directories can be status-checked manually or automatically via cron to ensure they remain live.

The plugin menu provides the following sections:

- **Directory Manager** – Browse, filter and manage all imported directories
- **Import Directories** – Bulk-import new directories by URL
- **Check Status** – Verify the live status of directories in bulk
- **Cron Command** – Automate status checking (admin only)
- **Plugin Settings** – Configure user access and cron behaviour (admin only)

~~~~~~~~~~~~~~~~~~
Directory Manager
~~~~~~~~~~~~~~~~~~

Directory Manager lists all directories available in SEO Panel for submission. Filter the list by:

- **Directory** – Name/URL keyword search
- **Status** – Working, Not Working, Not Checked, etc.
- **Captcha** – Yes / No (whether the directory uses a captcha)
- **Google PageRank** – Filter by PR level (0–10)
- **Language** – Filter by directory language

Each directory entry shows:

- **ID** – Internal identifier
- **Website** – The directory's submit URL (clickable, opens in a new tab)
- **PR** – Google PageRank
- **Captcha** – Whether the directory uses captcha
- **Language** – Directory language
- **Type** – Link type (Free, Paid, Reciprocal, Featured) — changeable via the inline dropdown
- **Script** – The submission script type used
- **Status** – Current live status (Working / Not Working / Not Checked)

**Directory Actions**

- **Check Status** – Individually verify this directory is still live and update its status
- **Edit** – Modify the directory's script type, language, link type, submit URL and advanced fields
- **Delete** – Remove the directory from the list

**Editing a Directory**

Click any directory name or select **Edit** from the action dropdown to open the edit form:

- **Directory Script Type** – The submission script template (e.g. PHPLink, Skalinks, Aardvark, etc.)
- **Language** – The directory's language
- **Link Type** – Free / Reciprocal / Featured / Paid
- **Directory Submit URL** – The full URL of the directory's submission page
- **Advanced Fields** – Script-specific fields (shown via **Show Advanced Fields**) such as column mappings, extra values and captcha configuration

~~~~~~~~~~~~~~~~~~~~
Import Directories
~~~~~~~~~~~~~~~~~~~~

Import Directories lets you add new web directories to SEO Panel in bulk by pasting their submission URLs.

**To import directories:**

1. Select the **Directory Script Type** — the submission script the directories use (e.g. PHPLink, Skalinks)
2. Select the **Language** of the directories
3. Select the **Link Type** — Free, Reciprocal, Featured or Paid
4. Check **Check Google PageRank** to fetch the PR of each directory during import (optional)
5. Check **Check Directory Status** to immediately verify each directory is live after import (optional)
6. Paste the directory **URLs** into the text area, separated by commas

   *Example:* ``http://directory.seofreetools.net/submit.php, http://www.fat64.net/submit.php``

7. Optionally click **Show Advanced Fields** to override specific script columns (for expert use)
8. Click **Proceed** to import

After import, a results summary is shown with counts of **Valid**, **Existing** (already in the database) and **Invalid** entries. If **Check Directory Status** was selected, the status check runs immediately after import.

~~~~~~~~~~~~~
Check Status
~~~~~~~~~~~~~

The Check Status section lets you run a bulk status verification across your existing directories. This confirms which directories are still live and updates their status in the Directory Manager.

**Filters before running:**

- **Status** – Limit the check to directories with a particular current status
- **Captcha** – Include or exclude captcha directories
- **Check Status** – Target only **Not Checked** or **Already Checked** directories
- **Language** – Limit to a specific language
- **Check Google PageRank** – Also refresh PageRank during the status check (checked by default)

Click **Proceed** to start. The check runs progressively in the background — the status of each directory is updated in real time. Press **Escape** to stop.

~~~~~~~~~~~~
Cron Command
~~~~~~~~~~~~

The Cron Command section (admin only) provides the server command to automate directory status checking on a schedule. Access via **Admin Panel → Directory Importer → Cron Command** for the pre-filled command for your installation.

~~~~~~~~~~~~~~~
Plugin Settings
~~~~~~~~~~~~~~~

- **Allow user to access directory manager** – When enabled, non-admin users can access the Directory Manager, Import Directories and Check Status sections
- **Check Google PageRank** *(Cron setting)* – Whether to check PageRank during automated cron status runs
- **Check status of directories** *(Cron setting)* – Which directories the cron job targets: **Not Checked** (only un-checked directories) or **All** (every directory, re-checking previously verified ones)
