Upgrade Steps
~~~~~~~~~~~~~

.. admonition:: Warning

   Before upgrade please take the **backup** of your current seo panel database and code


Simply use **Bitnami / Softaculous / Installatron / Webuzo / AMPPS** to upgrade SEO Panel or Follow the below steps


1. **Change** the current seo panel directory name or move it to another place, e.g seopanel to seopanel_bak

2. **Download** latest version from following link and **Unzip** the package.

   https://www.seopanel.org/download/

3. **Upload** all the files contained in this folder (retaining the directory structure) to a web accessible directory on 
    your server or hosting account.

4. **Copy** the contents of sample config file **config/sp-config-sample.php** to **config/sp-config.php** or remove 
    config/sp-config.php and rename config/sp-config-sample.php to config/sp-config.php

5. Open up **config/sp-config.php** with a text editor like Notepad or similar editor.

   Then **modify the following sections** with your **server and database settings of previous version** of seo panel.
   
   .. code-block:: php
    
      # The web path or url to access seo panel through browser.
      define('SP_WEBPATH', 'http://localhost/seopanel');
      
      # DB settings - You can get this info from your web hosting provider.
      # The name of the database for seo panel
      define('DB_NAME', 'seopanel');
      
      # DB database username
      define('DB_USER', 'root');
      
      # DB database password
      define('DB_PASSWORD', '');
      
      # DB hostname
      define('DB_HOST', 'localhost');
   
6. **Save** the contents of file **config/sp-config.php**

7. Change the permissions on the **'tmp' directory** to be writable by all (777 or -rwxrwxrwx within your FTP Client)

8. Using your web browser visit the location you placed Seo Panel with the addition of **install/upgrade.php** 

    e.g. http://yourdomain/seopanel/install/upgrade.php

9. Follow the steps and fill out all the requested information.

   .. image:: _static/sp_upgrade1.png   
   
   **Proceed to next step**

   .. image:: _static/sp_upgrade2.png


.. admonition:: Warning

   Remove install directory of seo panel
   
   Copy all plugins from **'plugins'** folder of old seo panel folder to 'plugins' folder of new Seo Panel.


If you have any issues while installation, Please contact seo panel team or open a ticket in support system
