.. title:: SEO Panel Settings Manager | System Configuration Guide

.. meta::
   :description: Guide for seo panel setting manager with email settings, Time zone, company name etc  


Settings
~~~~~~~~

~~~~~~~~~~~~~~~
System Settings
~~~~~~~~~~~~~~~

Next step is to update system settings according to your environment.

1) Go to **Admin Panel => System Settings=> System Settings**

2) Enter details as following screen shot

   .. image:: ../_static/sp_settings1.png

   - **Seo Panel Title** - The title of your seo panel installation *Eg:* Smith's seo panel 
   
   - **Seo Panel Description** - The meta description of your seo panel installation
   
   - **Seo Panel Keywords** - The meta keywords of your seo panel installation
   
   - **Number of entries per page** - The max number of entries to start pagination(Default value is '10')  
   
   - **User registration interface** - Enable / Disable users to register in your seo panel 
   
   - **Default Language** - The default language of your seo panel
   
   - SMTP Settings
   
      - **Enable SMTP** - Enable / Disable smtp settings for sending mail from seo panel
      
      - **SMTP Host** - The hostname of smtp server(default value is 'localhost')
       
      - **SMTP Username** - SMTP account username 
      
      - **SMTP Password** - SMTP account password 
      
      - **SMTP Mail Port** - SMTP mail port used(default value is '25')
       
       
   - **Time Zone:** - Your timezone to see reports in your time 
    
   - **Company Name** - The name of your company
    
   - **Currency** - Currency used in seo panel transactions
   

~~~~~~~~~~~~
MOZ Settings
~~~~~~~~~~~~

Setup MOZ API to get website ranking related informations

1) Go to **Admin Panel => System Settings=> MOZ Settings**

2) **Click on `Click here to get MOZ account`** link to get free MOZ API account

   https://moz.com/checkout/api

3) Enter details as following screen shot

   .. image:: ../_static/sp_moz_settings.png

   - **Access ID** - The access id of MOZ API
   
   - **Secret Key** - The secret key of MOZ API
   
   **Click on `Verify connection`** link to verify the API settings are working
   
   
~~~~~~~~~~~~~~~
Google Settings
~~~~~~~~~~~~~~~

Setup **Google API Key** and **OAuth2 credentials**  to get website informations from google api resources.


~~~~~~~~~~~~~~
Google API Key
~~~~~~~~~~~~~~

**Google API** key is mainly used for accessing public api resources like **Pagespeed checker**


1) Go to **Admin Panel => System Settings=> Google Settings**

2) **Click on `Click here to get Google API Key`** link to get google API key

   https://support.google.com/googleapi/answer/6158862?hl=en

3) Enter google api key generated from above step.

   .. image:: ../_static/sp_google_settings.png

   - **Google API Key** - The google API key generated using above step
   

**Click on `Verify connection`** link to verify the API Key settings are working

   
~~~~~~~~~~~~~~~~~~~~~~~~~
Google OAuth2 credentials
~~~~~~~~~~~~~~~~~~~~~~~~~

Google OAuth2 credentials used for accessing private api resources using secured connection.
It requires user authentication to access the api resources.

**Eg:** Webmaster Tools

1) Go to **Admin Panel => System Settings=> Google Settings**

2) **Click on `Click here to get Google API Client Id`** link to get OAuth2 credentials

   https://developers.google.com/adwords/api/docs/guides/authentication
   
   **Steps to create the OAuth2 credentials**
   
   1) Go to the **API Console**
   
      https://console.developers.google.com/
   
   2) From the projects list, select a project or create a new one.
   
   3) If the APIs & services page isn't already open, open the left side menu and select **APIs & services**.
   
   4) On the left, choose **Credentials**
   
   5) Click **Create credentials** and then select **OAuth client ID**
   
      .. image:: ../_static/google_qauth_step1.png
      
   6) Configure **Consent Screen**, If you didn't configure earlier. Click on **Configure consent screen**
   
      .. image:: ../_static/google_qauth_step2.png
      
   7) Configure **Consent Screen** like below image
   
      .. image:: ../_static/google_qauth_step3.png
   
      
      If your seo panel is setup in a link 
      
      http://testdomain.com/seopanel or http://seopanel.testdomain.com/ 
      
      Add **testdomain.com** in **Authorised domains** section.
      
   
   8) Once Consent Screen is configured, Click on **Create credentials** and then select **OAuth client ID**
   
      .. image:: ../_static/google_qauth_step1.png
      
   9) You will be redirected to a page like below image and Select **Application type**  as **Web application**
		
	  .. image:: ../_static/google_qauth_step4.png
   	  

      - **Authorised JavaScript origins** 
      
         If your seo panel is setup in a link http://testdomain.com/seopanel use http://testdomain.com
         
         If your seo panel is setup in a link http://seopanel.testdomain.com/ use http://seopanel.testdomain.com
         

      - **Authorised redirect URIs** - From below image screen copy **Authorised redirect URI**

         .. image:: ../_static/sp_google_settings.png
         
   
   10) After submission you will get Google **Client Id** and **Client Secret** from below screen
   
      .. image:: ../_static/google_qauth_step5.png
      
      
      Enter details as following screen shot

         .. image:: ../_static/sp_google_settings.png
      
         - **Google API Client Id** - The google **Client Id** generated using above step
      
         - **Google API Client Secret** - The google **Client Secret** generated using above step
         
      
3) **Enable Google API** used for seo panel

   
      1) **Webmaster Tools**
      
         Go to https://console.developers.google.com/apis/library/searchconsole.googleapis.com
         
         Then click on **ENABLE** button
         
      
      2) **PageSpeed Insights API**
      
         Go to https://console.developers.google.com/apis/library/pagespeedonline.googleapis.com
         
         Then click on **ENABLE** button
         
      
      3) **Google Analytics API**
      
         Go to https://console.developers.google.com/apis/library/analyticsreporting.googleapis.com
         
         Then click on **ENABLE** button
         
         
4) **Connect to your google account**


	Each user needs to **connect** to their own google account to provide access to their webmaster tools, analytics etc
      
	.. include:: google_connection.rst
      
   

~~~~~~~~~~~~~~~~~~~
DataForSEO Settings
~~~~~~~~~~~~~~~~~~~

New in Seo Panel 7.0.0. DataForSEO is an alternative data source several checker tools can use instead of (or alongside) a direct crawl: Review Checker, Backlink/Saturation Checker, SERP Checker, and the new Keyword Search Volume and Google AI Overview tracking under **AI SERP Overview**.

1) Go to **Admin Panel => System Settings => DataForSEO Settings**

2) **Click on `Click here to get Free DataForSEO account`** link if you don't already have one

   https://dataforseo.com/

3) Enter details as following screen shot

   .. image:: ../_static/sp_settings_dataforseo.png

   - **Enable DataForSEO** - Master switch for this integration. Leave this on **No** until your API login/password are saved - every sub-toggle below is ignored while this is off

   - **API Login** / **API Password** - Credentials from your DataForSEO dashboard

   - **DataForSEO Balance($)** - Your remaining account balance, shown read-only once connected

   - **Enable for Backlink and Saturation Checker** - Use DataForSEO as the data source for the Backlink Checker and Search Engine Saturation Checker

   - **Enable Sandbox** - Use DataForSEO's sandbox (test) endpoints instead of live ones - no real credits are spent, but results are dummy data. Useful while wiring things up

   - **Enable for Review Checker** - Use DataForSEO for the async Google/Trustpilot/TripAdvisor Review Checker

   - **Enable for SERP Checker** - Use DataForSEO as a source for the Keyword Position Checker, and feeds the AI Overview presence/citation data shown on **AI SERP Overview** and **SERP Results Archive**

   - **Enable for Search Volume** - Turns on the **Search Volume** column shown alongside your tracked keywords (see :ref:`Keyword Position Summary <keyword-position-summary>`)

   **Click on `Verify connection`** link to confirm your login/password are valid before relying on them


~~~~~~~~~~~~~~~~~~~~~~
Seo Panel API Settings
~~~~~~~~~~~~~~~~~~~~~~

New in Seo Panel 7.0.0. The hosted **Seo Panel API** (spAPI) is a free, optional alternative source for SERP and search volume data - separate from DataForSEO and Moz, and run by the Seo Panel team.

1) Go to **Admin Panel => System Settings => Seo Panel API Settings**

2) If you haven't registered yet, **Click on `Register`** - it's free and needs no credit card

   .. image:: ../_static/sp_settings_seopanel_api.png

   - **API Key** - Issued automatically once you register. **Verify connection**, **Reset API Token** and **Upgrade Token** links sit right next to it

   - **Email** / **Name** - The contact details used for your spAPI registration

   - **Enable for SERP Checker** - Use the Seo Panel API as a source for the Keyword Position Checker

   - **Enable for Search Volume** - Turns on the **Search Volume** column for your tracked keywords, sourced from spAPI instead of (or alongside) DataForSEO

   - **Resetting your API Token** immediately invalidates the old one - update anywhere else it's in use before resetting


~~~~~~~~~~~~~~~~~~
Local AI Settings
~~~~~~~~~~~~~~~~~~

New in Seo Panel 7.0.0. Connects Seo Panel to a local `Ollama <https://ollama.com/>`_ instance running on your own server or network, powering the optional **Summarize with AI** trend buttons found on several report pages (including AI Insights). Nothing here is sent to a third party - the request goes from your Seo Panel server straight to your own Ollama instance.

1) Go to **Admin Panel => System Settings => Local AI Settings**

2) Enter details as following screen shot

   .. image:: ../_static/sp_settings_local_ai.png

   - **Enable Local AI** - Master switch for this feature

   - **Ollama Base URL** - Where your Ollama instance listens, *Eg:* ``http://localhost:11434``

   - **Ollama Model** - The model name to use, *Eg:* ``llama3.2:3b`` - must already be pulled on that Ollama instance

   **Click on `Verify connection`** link to confirm Seo Panel can reach your Ollama instance before relying on it


~~~~~~~~~~~~~~~~
Google Analytics
~~~~~~~~~~~~~~~~

Google analytics code used to know the number of visitors accessing your seo panel.

1) Go to **Admin Panel => System Settings=> Google Settings**

2) Enter details as following screen shot

   .. image:: ../_static/sp_google_settings.png

   - **Google Analytics Tracking Code** - Enter the corresponding code from google analytics for your seo panel.
   

Go to google analytics dashboard and verify the code is working.
