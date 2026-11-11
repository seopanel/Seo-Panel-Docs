.. title:: Yandex Search Engine Package for SEO Panel | Russian Market Rank Tracking

.. meta::
   :description: Yandex Search Engine Package adds Yandex rank tracking to SEO Panel, enabling keyword position monitoring for Russia and Eastern Europe — imported as a simple SQL file.
   :keywords: yandex search engine seo panel, yandex rank tracker, russian keyword ranking, seo panel yandex, yandex position checker


Yandex Search Engine Package
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. raw:: html

   <div style="background: linear-gradient(135deg, #92400e 0%, #b45309 50%, #d97706 100%); border-radius: 10px; padding: 18px 24px; margin: 16px 0 28px 0; display: flex; align-items: center; justify-content: space-between; flex-wrap: wrap; gap: 14px; box-shadow: 0 4px 14px rgba(146,64,14,0.35);">
     <div style="display: flex; align-items: center; gap: 16px;">
       <div style="background: rgba(255,255,255,0.15); border-radius: 8px; width: 48px; height: 48px; display: flex; align-items: center; justify-content: center; flex-shrink: 0;">
         <i class="fa fa-search" style="color: #fff; font-size: 22px;"></i>
       </div>
       <div>
         <div style="display: flex; align-items: center; gap: 8px; margin-bottom: 4px;">
           <span style="color: #fff; font-size: 16px; font-weight: 700; line-height: 1;">Yandex Search Engine Package</span>
           <span style="background: rgba(255,255,255,0.2); color: #fff; font-size: 11px; font-weight: 600; padding: 2px 8px; border-radius: 20px; line-height: 1.5;">SQL Package</span>
         </div>
         <div style="color: rgba(255,255,255,0.82); font-size: 13px; line-height: 1.4;">Add <strong style="color:#fff;">Yandex (www.yandex.ru)</strong> to SEO Panel — track keyword rankings in Russia &amp; Eastern Europe.</div>
       </div>
     </div>
     <a href="https://www.seopanel.org/plugin/l/8/yandex-search-engine-package/" target="_blank"
        style="display: inline-flex; align-items: center; gap: 8px; background: #fff; color: #92400e; padding: 10px 22px; border-radius: 7px; font-weight: 700; font-size: 14px; text-decoration: none; box-shadow: 0 2px 8px rgba(0,0,0,0.18); white-space: nowrap; transition: opacity .2s;"
        onmouseover="this.style.opacity='.88'" onmouseout="this.style.opacity='1'">
       <i class="fa fa-download"></i> Download
     </a>
   </div>

The Yandex Search Engine Package is a downloadable SQL data file that adds **Yandex** (``www.yandex.ru``) to SEO Panel's search engine list. Once imported, you can track keyword rankings in Russia's dominant search engine — which holds approximately 60% of the Russian search market — using all of SEO Panel's rank tracking tools.

This package is ideal for businesses and agencies managing SEO for Russian-speaking markets and Eastern Europe / CIS countries.

~~~~~~~~~~~~~
What It Does
~~~~~~~~~~~~~

Imports a Yandex search engine entry into the ``searchengines`` table of your SEO Panel database. Once imported, ``yandex.ru`` appears in the **Search Engine Manager** and becomes selectable in:

- **Rank Checker**
- **Keyword Position Checker**
- **Search Engine Saturation Checker**
- **Bulk Keyword Rank Checker** (if installed)

~~~~~~~~~~~~~
How to Import
~~~~~~~~~~~~~

**Step 1 — Download the package**

Download the SQL file from the `Yandex Search Engine Package page <https://www.seopanel.org/plugin/l/8/yandex-search-engine-package/>`_ on seopanel.org.

**Step 2 — Import the SQL file**

*Using phpMyAdmin:*

1. Open phpMyAdmin and select your SEO Panel database
2. Click the **Import** tab
3. Choose the downloaded ``.sql`` file and click **Go**

*Using the MySQL command line:*

.. code-block:: bash

   mysql -u your_db_user -p your_db_name < yandex_search_engine.sql

**Step 3 — Verify**

Go to **Admin Panel → Search Engine Manager** — Yandex will appear in the list with Active status.

.. note::
   To manage the Yandex entry after import, use the **Search Engine Manager** to activate, inactivate or adjust the maximum results setting.
