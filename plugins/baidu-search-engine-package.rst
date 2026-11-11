.. title:: Baidu Search Engine Package for SEO Panel | Chinese Market Rank Tracking

.. meta::
   :description: Baidu Search Engine Package adds Baidu rank tracking to SEO Panel, enabling keyword position monitoring for China — the world's largest search market — imported as a simple SQL file.
   :keywords: baidu search engine seo panel, baidu rank tracker, chinese keyword ranking, seo panel baidu, china search engine position checker


Baidu Search Engine Package
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. raw:: html

   <div style="background: linear-gradient(135deg, #1e40af 0%, #2563eb 50%, #3b82f6 100%); border-radius: 10px; padding: 18px 24px; margin: 16px 0 28px 0; display: flex; align-items: center; justify-content: space-between; flex-wrap: wrap; gap: 14px; box-shadow: 0 4px 14px rgba(30,64,175,0.35);">
     <div style="display: flex; align-items: center; gap: 16px;">
       <div style="background: rgba(255,255,255,0.15); border-radius: 8px; width: 48px; height: 48px; display: flex; align-items: center; justify-content: center; flex-shrink: 0;">
         <i class="fa fa-search" style="color: #fff; font-size: 22px;"></i>
       </div>
       <div>
         <div style="display: flex; align-items: center; gap: 8px; margin-bottom: 4px;">
           <span style="color: #fff; font-size: 16px; font-weight: 700; line-height: 1;">Baidu Search Engine Package</span>
           <span style="background: rgba(255,255,255,0.2); color: #fff; font-size: 11px; font-weight: 600; padding: 2px 8px; border-radius: 20px; line-height: 1.5;">SQL Package</span>
         </div>
         <div style="color: rgba(255,255,255,0.82); font-size: 13px; line-height: 1.4;">Add <strong style="color:#fff;">Baidu (www.baidu.com)</strong> to SEO Panel — track keyword rankings in China's dominant search engine.</div>
       </div>
     </div>
     <a href="https://www.seopanel.org/plugin/l/7/baidu-search-engine-package/" target="_blank"
        style="display: inline-flex; align-items: center; gap: 8px; background: #fff; color: #1e40af; padding: 10px 22px; border-radius: 7px; font-weight: 700; font-size: 14px; text-decoration: none; box-shadow: 0 2px 8px rgba(0,0,0,0.18); white-space: nowrap; transition: opacity .2s;"
        onmouseover="this.style.opacity='.88'" onmouseout="this.style.opacity='1'">
       <i class="fa fa-download"></i> Download
     </a>
   </div>

The Baidu Search Engine Package is a downloadable SQL data file that adds **Baidu** (``www.baidu.com``) to SEO Panel's search engine list. Once imported, you can track keyword rankings in China's dominant search engine — which holds approximately 70% of the Chinese search market — using all of SEO Panel's rank tracking tools.

This package is essential for businesses targeting Chinese audiences or managing SEO campaigns in the Chinese-speaking market.

~~~~~~~~~~~~~
What It Does
~~~~~~~~~~~~~

Imports a Baidu search engine entry into the ``searchengines`` table of your SEO Panel database. Once imported, ``baidu.com`` appears in the **Search Engine Manager** and becomes selectable in:

- **Rank Checker**
- **Keyword Position Checker**
- **Search Engine Saturation Checker**
- **Bulk Keyword Rank Checker** (if installed)

~~~~~~~~~~~~~
How to Import
~~~~~~~~~~~~~

**Step 1 — Download the package**

Download the SQL file from the `Baidu Search Engine Package page <https://www.seopanel.org/plugin/l/7/baidu-search-engine-package/>`_ on seopanel.org.

**Step 2 — Import the SQL file**

*Using phpMyAdmin:*

1. Open phpMyAdmin and select your SEO Panel database
2. Click the **Import** tab
3. Choose the downloaded ``.sql`` file and click **Go**

*Using the MySQL command line:*

.. code-block:: bash

   mysql -u your_db_user -p your_db_name < baidu_search_engine.sql

**Step 3 — Verify**

Go to **Admin Panel → Search Engine Manager** — Baidu will appear in the list with Active status.

.. note::
   To manage the Baidu entry after import, use the **Search Engine Manager** to activate, inactivate or adjust the maximum results setting.
