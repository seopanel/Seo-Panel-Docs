SEO Panel Installation
======================

.. admonition:: Important

   Please install SEO Panel in a *subdirectory of your website* like https://yourwebsite.com/seopanel to prevent any issues with your main website.


Installation Methods
--------------------

**Method 1: Quick Install (Recommended for Beginners)**

Simply use **Bitnami / Softaculous / Installatron / Webuzo / AMPPS** to install SEO Panel with one click.

**Method 2: Manual Installation**

Follow the steps below for manual installation.

**Method 3: Docker Installation**

See the Docker Installation section below for containerized deployment.


Manual Installation Steps
-------------------------

1. **Download Latest Version**

   Download the latest version from: https://www.seopanel.org/download/

   Extract the package to your local machine.

2. **Upload Files**

   Upload all files (maintaining the directory structure) to a web-accessible directory on your server.

   Recommended path: ``/var/www/html/seopanel`` or ``public_html/seopanel``

3. **Set File Permissions (Temporary)**

   .. code-block:: bash

      # For Linux/Unix servers
      chmod 666 config/sp-config.php
      chmod 777 tmp/

   **Note:** These are temporary permissions for installation only and will be secured in step 7.

4. **Create Database**

   Create a MySQL/MariaDB database and user for SEO Panel:

   .. code-block:: sql

      CREATE DATABASE seopanel_db CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;
      CREATE USER 'seopanel_user'@'localhost' IDENTIFIED BY 'strong_password_here';
      GRANT ALL PRIVILEGES ON seopanel_db.* TO 'seopanel_user'@'localhost';
      FLUSH PRIVILEGES;

5. **Run Web Installer**

   Visit the installation URL in your web browser:

   ``https://yourdomain.com/seopanel/install/``

   .. image:: _static/sp_install1.png

   **Enter Database Details**

   - Database Host: localhost (or your database server)
   - Database Name: seopanel_db
   - Database Username: seopanel_user
   - Database Password: (the password you created)

   .. image:: _static/sp_install2.png

   **Configure Admin Settings**

   - Select admin language
   - Set timezone for your location
   - Create a strong admin password (don't use default!)

   .. image:: _static/sp_install3.png

6. **Complete Installation**

   Follow the on-screen instructions to complete the installation.

7. **Secure Your Installation (Critical)**

   .. code-block:: bash

      # Secure config file permissions
      chmod 644 config/sp-config.php

      # Secure tmp directory (allow only web server write access)
      chmod 755 tmp/

      # Remove installation directory
      rm -rf install/

   **Important:** Failing to remove the install directory is a serious security risk!

8. **First Login**

   Access the admin panel at: ``https://yourdomain.com/seopanel/``

   **Default Login Credentials:**

   - Username: ``spadmin``
   - Password: ``spadmin`` (or the password you set during installation)

9. **Immediate Security Steps (Required)**

   a. **Change Admin Password**

      - Click on your profile (top right corner)
      - Change the default password immediately
      - Use a strong password (12+ characters, mixed case, numbers, symbols)

   b. **Configure API Keys**

      Go to **Admin Panel => System Settings => MOZ Settings**

      Add your free MOZ API key: https://moz.com/help/guides/moz-api/

   c. **Review Security Settings**

      - Enable HTTPS/SSL if available
      - Configure proper backup procedures
      - Review user permissions

10. **Additional Configuration**

    - Configure cron jobs for automated tasks
    - Set up email settings for notifications
    - Configure proxy settings if needed


Docker Installation
-------------------

For a modern, containerized deployment:

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


Security Best Practices
-----------------------

.. admonition:: Security Checklist

    - ✓ Change default admin password immediately
    - ✓ Remove install/ directory after installation
    - ✓ Use HTTPS/SSL encryption
    - ✓ Keep SEO Panel updated to latest version
    - ✓ Use strong, unique database passwords
    - ✓ Restrict database access to localhost only
    - ✓ Regular backups of database and files
    - ✓ Use file permissions: 644 for files, 755 for directories
    - ✓ Disable directory listing in web server
    - ✓ Keep PHP and server software updated


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


If you have any issues while installation, Please contact seo panel team or open a ticket in support system 
