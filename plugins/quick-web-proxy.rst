.. title:: Quick Web Proxy Plugin for SEO Panel | Anonymous Web Proxy Server

.. meta::
   :description: Quick Web Proxy plugin for SEO Panel lets you browse websites anonymously through your hosting server or external proxies — bypass restrictions and test accessibility from different locations.
   :keywords: quick web proxy plugin, seo panel proxy, anonymous browsing seo panel, web proxy server, bypass restrictions seo panel


Quick Web Proxy
~~~~~~~~~~~~~~~

.. raw:: html

   <div style="background: linear-gradient(135deg, #374151 0%, #4b5563 50%, #6b7280 100%); border-radius: 10px; padding: 18px 24px; margin: 16px 0 28px 0; display: flex; align-items: center; justify-content: space-between; flex-wrap: wrap; gap: 14px; box-shadow: 0 4px 14px rgba(55,65,81,0.35);">
     <div style="display: flex; align-items: center; gap: 16px;">
       <div style="background: rgba(255,255,255,0.15); border-radius: 8px; width: 48px; height: 48px; display: flex; align-items: center; justify-content: center; flex-shrink: 0;">
         <i class="fa fa-shield" style="color: #fff; font-size: 22px;"></i>
       </div>
       <div>
         <div style="display: flex; align-items: center; gap: 8px; margin-bottom: 4px;">
           <span style="color: #fff; font-size: 16px; font-weight: 700; line-height: 1;">Quick Web Proxy Plugin</span>
           <span style="background: rgba(255,255,255,0.2); color: #fff; font-size: 11px; font-weight: 600; padding: 2px 8px; border-radius: 20px; line-height: 1.5;">v2.2.0</span>
         </div>
         <div style="color: rgba(255,255,255,0.82); font-size: 13px; line-height: 1.4;">Browse anonymously &amp; bypass restrictions using your <strong style="color:#fff;">hosting server or external proxies</strong> — directly from SEO Panel.</div>
       </div>
     </div>
     <a href="https://www.seopanel.org/plugin/l/94/quick-web-proxy/" target="_blank"
        style="display: inline-flex; align-items: center; gap: 8px; background: #fff; color: #374151; padding: 10px 22px; border-radius: 7px; font-weight: 700; font-size: 14px; text-decoration: none; box-shadow: 0 2px 8px rgba(0,0,0,0.18); white-space: nowrap; transition: opacity .2s;"
        onmouseover="this.style.opacity='.88'" onmouseout="this.style.opacity='1'">
       <i class="fa fa-download"></i> Download
     </a>
   </div>

Quick Web Proxy enables anonymous and secure website browsing directly from within SEO Panel. It uses your own hosting server or configured external proxy servers as intermediaries, allowing you to access restricted content, test website accessibility from different locations, and maintain privacy while browsing.

The plugin menu provides the following sections:

- **Web Proxy** – Browse any URL anonymously through a selected proxy server
- **Reports** – View proxy usage logs (admin only)
- **Settings** – Configure proxy behaviour and user access (admin only)

~~~~~~~~~
Web Proxy
~~~~~~~~~

The Web Proxy section is the main browsing interface. Select a proxy server, enter a URL and click **Proceed** to load the page through the chosen proxy.

**To browse via proxy:**

1. Select the **Server** from the dropdown — this lists all configured proxy servers plus the option to use your web hosting server directly
2. Enter the target **URL** to load
3. Click **Proceed**

The page loads inside the content area, routed through the selected proxy. This is useful for:

- Checking how a site appears from a different geographic location
- Bypassing IP blocks or geo-restrictions when crawling
- Testing website accessibility without exposing your real IP

~~~~~~~
Reports
~~~~~~~

The Reports section (admin only) shows a log of all web proxy requests made through the plugin, linking to the standard SEO Panel crawl log filtered by proxy activity.

~~~~~~~~
Settings
~~~~~~~~

Plugin Settings (admin only) controls access and server behaviour.

Available settings:

- **Allow user to access the web proxy** – When enabled, non-admin users can use the Web Proxy section
- **Allow web server to act as a proxy** – When enabled, your own hosting server is available as a proxy option in addition to any external proxies configured in SEO Panel's Proxy Manager

To update settings, change the values and click **Proceed**.

.. note::
   External proxy servers are managed in **Admin Panel → Proxy Manager**. Add your proxy servers there first, then they will appear in the Quick Web Proxy server dropdown.
