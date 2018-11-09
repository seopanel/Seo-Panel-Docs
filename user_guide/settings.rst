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

   https://moz.com/help/guides/moz-api/mozscape/getting-started-with-mozscape/create-and-manage-your-account

3) Enter details as following screen shot

   .. image:: ../_static/sp_moz_settings.png

   - **Access ID** - The access id of MOZ API
   
   - **Secret Key** - The secret key of MOZ API
   
   **Click on `Verify connection`** link to verify the API settings are working
   
   
~~~~~~~~~~~~~~~
Google Settings
~~~~~~~~~~~~~~~

Setup Google API to get website informations from google api resources.


~~~~~~~~~~~~~~
Google API Key
~~~~~~~~~~~~~~

Google API key is mainly used for accessing public api resources like Pagespeed checker

1) Go to **Admin Panel => System Settings=> Google Settings**

2) **Click on `Click here to get Google API Key`** link to get google API key

   https://support.google.com/googleapi/answer/6158862?hl=en

3) Enter details as following screen shot

   .. image:: ../_static/sp_google_settings.png

   - **Google API Key** - The google API key generated using above step
   
   **Click on `Verify connection`** link to verify the API Key settings are working

   
~~~~~~~~~~~~~~~~~~~~~~~~~
Google OAuth2 credentials
~~~~~~~~~~~~~~~~~~~~~~~~~

Google OAuth2 credentials used for accessing private resources api using secured connection. It requires user authentication to access the api resources.

Eg: Webmaster Tools

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
   
      If your seo panel is setup in a link http://testdomain.com/seopanel or http://seopanel.testdomain.com/, add **testdomain.com** in **Authorised domains** section.
   
   8) Click **Create credentials** and then select **OAuth client ID**
   
      .. image:: ../_static/google_qauth_step1.png
      
      You will be redirected to a page like below image
   
      .. image:: ../_static/google_qauth_step4.png
   
   9) Select **Application type**  as **Web application**

      - **Authorised JavaScript origins** - 
      
         If your seo panel is setup in a link http://testdomain.com/seopanel use http://testdomain.com
         If your seo panel is setup in a link http://seopanel.testdomain.com/ use http://seopanel.testdomain.com

      - **Authorised redirect URIs** - From below image enter **Authorised redirect URI**

         .. image:: ../_static/sp_google_settings.png
   
   9) After submission you will get Google **Client Id** and **Client Secret** from below screen
   
      .. image:: ../_static/google_qauth_step1.png
      
      Enter details as following screen shot

         .. image:: ../_static/sp_google_settings.png
      
         - **Google API Client Id** - The google **Client Id** generated using above step
      
         - **Google API Client Secret** - The google **Client Secret** generated using above step
         
      
3) Enable Google API used for seo panel
   
      1) Webmaster Tools
      
         Go to https://console.developers.google.com/apis/library/webmasters.googleapis.com
         
         Then click on **ENABLE** button
      
      2) PageSpeed Insights API
      
         Go to https://console.developers.google.com/apis/library/pagespeedonline.googleapis.com
         
         Then click on **ENABLE** button
   

~~~~~~~~~~~~~~~~
Google Analytics
~~~~~~~~~~~~~~~~

Google analytics code used to know the number of visitors accessing your seo panel.

1) Go to **Admin Panel => System Settings=> Google Settings**

2) Enter details as following screen shot

   .. image:: ../_static/sp_google_settings.png

   - **Google Analytics Tracking Code** - Enter the corresponding code from google analytics for your seo panel.
   
   Go to google analytics dashboard and verify the code is working.