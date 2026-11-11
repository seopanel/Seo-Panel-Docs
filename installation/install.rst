.. title:: SEO Panel Installation Guide | Manual, One-Click & Docker Setup

.. meta::
   :description: Step-by-step SEO Panel installation guide — manual setup, one-click installers (Softaculous, Installatron, Webuzo), cloud hosting and Docker deployment.

SEO Panel Installation
======================

.. raw:: html

   <div style="background: linear-gradient(135deg, #1a6b3c 0%, #2d9e5f 50%, #34a85a 100%); border-radius: 10px; padding: 14px 20px; margin: 16px 0 28px 0; display: flex; align-items: center; justify-content: space-between; flex-wrap: wrap; gap: 12px; box-shadow: 0 4px 14px rgba(26,107,60,0.35);">
     <div style="display: flex; align-items: center; gap: 14px;">
       <div style="background: rgba(255,255,255,0.15); border-radius: 8px; width: 42px; height: 42px; display: flex; align-items: center; justify-content: center; flex-shrink: 0;">
         <i class="fa fa-download" style="color: #fff; font-size: 20px;"></i>
       </div>
       <div>
         <div style="display: flex; align-items: center; gap: 8px; margin-bottom: 3px;">
           <span style="color: #fff; font-size: 15px; font-weight: 700; line-height: 1;">SEO Panel</span>
           <span style="background: rgba(255,255,255,0.2); color: #fff; font-size: 11px; font-weight: 600; padding: 2px 8px; border-radius: 20px; line-height: 1.5;">Latest</span>
           <span style="background: rgba(255,255,255,0.15); color: #fff; font-size: 11px; font-weight: 600; padding: 2px 8px; border-radius: 20px; line-height: 1.5;">Free</span>
         </div>
         <div style="color: rgba(255,255,255,0.85); font-size: 12px; line-height: 1.4;">Download the latest stable release and get started in minutes.</div>
       </div>
     </div>
     <a href="https://www.seopanel.org/download/" target="_blank"
        style="display: inline-flex; align-items: center; gap: 8px; background: #fff; color: #1a6b3c; padding: 9px 20px; border-radius: 7px; font-weight: 700; font-size: 14px; text-decoration: none; box-shadow: 0 2px 8px rgba(0,0,0,0.18); white-space: nowrap;"
        onmouseover="this.style.opacity='.88'" onmouseout="this.style.opacity='1'">
       <i class="fa fa-download"></i> Download
     </a>
   </div>

.. admonition:: Important

   Please install SEO Panel in a *subdirectory of your website* like https://yourwebsite.com/seopanel to prevent any issues with your main website.


Installation Methods
--------------------

**Method 1: Cloud Hosted (Zero Setup)**

Get a cloud-hosted SEO Panel instance ready in 2 minutes with no server configuration required.

**Method 2: One-Click Installers (Recommended for Beginners)**

Use **Softaculous**, **Installatron**, **Webuzo**, or **AMPPS** to install SEO Panel with a single click from your hosting control panel.

**Method 3: Manual Installation**

Follow the steps below for a manual 5-minute installation.

**Method 4: Docker Installation**

See the Docker Installation section below for containerised deployment.


Manual Installation Steps
-------------------------

1. **Download & Extract**

   Download the latest version from: https://www.seopanel.org/download/

   Unzip the package to your local computer.

2. **Upload Files**

   Transfer all files to a web-accessible directory on your server via FTP, maintaining the directory structure.

   Recommended path: ``public_html/seopanel`` or ``/var/www/html/seopanel``

3. **Set Config File Permissions**

   .. code-block:: bash

      chmod 666 config/sp-config.php

   Or set to ``-rw-rw-rw-`` via your FTP client.

4. **Set Temp Directory Permissions**

   .. code-block:: bash

      chmod 777 tmp

   Or set to ``-rwxrwxrwx`` via your FTP client.

5. **Run the Installation Wizard**

   Open your web browser and visit:

   ``http://www.yourdomain.com/seopanel/install/``

   .. image:: _static/sp_install1.png

6. **Complete the Setup Form**

   Follow the on-screen instructions and fill in all required information:

   - Database host, name, username and password
   - Admin language and timezone
   - Admin credentials

   .. image:: _static/sp_install2.png

   .. image:: _static/sp_install3.png

7. **Secure the Config File**

   After installation completes, lock down the config file:

   .. code-block:: bash

      chmod 644 config/sp-config.php

   Or set to ``-rw-r--r--`` via your FTP client.

8. **First Login**

   Access the admin panel at: ``https://yourdomain.com/seopanel/``

   **Default login credentials:**

   - Username: ``spadmin``
   - Password: ``spadmin``

   .. admonition:: Security Warning

      Change the default password immediately after your first login. Click your profile link (top right) to update it.

9. **Configure MOZ API**

   Go to **Admin Panel → System Settings → MOZ Settings** and add your MOZ API key.

   Get a free API key at: https://moz.com/help/guides/moz-api/


Post-Installation Security Steps
---------------------------------

.. admonition:: Security Checklist

    - ✓ Change default admin password immediately
    - ✓ Remove the ``install/`` directory after installation
    - ✓ Use HTTPS/SSL encryption
    - ✓ Keep SEO Panel updated to the latest version
    - ✓ Use strong, unique database passwords
    - ✓ Regular backups of database and files

**Remove the install directory (required):**

.. code-block:: bash

   rm -rf install/

Failing to remove this directory is a serious security risk.


Docker Installation
-------------------

For a modern, containerised deployment:

1. **Create docker-compose.yml**

   .. code-block:: yaml

      version: '3.8'

      services:
        seopanel:
          image: php:8.1-apache
          container_name: seopanel
          ports:
            - "8080:80"
          volumes:
            - ./seopanel:/var/www/html
          environment:
            - MYSQL_HOST=mysql
            - MYSQL_DATABASE=seopanel_db
            - MYSQL_USER=seopanel_user
            - MYSQL_PASSWORD=strong_password_here
          depends_on:
            - mysql

        mysql:
          image: mysql:8.0
          container_name: seopanel_mysql
          environment:
            - MYSQL_ROOT_PASSWORD=root_password_here
            - MYSQL_DATABASE=seopanel_db
            - MYSQL_USER=seopanel_user
            - MYSQL_PASSWORD=strong_password_here
          volumes:
            - mysql_data:/var/lib/mysql

      volumes:
        mysql_data:

2. **Start Containers**

   .. code-block:: bash

      docker-compose up -d

3. **Access Installation**

   Visit: ``http://localhost:8080/install/``

   Follow the web installer steps above.


===============
Video Tutorials
===============

**Tutorial 1**

.. raw:: html

	<div class="embed-responsive embed-responsive-16by9">
    	<iframe class="embed-responsive-item" src="https://www.youtube.com/embed/pVjoJDbi9KI" frameborder="0" allowfullscreen></iframe>
    </div>


**Tutorial 2**

.. raw:: html

	<div class="embed-responsive embed-responsive-16by9">
    	<iframe class="embed-responsive-item" src="https://www.youtube.com/embed/9CN4MDu2eNY" frameborder="0" allowfullscreen></iframe>
    </div>


**How to Install Seo Panel Using Softaculous**

.. raw:: html

	<div class="embed-responsive embed-responsive-16by9">
    	<iframe src="https://player.vimeo.com/video/31817285" class="embed-responsive-item" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>
    </div>


If you have any issues during installation, please contact the SEO Panel team or open a ticket in the support system.
