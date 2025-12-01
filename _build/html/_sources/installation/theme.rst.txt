Theme Management
================

.. admonition:: Important

   - Only install themes from trusted sources
   - Always backup your database before installing new themes
   - Check theme compatibility with your SEO Panel version
   - Preview themes before activating on production sites


Theme Installation Process
--------------------------

Themes must be installed manually by uploading files to the server via FTP/SSH.


Manual Theme Installation Steps
--------------------------------

1. **Download Theme**

   Download the theme from the official SEO Panel themes repository:

   https://www.seopanel.org/themes/

   Save the theme ZIP file to your local computer.

2. **Extract Theme Archive**

   .. code-block:: bash

      # Extract the theme ZIP file
      unzip theme-name.zip

      # This will create a theme folder, e.g., 'odbox'

3. **Upload Theme Files**

   Upload the extracted theme folder to the ``/themes/`` directory:

   **Via FTP:**
   - Connect to your server via FTP
   - Navigate to ``/seopanel/themes/``
   - Upload the entire theme folder (e.g., ``odbox``)

   **Via SSH:**

   .. code-block:: bash

      # Copy theme to themes directory
      cp -r odbox /var/www/html/seopanel/themes/

      # Set proper permissions
      chown -R www-data:www-data /var/www/html/seopanel/themes/odbox
      find /var/www/html/seopanel/themes/odbox -type d -exec chmod 755 {} \;
      find /var/www/html/seopanel/themes/odbox -type f -exec chmod 644 {} \;

4. **Verify Theme Files**

   Ensure the theme directory structure is correct:

   .. code-block:: text

      seopanel/
      └── themes/
          └── odbox/
              ├── theme.php         # Main theme file
              ├── style.css         # Theme stylesheet
              ├── images/           # Theme images
              ├── js/               # JavaScript files (if any)
              ├── readme.txt        # Theme documentation
              └── [other files]

5. **Access Theme Manager**

   Go to **Admin Panel => Themes Manager**

   The new theme should appear in the themes list.

   .. image:: _static/sp_theme_installation.png

6. **Preview Theme** (Optional but Recommended)

   Before activating:

   - Click **"Preview"** to see how the theme looks
   - Test theme responsiveness
   - Check compatibility with your content
   - Verify all elements display correctly

7. **Activate Theme**

   When ready to switch themes:

   - Locate the theme in the list
   - Click **"Activate"** button
   - Wait for confirmation message
   - The theme status will change to "Active"

8. **Configure Theme Settings**

   After activation:

   - Access theme customization options (if available)
   - Upload custom logos or images
   - Configure color schemes
   - Set layout preferences
   - Adjust responsive breakpoints

9. **Test Theme Functionality**

   Thoroughly test the new theme:

   - Check all pages render correctly
   - Test navigation menus
   - Verify mobile responsiveness
   - Check browser compatibility (Chrome, Firefox, Safari, Edge)
   - Test form submissions
   - Verify print styles (if applicable)

10. **Clear Browser Cache**

   .. code-block:: bash

      # Clear server-side cache
      rm -rf /var/www/html/seopanel/tmp/cache/*

   Also clear browser cache (Ctrl+Shift+Delete) to see changes.


Theme Upgrade Steps
~~~~~~~~~~~~~~~~~~~

.. admonition:: Critical

   - Always backup your theme customizations before upgrading
   - Document any custom CSS or template modifications
   - Test theme upgrades on staging environment first
   - Keep old theme folder as backup for 7-14 days


Theme Upgrade Process
---------------------

Themes must be upgraded manually by replacing theme files on the server.


Manual Theme Upgrade Steps
---------------------------

1. **Check Current Version**

   Go to **Admin Panel => Themes Manager**

   Note the current version of your active theme.

2. **Backup Current Theme**

   .. code-block:: bash

      # Create timestamped backup of current theme
      cd /var/www/html/seopanel/themes/
      cp -r odbox odbox_backup_$(date +%Y%m%d_%H%M%S)

      # Or via FTP: Download the theme folder

3. **Document Custom Changes**

   Create a list of any custom modifications:

   - Custom CSS in style.css
   - Modified template files
   - Custom images or logos
   - Configuration changes

4. **Export Customizations**

   Save any custom code or settings:

   .. code-block:: bash

      # Save custom CSS
      cp odbox/style.css odbox_custom_styles_$(date +%Y%m%d).css

      # Save custom images
      cp -r odbox/images/custom odbox_custom_images_backup/

5. **Download New Version**

   Download the latest theme version from:

   https://www.seopanel.org/themes/

6. **Switch to Default Theme** (Recommended)

   Go to **Admin Panel => Themes Manager**

   Activate the default theme temporarily to avoid issues during upgrade.

7. **Replace Theme Files**

   **Via FTP:**
   - Delete the old theme folder (after backing up!)
   - Upload the new theme folder

   **Via SSH:**

   .. code-block:: bash

      # Remove old theme (backup already created)
      rm -rf /var/www/html/seopanel/themes/odbox

      # Extract and copy new version
      unzip odbox-new.zip
      cp -r odbox /var/www/html/seopanel/themes/

      # Set proper permissions
      chown -R www-data:www-data /var/www/html/seopanel/themes/odbox
      find /var/www/html/seopanel/themes/odbox -type d -exec chmod 755 {} \;
      find /var/www/html/seopanel/themes/odbox -type f -exec chmod 644 {} \;

8. **Reapply Customizations**

   Carefully merge your custom changes:

   .. code-block:: bash

      # Review differences between old and new
      diff -r odbox_backup_* odbox/

      # Manually merge custom changes into new theme
      # DO NOT simply copy old files over new ones!

9. **Run Theme Upgrade** (If Required)

   Go to **Admin Panel => Themes Manager**

   - Find the upgraded theme
   - Select **"Upgrade"** from the action dropdown
   - Confirm to run any database updates
   - Wait for completion

10. **Reactivate Theme**

    - Click **"Activate"** on the upgraded theme
    - Clear cache: ``rm -rf seopanel/tmp/cache/*``
    - Refresh browser cache

11. **Verify Upgrade**

   - Test all pages thoroughly
   - Check responsive design on mobile devices
   - Verify custom features still work
   - Test in multiple browsers
   - Review logs for any errors


Theme Compatibility Check
-------------------------

Before installing or upgrading themes:

1. **Check SEO Panel Version**

   View your SEO Panel version in the dashboard.

2. **Review Theme Requirements**

   Check the theme's readme.txt for:

   - Minimum SEO Panel version
   - PHP version requirements
   - Browser compatibility
   - Required features or plugins

3. **Check Browser Support**

   Ensure the theme supports:

   - Chrome (latest 2 versions)
   - Firefox (latest 2 versions)
   - Safari (latest 2 versions)
   - Edge (latest 2 versions)
   - Mobile browsers

4. **Test Responsive Design**

   Preview theme on various screen sizes:

   - Desktop (1920px, 1366px, 1024px)
   - Tablet (768px, 1024px)
   - Mobile (375px, 414px, 360px)


Theme Customization Best Practices
-----------------------------------

**Child Themes (Advanced)**

For extensive customizations, consider creating a child theme:

.. code-block:: text

   seopanel/
   └── themes/
       ├── parent-theme/          # Original theme
       └── parent-theme-child/    # Your customizations

**Custom CSS**

Add custom CSS without modifying theme files:

.. code-block:: css

   /* Create custom.css in theme folder */
   /* Add your custom styles here */

   .custom-header {
       background-color: #your-color;
   }

**Version Control**

Track theme customizations with Git:

.. code-block:: bash

   cd /var/www/html/seopanel/themes/your-theme
   git init
   git add .
   git commit -m "Initial theme customization"


Troubleshooting Theme Issues
-----------------------------

**Issue: Theme doesn't appear in Theme Manager**

- Check the theme folder is in ``/themes/`` directory
- Verify the theme has a valid ``theme.php`` file
- Check file permissions (755 for directories, 644 for files)
- Review error logs: ``seopanel/tmp/logs/``

**Issue: Theme activation fails**

- Check if theme is compatible with SEO Panel version
- Verify all required theme files are present
- Check PHP error logs for specific errors
- Try activating default theme first

**Issue: Broken layout after theme activation**

- Clear browser cache (Ctrl+Shift+Delete)
- Clear server cache: ``rm -rf seopanel/tmp/cache/*``
- Check CSS file is loading (view page source)
- Verify file permissions on CSS files
- Check for JavaScript errors in browser console

**Issue: Theme looks different than preview**

- Clear all caches (browser and server)
- Check if custom CSS is interfering
- Verify all theme files uploaded correctly
- Compare file sizes with original download
- Check for missing images or assets

**Issue: Mobile responsive issues**

- Test with browser developer tools
- Check viewport meta tag in theme header
- Verify media queries in CSS
- Test on actual mobile devices
- Check for JavaScript conflicts

**Issue: Theme performance is slow**

- Optimize images (compress, use appropriate formats)
- Minimize CSS and JavaScript files
- Enable browser caching
- Remove unused CSS/JS
- Consider using a CDN for assets


Theme Security Best Practices
------------------------------

.. admonition:: Security Checklist

   - ✓ Only install themes from official SEO Panel repository
   - ✓ Verify theme developer/author reputation
   - ✓ Read theme reviews before installation
   - ✓ Keep themes updated to latest versions
   - ✓ Remove unused themes completely
   - ✓ Review theme code for suspicious functions
   - ✓ Check for hardcoded external links
   - ✓ Validate theme doesn't load external resources
   - ✓ Backup before installing or upgrading themes
   - ✓ Test themes in staging environment first


Theme Optimization Tips
-----------------------

**Performance:**

- Use optimized images (WebP format when possible)
- Minimize HTTP requests
- Combine and minify CSS/JS files
- Use lazy loading for images
- Enable GZIP compression

**Accessibility:**

- Ensure proper color contrast ratios
- Use semantic HTML elements
- Add ARIA labels where needed
- Test with screen readers
- Ensure keyboard navigation works

**SEO:**

- Use proper heading hierarchy (H1, H2, H3)
- Include schema markup
- Optimize meta tags
- Ensure fast page load times
- Make theme mobile-friendly

**Maintenance:**

- Document all customizations
- Keep themes updated regularly
- Remove unused theme assets
- Monitor theme performance
- Test after each update


Theme Resources
---------------

- **Official Theme Repository:** https://www.seopanel.org/themes/
- **Theme Documentation:** Available in each theme's readme.txt
- **GitHub Issues:** https://github.com/seopanel/seopanel/issues
- **Support System:** Open tickets through official website

**Popular SEO Panel Themes:**

- Classic Theme - Traditional SEO Panel design
- Modern Theme - Contemporary flat design
- Dark Theme - Dark mode interface
- Minimal Theme - Clean, minimalist design
- Responsive Theme - Mobile-first responsive design


Custom Theme Development
------------------------

For developers wanting to create custom themes:

**Basic Theme Structure:**

.. code-block:: text

   mytheme/
   ├── theme.php          # Theme configuration
   ├── style.css          # Main stylesheet
   ├── header.php         # Header template
   ├── footer.php         # Footer template
   ├── sidebar.php        # Sidebar template
   ├── functions.php      # Theme functions
   ├── images/            # Theme images
   ├── js/                # JavaScript files
   └── readme.txt         # Documentation

**Theme Configuration (theme.php):**

.. code-block:: php

   <?php
   // Theme Name: My Custom Theme
   // Description: A custom theme for SEO Panel
   // Version: 1.0.0
   // Author: Your Name
   // Requires: SEO Panel 4.x or higher
   ?>

**Development Best Practices:**

- Follow SEO Panel coding standards
- Use proper PHP templating
- Implement responsive design
- Test cross-browser compatibility
- Document all custom functions
- Include theme preview screenshot
- Provide detailed readme.txt
