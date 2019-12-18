Installation Steps
~~~~~~~~~~~~~~~~~~

.. admonition:: Warning

   Please install seo panel in *subdirectory of your website* like http://yourwebsite.com/seopanel to prevent any issues with main website.


Simply use **Bitnami / Softaculous / Installatron / Webuzo / AMPPS** to install SEO Panel or Follow the below steps


1. **Download** latest version from following link and **Unzip** the package.

   https://www.seopanel.org/download/

2. **Upload** all the files contained in this folder (retaining the directory structure) to a web accessible directory on your server or hosting account.

3. Change the permissions on **config/sp-config.php** to be writable by all (666 or -rw-rw-rw- within your FTP Client)

4. Change the permissions on the **tmp directory** to be writable by all (777 or -rwxrwxrwx within your FTP Client)

5. Using your web browser visit the location you placed Seo Panel with the addition of **install/index.php** or pointing directly to install/

	Eg: http://yourdomain/seopanel/install/
	
	.. image:: _static/sp_install1.png	
	
	**Enter database details**
	
	.. image:: _static/sp_install2.png

	**Select admin language and timezone**
	
	.. image:: _static/sp_install3.png
	


6. Change the permissions on **config/sp-config.php** to be writable only by yourself (644 or -rw-r--r-- within your FTP Client)

8. Please use following **login details** to access Admin Interface.

    **Username:** spadmin

    **Password:** spadmin
    
    
9. Go to **Admin Panel => System Settings => MOZ Settings**

   Add free **moz api key** in seo panel using the link shown in the page - https://moz.com/help/guides/moz-api/    


.. admonition:: Warning

    - Please change password of administrator by visiting Profile link on right top of the seo panel to prevent from security threats.

    - Remove install directory of seo panel


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
