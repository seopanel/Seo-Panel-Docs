Plugin Management
=================

.. admonition:: Important

   - Only install plugins from trusted sources
   - Always backup your database before installing new plugins
   - Check plugin compatibility with your SEO Panel version
   - Review plugin permissions and requirements


Plugin Installation Process
---------------------------

Plugins must be installed manually by uploading files to the server via FTP/SSH.


Manual Plugin Installation Steps
---------------------------------

1. **Download Plugin**

   Download the plugin from the official SEO Panel plugins repository:

   https://www.seopanel.org/plugins/

   Save the plugin ZIP file to your local computer.

2. **Extract Plugin Archive**

   .. code-block:: bash

      # Extract the plugin ZIP file
      unzip plugin-name.zip

      # This will create a plugin folder, e.g., 'linkdiagnosis'

3. **Upload Plugin Files**

   Upload the extracted plugin folder to the ``/plugins/`` directory:

   **Via FTP:**
   - Connect to your server via FTP
   - Navigate to ``/seopanel/plugins/``
   - Upload the entire plugin folder (e.g., ``linkdiagnosis``)

   **Via SSH:**

   .. code-block:: bash

      # Copy plugin to plugins directory
      cp -r linkdiagnosis /var/www/html/seopanel/plugins/

      # Set proper permissions
      chown -R www-data:www-data /var/www/html/seopanel/plugins/linkdiagnosis
      find /var/www/html/seopanel/plugins/linkdiagnosis -type d -exec chmod 755 {} \;
      find /var/www/html/seopanel/plugins/linkdiagnosis -type f -exec chmod 644 {} \;

4. **Verify Plugin Files**

   Ensure the plugin directory structure is correct:

   .. code-block:: text

      seopanel/
      └── plugins/
          └── linkdiagnosis/
              ├── plugin.php        # Main plugin file
              ├── readme.txt        # Plugin documentation
              ├── install.php       # Installation script (if any)
              └── [other files]

5. **Access Plugin Manager**

   Go to **Admin Panel => Seo Plugins Manager**

   The new plugin should appear in the plugins list.

   .. image:: _static/sp_plugin_installation1.png

6. **Activate Plugin**

   - Locate the plugin in the list
   - Click **"Activate"** button
   - Wait for confirmation message
   - The plugin status will change to "Active"

7. **Configure Plugin**

   After activation:

   - Access the plugin from **"Seo Plugins"** in the main menu
   - Configure plugin settings as needed
   - Set up any required API keys or credentials

   .. image:: _static/sp_plugin_installation2.png

8. **Test Plugin Functionality**

   - Run a test operation with the plugin
   - Check for any error messages
   - Verify results are displayed correctly


Plugin Upgrade Steps
~~~~~~~~~~~~~~~~~~~~

.. admonition:: Critical

   - Always backup your database before upgrading plugins
   - Check the plugin changelog for breaking changes
   - Test plugin upgrades on staging environment first
   - Deactivate plugin before upgrading if experiencing issues


Plugin Upgrade Process
----------------------

Plugins must be upgraded manually by replacing plugin files on the server.


Manual Plugin Upgrade Steps
----------------------------

1. **Check Current Version**

   Go to **Admin Panel => Seo Plugins Manager**

   Note the current version of the plugin you want to upgrade.

2. **Backup Plugin Data** (If Applicable)

   Some plugins store configuration or data:

   .. code-block:: bash

      # Backup plugin database tables (if any)
      mysqldump -u seopanel_user -p seopanel_db plugin_table_name > plugin_backup.sql

3. **Backup Current Plugin**

   .. code-block:: bash

      # Backup the current plugin folder
      cp -r /var/www/html/seopanel/plugins/linkdiagnosis \
            /var/www/html/seopanel/plugins/linkdiagnosis_backup_$(date +%Y%m%d)

      # Or via FTP: Download the plugin folder to your computer

4. **Download New Version**

   Download the latest plugin version from:

   https://www.seopanel.org/plugins/

5. **Deactivate Plugin** (Optional but Recommended)

   Go to **Admin Panel => Seo Plugins Manager**

   Deactivate the plugin before replacing files.

6. **Replace Plugin Files**

   **Via FTP:**
   - Delete the old plugin folder (after backing up!)
   - Upload the new plugin folder

   **Via SSH:**

   .. code-block:: bash

      # Remove old plugin (backup already created)
      rm -rf /var/www/html/seopanel/plugins/linkdiagnosis

      # Extract and copy new version
      unzip linkdiagnosis-new.zip
      cp -r linkdiagnosis /var/www/html/seopanel/plugins/

      # Set proper permissions
      chown -R www-data:www-data /var/www/html/seopanel/plugins/linkdiagnosis
      find /var/www/html/seopanel/plugins/linkdiagnosis -type d -exec chmod 755 {} \;
      find /var/www/html/seopanel/plugins/linkdiagnosis -type f -exec chmod 644 {} \;

7. **Run Database Upgrade** (If Required)

   Go to **Admin Panel => Seo Plugins Manager**

   - Find the upgraded plugin
   - Select **"Upgrade"** from the action dropdown
   - Confirm to run database updates
   - Wait for completion

8. **Reactivate Plugin**

   If you deactivated the plugin:

   - Click **"Activate"** to enable it again
   - Reconfigure settings if needed

9. **Verify Upgrade**

   - Check version number in Plugin Manager
   - Test all plugin features
   - Review logs for any errors


Plugin Compatibility Check
--------------------------

Before installing or upgrading plugins, verify compatibility:

1. **Check SEO Panel Version**

   View your SEO Panel version in the dashboard footer.

2. **Review Plugin Requirements**

   Check the plugin's readme.txt or documentation for:

   - Minimum SEO Panel version
   - PHP version requirements
   - Required PHP extensions
   - Database requirements

3. **Test in Staging** (Recommended)

   If possible, test the plugin in a staging environment first.


Troubleshooting Plugin Issues
------------------------------

**Issue: Plugin doesn't appear in Plugin Manager**

- Check the plugin folder is in ``/plugins/`` directory
- Verify the plugin has a valid ``plugin.php`` file
- Check file permissions (755 for directories, 644 for files)
- Review error logs: ``seopanel/tmp/logs/``

**Issue: Plugin activation fails**

- Check database connectivity
- Verify plugin has proper install.php if required
- Check PHP error logs for specific errors
- Ensure database user has CREATE/ALTER permissions

**Issue: Plugin causes errors after activation**

- Deactivate the plugin immediately
- Check PHP version compatibility
- Review plugin changelog for known issues
- Check for conflicting plugins
- Enable PHP error display to see specific errors

**Issue: Plugin not working after upgrade**

- Clear SEO Panel cache: ``rm -rf seopanel/tmp/cache/*``
- Deactivate and reactivate the plugin
- Check if database upgrade completed successfully
- Review new plugin requirements
- Restore backup and try again if needed

**Issue: White screen after plugin installation**

- Access server via SSH/FTP
- Remove the problematic plugin folder
- Clear cache and restart web server
- Check Apache/Nginx error logs
- Restore from backup if needed


Plugin Security Best Practices
-------------------------------

.. admonition:: Security Checklist

   - ✓ Only install plugins from official SEO Panel repository
   - ✓ Verify plugin developer/author reputation
   - ✓ Read plugin reviews and ratings before installation
   - ✓ Keep plugins updated to latest versions
   - ✓ Remove unused or inactive plugins completely
   - ✓ Review plugin permissions and file access
   - ✓ Monitor plugin activity in logs
   - ✓ Use staging environment for testing new plugins
   - ✓ Backup before installing or upgrading plugins
   - ✓ Check for plugin vulnerabilities before installation


Plugin Management Tips
----------------------

**Regular Maintenance:**

- Review installed plugins quarterly
- Remove plugins that are no longer needed
- Keep all plugins updated to latest versions
- Monitor plugin performance impact
- Check for abandoned or unmaintained plugins

**Performance Optimization:**

- Disable plugins not actively being used
- Monitor plugin memory usage
- Check plugin impact on page load times
- Review plugin database queries for efficiency

**Backup Strategy:**

- Include plugins in regular backup routine
- Document plugin configurations
- Keep copies of plugin settings
- Test plugin restoration procedures


Plugin Resources
----------------

- **Official Plugin Repository:** https://www.seopanel.org/plugins/
- **Plugin Documentation:** Available in each plugin's readme.txt
- **GitHub Issues:** https://github.com/seopanel/seopanel/issues
- **Support System:** Open tickets through official website

**Popular SEO Panel Plugins:**

- Link Diagnosis - Analyze backlink quality
- Social Bookmarker - Submit to social bookmarking sites
- Directory Importer - Import web directory lists
- Blog Commenter - Automated blog commenting
- SEO Panel Customizer - Customize panel appearance
