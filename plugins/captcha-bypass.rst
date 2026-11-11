.. title:: Captcha Bypass Plugin for SEO Panel | Automated Captcha Recognition

.. meta::
   :description: Captcha Bypass plugin for SEO Panel integrates with leading captcha solving services to automatically bypass captchas during directory submissions, enabling fully automated link building.
   :keywords: captcha bypass plugin, seo panel captcha, automated captcha solving, directory submission captcha, anti-captcha seo panel, 2captcha seo panel


Captcha Bypass
~~~~~~~~~~~~~~

.. raw:: html

   <div style="background: linear-gradient(135deg, #7c2d12 0%, #9a3412 50%, #c2410c 100%); border-radius: 10px; padding: 18px 24px; margin: 16px 0 28px 0; display: flex; align-items: center; justify-content: space-between; flex-wrap: wrap; gap: 14px; box-shadow: 0 4px 14px rgba(124,45,18,0.35);">
     <div style="display: flex; align-items: center; gap: 16px;">
       <div style="background: rgba(255,255,255,0.15); border-radius: 8px; width: 48px; height: 48px; display: flex; align-items: center; justify-content: center; flex-shrink: 0;">
         <i class="fa fa-unlock-alt" style="color: #fff; font-size: 22px;"></i>
       </div>
       <div>
         <div style="display: flex; align-items: center; gap: 8px; margin-bottom: 4px;">
           <span style="color: #fff; font-size: 16px; font-weight: 700; line-height: 1;">Captcha Bypass Plugin</span>
           <span style="background: rgba(255,255,255,0.2); color: #fff; font-size: 11px; font-weight: 600; padding: 2px 8px; border-radius: 20px; line-height: 1.5;">v1.1.0</span>
         </div>
         <div style="color: rgba(255,255,255,0.82); font-size: 13px; line-height: 1.4;">Automatically solve captchas during directory submissions — <strong style="color:#fff;">fully automated link building</strong> with no manual interruptions.</div>
       </div>
     </div>
     <a href="https://www.seopanel.org/plugin/l/114/captcha-recognition/" target="_blank"
        style="display: inline-flex; align-items: center; gap: 8px; background: #fff; color: #7c2d12; padding: 10px 22px; border-radius: 7px; font-weight: 700; font-size: 14px; text-decoration: none; box-shadow: 0 2px 8px rgba(0,0,0,0.18); white-space: nowrap; transition: opacity .2s;"
        onmouseover="this.style.opacity='.88'" onmouseout="this.style.opacity='1'">
       <i class="fa fa-download"></i> Download
     </a>
   </div>

Captcha Bypass integrates SEO Panel's Directory Submission tool with leading captcha solving services. When a captcha challenge appears during a directory submission, the plugin automatically sends it to the configured solving service and returns the answer — allowing submissions to proceed without manual intervention.

The plugin menu provides the following sections (admin only):

- **Captcha Bypass Manager** – Configure captcha solving service accounts
- **Settings** – Global plugin settings

~~~~~~~~~~~~~~~~~~~~~~
Captcha Bypass Manager
~~~~~~~~~~~~~~~~~~~~~~

The Captcha Bypass Manager lists all configured captcha solving service accounts. Each entry shows the service name, type (identifier), username, and status.

**Supported Services**

- **Death By Captcha** (deathbycaptcha)
- **Anti-Captcha** (anti-captcha)
- **2Captcha** (2captcha)
- **RuCaptcha** (rucaptcha)
- **Captchas.io** (captchas.io)

**Adding a New Captcha Service**

1. Click **New Captcha Bypass Service**
2. Enter a **Name** to identify this account
3. Select the **Service Type** (identifier)
4. Enter your **Username** for the service
5. Enter your **Password**
6. Enter your **API Key** (if required by the selected service)
7. Click **Proceed** to save

**Service Actions**

- **Activate / Inactivate** – Enable or disable this service for use during submissions
- **Edit** – Update credentials
- **Delete** – Remove the service account

~~~~~~~~
Settings
~~~~~~~~

Plugin Settings (admin only) allows configuring how the captcha bypass behaves globally within SEO Panel's directory submission workflow.

.. note::
   Once a captcha solving service is configured and activated, SEO Panel's Directory Submission tool will automatically use it whenever a captcha is encountered. No additional setup is required in the directory submission workflow.
