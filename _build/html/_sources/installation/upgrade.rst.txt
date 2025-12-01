SEO Panel Upgrade
=================

.. admonition:: Critical - Read Before Upgrading

   - **Always backup** your database and files before upgrading
   - Test the upgrade on a staging environment first if possible
   - Plan for maintenance window - put site in maintenance mode
   - Keep the old version until you confirm the upgrade is successful
   - Document your current version and target version


Upgrade Methods
---------------

**Method 1: Quick Upgrade (Recommended for Beginners)**

Use **Bitnami / Softaculous / Installatron / Webuzo / AMPPS** one-click upgrade tools.

**Method 2: Manual Upgrade**

Follow the detailed steps below for manual upgrade with full control.

**Method 3: Docker Upgrade**

See Docker Upgrade section for containerized deployments.


Pre-Upgrade Checklist
----------------------

Before starting the upgrade, complete these essential steps:

1. **Check Current Version**

   Log in to SEO Panel and note your current version from the dashboard.

2. **Review Release Notes**

   Visit https://www.seopanel.org/changelog/ to review changes and breaking updates.

3. **Check PHP Compatibility**

   Ensure your server meets the requirements for the new version:

   .. code-block:: bash

      php -v  # Should be PHP 7.4 or higher

4. **Verify Disk Space**

   Ensure you have enough disk space (at least 500MB free recommended).

5. **Put Site in Maintenance Mode**

   Create a maintenance page or use your hosting control panel to enable maintenance mode.


Complete Backup Procedure
--------------------------

**Critical:** Never skip this step!

1. **Backup Database**

   .. code-block:: bash

      # Using mysqldump
      mysqldump -u seopanel_user -p seopanel_db > seopanel_backup_$(date +%Y%m%d_%H%M%S).sql

      # Or using MySQL Workbench / phpMyAdmin export feature

2. **Backup Files**

   .. code-block:: bash

      # Create complete backup of SEO Panel directory
      tar -czf seopanel_backup_$(date +%Y%m%d_%H%M%S).tar.gz /path/to/seopanel/

      # Or using FTP client, download the entire seopanel folder

3. **Verify Backups**

   .. code-block:: bash

      # Check backup file exists and has content
      ls -lh seopanel_backup_*.sql
      ls -lh seopanel_backup_*.tar.gz

4. **Store Backups Safely**

   - Copy backups to a different server or local machine
   - Do not store backups in the same directory as SEO Panel


Manual Upgrade Steps
--------------------

1. **Rename Current Installation**

   .. code-block:: bash

      # Via SSH/Terminal
      cd /var/www/html  # or your web root
      mv seopanel seopanel_old_$(date +%Y%m%d)

      # Or via FTP: Rename seopanel to seopanel_old

   This preserves your old installation for quick rollback if needed.

2. **Download Latest Version**

   .. code-block:: bash

      # Download latest version
      wget https://www.seopanel.org/download/seo-panel-latest.zip

      # Or download from: https://www.seopanel.org/download/

3. **Extract New Version**

   .. code-block:: bash

      # Extract the package
      unzip seo-panel-latest.zip

      # Rename to your desired directory name
      mv seopanel-x.x.x seopanel

   Or extract locally and upload via FTP to your web server.

4. **Copy Configuration File**

   .. code-block:: bash

      # Copy your old config to new installation
      cp seopanel_old_*/config/sp-config.php seopanel/config/

      # If that file doesn't exist, copy from sample
      cp seopanel/config/sp-config-sample.php seopanel/config/sp-config.php

5. **Update Configuration Settings**

   Edit **config/sp-config.php** with your existing database credentials:

   .. code-block:: php

      <?php
      # The web path or url to access seo panel through browser.
      define('SP_WEBPATH', 'https://yourdomain.com/seopanel');

      # DB settings - Use your existing database credentials
      define('DB_NAME', 'seopanel_db');
      define('DB_USER', 'seopanel_user');
      define('DB_PASSWORD', 'your_secure_password');
      define('DB_HOST', 'localhost');

      # Database type (mysqli is recommended for PHP 7+)
      define('DB_ENGINE', 'mysqli');
      ?>

   **Important:** Update SP_WEBPATH to use HTTPS if you have SSL enabled.

6. **Copy Custom Files and Plugins**

   .. code-block:: bash

      # Copy custom plugins
      cp -r seopanel_old_*/plugins/custom_* seopanel/plugins/

      # Copy custom themes (if any)
      cp -r seopanel_old_*/themes/custom_* seopanel/themes/

      # Copy any custom uploads or data
      cp -r seopanel_old_*/uploads/* seopanel/uploads/

7. **Set File Permissions**

   .. code-block:: bash

      # Set proper ownership (replace www-data with your web server user)
      chown -R www-data:www-data seopanel/

      # Set directory permissions
      find seopanel/ -type d -exec chmod 755 {} \;

      # Set file permissions
      find seopanel/ -type f -exec chmod 644 {} \;

      # Set tmp directory writable
      chmod 755 seopanel/tmp/

8. **Run Database Upgrade**

   Visit the upgrade script in your web browser:

   ``https://yourdomain.com/seopanel/install/upgrade.php``

   .. image:: _static/sp_upgrade1.png

   **Follow the upgrade wizard:**

   - The system will detect your current version
   - Review the changes to be made
   - Click "Proceed" to start the database upgrade

   .. image:: _static/sp_upgrade2.png

9. **Complete Upgrade**

   After successful database upgrade:

   .. code-block:: bash

      # Remove install directory (Critical for security!)
      rm -rf seopanel/install/

      # Or via FTP: Delete the install folder

10. **Verify Upgrade**

    - Log in to SEO Panel admin panel
    - Check the version number in the dashboard
    - Test key functionality:
      - Check websites are listed correctly
      - Run a quick rank check
      - Verify reports are accessible
      - Test user permissions


Post-Upgrade Tasks
------------------

1. **Clear Cache**

   .. code-block:: bash

      # Clear application cache
      rm -rf seopanel/tmp/cache/*

2. **Test All Features**

   - Verify all plugins are working
   - Check scheduled tasks/cron jobs
   - Test API integrations (MOZ, Google, etc.)
   - Verify email notifications

3. **Update Cron Jobs**

   Check if cron job paths need updating:

   .. code-block:: bash

      # Edit crontab
      crontab -e

      # Ensure paths point to new installation
      */30 * * * * php /var/www/html/seopanel/cron.php

4. **Disable Maintenance Mode**

   Remove maintenance page and restore normal operation.

5. **Monitor for Issues**

   - Check error logs: ``seopanel/tmp/logs/``
   - Monitor server logs for any PHP errors
   - Watch for user-reported issues

6. **Keep Old Version Temporarily**

   Keep ``seopanel_old_*`` directory for 7-14 days before deleting, in case rollback is needed.


Docker Upgrade
--------------

For Docker-based installations:

1. **Backup Database**

   .. code-block:: bash

      # Backup database from Docker container
      docker exec seopanel_mysql mysqldump -u seopanel_user -pYOUR_PASSWORD seopanel_db > backup.sql

2. **Update docker-compose.yml**

   Update the SEO Panel image version or rebuild with new code:

   .. code-block:: yaml

      services:
        seopanel:
          image: php:8.1-apache  # Update PHP version if needed
          # ... rest of configuration

3. **Pull New Images**

   .. code-block:: bash

      docker-compose pull

4. **Stop Containers**

   .. code-block:: bash

      docker-compose down

5. **Update Application Files**

   .. code-block:: bash

      # Download and extract new version to mounted volume
      cd /path/to/docker/volumes/seopanel
      wget https://www.seopanel.org/download/seo-panel-latest.zip
      unzip seo-panel-latest.zip
      # Copy files to mounted directory

6. **Start Containers**

   .. code-block:: bash

      docker-compose up -d

7. **Run Upgrade Script**

   Access upgrade.php through your browser and follow the wizard.

8. **Remove Install Directory**

   .. code-block:: bash

      docker exec seopanel rm -rf /var/www/html/install


Rollback Procedure
------------------

If the upgrade fails or causes issues:

1. **Stop Web Server** (if possible)

   .. code-block:: bash

      sudo systemctl stop apache2  # or nginx

2. **Restore Database**

   .. code-block:: bash

      # Drop current database and restore backup
      mysql -u root -p -e "DROP DATABASE seopanel_db;"
      mysql -u root -p -e "CREATE DATABASE seopanel_db CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;"
      mysql -u seopanel_user -p seopanel_db < seopanel_backup_YYYYMMDD_HHMMSS.sql

3. **Restore Files**

   .. code-block:: bash

      # Remove failed upgrade
      rm -rf seopanel/

      # Restore old version
      mv seopanel_old_YYYYMMDD seopanel

4. **Restart Web Server**

   .. code-block:: bash

      sudo systemctl start apache2  # or nginx

5. **Verify Rollback**

   - Access SEO Panel and confirm it's working
   - Check that you're back to the previous version


Troubleshooting Upgrade Issues
-------------------------------

**Issue: Database upgrade fails**

- Check database user has ALTER, CREATE, DROP privileges
- Verify database connection settings in sp-config.php
- Check MySQL/PHP error logs for specific errors
- Try running upgrade.php again (it should be safe to re-run)

**Issue: White screen after upgrade**

- Enable PHP error display temporarily
- Check file permissions (644 for files, 755 for directories)
- Verify PHP version compatibility
- Check Apache/Nginx error logs

**Issue: Plugins not working**

- Deactivate and reactivate plugins
- Check plugin compatibility with new version
- Update plugins to latest versions
- Check plugin directory permissions

**Issue: Missing data after upgrade**

- This should not happen if upgrade completed successfully
- Restore from backup and try upgrade again
- Check database tables are present: ``SHOW TABLES LIKE 'seopanel_%';``

**Issue: Performance degraded after upgrade**

- Clear all caches: ``rm -rf seopanel/tmp/cache/*``
- Optimize database tables
- Check PHP memory_limit and max_execution_time
- Review new version's system requirements


Version-Specific Upgrade Notes
-------------------------------

**Upgrading from very old versions (3.x to 4.x)**

- Major version upgrades may require intermediate upgrades
- Review all changelogs between versions
- Expect longer upgrade time for database migrations
- Consider fresh install + data migration for very old versions

**PHP Version Upgrades**

If upgrading PHP version alongside SEO Panel:

- Test compatibility thoroughly
- Update PHP extensions as needed
- Review deprecated PHP functions in custom code
- Update configuration files if needed


Support Resources
-----------------

If you encounter issues during upgrade:

- Official Documentation: https://www.seopanel.org/docs/
- GitHub Issues: https://github.com/seopanel/seopanel
- Support System: Open a ticket through the official website

**Before contacting support, gather:**

- Current SEO Panel version
- Target upgrade version
- PHP version (``php -v``)
- MySQL version (``mysql -V``)
- Error messages from logs
- Steps you've already tried
