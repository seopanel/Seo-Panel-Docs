Plugin Dvelopment Guide
~~~~~~~~~~~~~~~~~~~~~~~

~~~~~~~~~~~~
Introduction
~~~~~~~~~~~~

Seo Panel Plugins help us to **modify, customize, and extend** the features of Seo Panel according to our requirement. Instead of changing the core programming of Seo Panel, you can add extra functionality to Seo Panel with Seo Panel Plugins.
 
**Seo Panel Plugin:** A Seo Panel Plugin is a independant program with a set of extra features, written in the PHP scripting language, that adds a specific set of features or services to the Seo Panel.
 
If you would like to create a new Seo Panel plugin, then first search the plugin in Seo Panel plugin repository - http://www.seopanel.in/plugins/
If it is not existing any where, then use following articles to create a new plugin for Seo Panel and publish it through Seo Panel repository. 

**Note:** This article assumes you are already familiar with the basic functionality of Seo Panel, and PHP programming.


~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Steps to Create a Seo Panel Plugin
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

This section guide us through the steps needs to follow while creating a  new Seo Panel plugin.

--------------------------- 
Names, Files, and Locations
---------------------------


**Plugin Name**
 
The first step for plugin creation is finding a name for your plugin according to the features you would like to implement with it.

**Eg:** The name for a search engine submission plugin can be named like "Search Engine Submitter"

Once you found a name for your plugin, then search it in `Seo Panel plugin repository <http://www.seopanel.in/plugins>`_ to find any other plugin existing with the same name. If it is already existing, then choose another name or create plugin for another feature.



**License**

It is customary to follow the standard header with information about licensing for the Plugin. Most Plugins use the `GPL2 <http://www.gnu.org/licenses/old-licenses/gpl-2.0.html>`_ license used by Seo Panel  or a license `compatible with the GPL2 <http://www.gnu.org/licenses/license-list.html#GPLCompatibleLicenses>`_. To indicate a GPL2 license, include the following lines in all files of your Plugin:

.. code-block:: php

    <?php
    /*  Copyright YEAR  PLUGIN_AUTHOR_NAME  (email : PLUGIN AUTHOR EMAIL)
   
     This program is free software; you can redistribute it and/or modify
     it under the terms of the GNU General Public License, version 2, as
     published by the Free Software Foundation.
   
     This program is distributed in the hope that it will be useful,
     but WITHOUT ANY WARRANTY; without even the implied warranty of
     MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
     GNU General Public License for more details.
   
     You should have received a copy of the GNU General Public License
     along with this program; if not, write to the Free Software
     Foundation, Inc., 51 Franklin St, Fifth Floor, Boston, MA  02110-1301  USA
    */
    ?>
   
   
**Plugin Files**

If you are creating a plugin Named **Test Plugin**, Then plugin file structure should be like below list
   
   - TestPlugin
      - TestPlugin.ctrl.php
      - css
      - js
      - images
      - views
	      - menu.ctp
      - conf.php
      - plugin.xml
      - database.sql
      - upgrade.sql
  
      
   **i) TestPlugin**

   First step is to create a folder named **"TestPlugin"**,  which contains all plugin files and folders. The plugin directory name should not contain spaces and other special characters.
   
   
   **ii) TestPlugin.ctrl.php**
   
   Next step is to create a controller class file with the same name as plugin directory and with an extension **".ctrl.php"** The controller class file will extends the Seo Panel plugin class. 
   
   **Syntax:**
   
   .. code-block:: php
   
	<?php
	class TestPlugin extends SeoPluginsController{
	
		function index() {
			$this->set('sectionHead', "Test Plugin Index Section");
			$this->pluginRender('index');
		}
		
	}
	?>

   
   **$this->set("sectionHead", "Test Plugin Index section")** - This function will set data  to view helpers and  in above code it will set the "Test Plugin Index Section" to "sectionHead" variable  and it can be accessed in template as "$sectionHead".

   **$this->pluginRender('index')** - This function will  call template file to output the data processed in plugin controller functions. This code will display the template file "index.ctp" in the folder "views". In this file we can  access all values set from controller functions.
   

   **iii) views**

   Create a “views” folder to add all template files required by plugin to show the HTML output.

   **menu.ctp**
   After creating a "views" folder next step is to create a “menu.ctp” file inside the folder “views”. This file will display the left menu for a plugin and using that different features of plugin is accessed by user.

   **Syntax:**

   .. code-block:: php
   		
	<ul id='subui'>
		<li>
			<a href="javascript:void(0);" onclick="<?php echo pluginMenu('action=index');?>">Test Plugin</a>
		</li>
		<?php if(isAdmin()){?>
			<li>
				<a href="javascript:void(0);" onclick="<?php echo pluginMenu('action=settings');?>">Settings</a>
			</li>
		<?php }?>
	</ul>
   		
   The above code will show two menu items under plugin "TestPlugin"  in "Seo Plugins" page of Seo Panel.

   **isAdmin()** - This function is used to find whether logged in user is admin and then restrict some menu items to only for Seo Panel admin.

   **pluginMenu('action=settings'), pluginMenu('action=index')** - This function will create an ajax function for "onClick" event and while click on this menu link it will call “settings” and “index” functions of “TestPlugin.ctrl.php” respectively.

   All templates files are created inside “ views” folder with “.ctp.php” extension.    
   
   
   Sample **"index.ctp.php"**
   
   .. code-block:: php

	<?php echo showSectionHead($sectionHead); ?>
	<form id='search_form'>
	<table width="45%" border="0" cellspacing="0" cellpadding="0" class="search">
		<tr>
			<th>Test Plugin Type: </th>
			<td>
				<select name="tp_type">
					<option value="1">active</option>
					<option value="0">inactive</option>
				</select>
			</td>
			<td align='left'>
				<a onclick="<?php echo pluginPOSTMethod('search_form', 'subcontent', 'action=show'); ?>" href="javascript:void(0);">
					<img border="0" alt="" src="<?=SP_IMGPATH?>/show_records.gif"/>
				</a>
			</td>
		</tr>
	</table>
	</form>
	<div id='subcontent'>
		<p class='note'>Click Show Records to <b class="testplugin">Show</b> Test Plugin Records.</p>
	</div>

   **showSectionHead** - This function will display the header text for a page

   **pluginPOSTMethod('search_form', 'subcontent', 'action=show')** - This function will create an AJAX POST method for “onClick” event and it will post the elements in the HTML form  “search_form” with extra arguments  'action=show'. The result will be updated in  the div with id “subcontent”.

   There are lots of useful functions are available in Seo Panel and explained under section the “Common Functions” .
   
   
   **iv) conf.php**

   This file is used to include common constants used in plugin functions.

   **Eg:**
   
   .. code-block:: php
   
	// contant used to get the name of test head section
	define('TEST_HEAD', 'Seo Panel Test Plugin');

   This "TEST_HEAD" constant can be used in any part of the plugin code.

   **v) css**

   The folder contains all css files required by plugin. The plugin **automatically include** it in seo panel and will help you to customise plugin interface.


   **vi) js**

   The folder contains all javascript files required by plugin. The plugin **automatically include** it in seo panel and will help you to create new javascript functions for plugin.


   **vii) images**

   This folder contains all images required for a plugin. The images can be accessed in templates using the constant “PLUGIN_IMGPATH”.

   **Eg:**
   
   .. code-block:: php
   
   	<img src="<?=PLUGIN_IMGPATH?>/star.gif">


   **viii) database.sql**

   This file contains the MYSQL dump of all database tables and data required to install plugin in to Seo Panel. This file is imported to Seo Panel database during the time of installation of plugin.


   **ix) upgrade.sql**

   This file contains the MYSQL dump of all database tables and data required to upgrade intstalled plugin in Seo Panel. This file is imported to Seo Panel database during the time of upgradation of plugin.


   **x) plugin.xml**

   This XML file is used to add the details about the plugin. Please check below sample “plugin.xml” file.

   **Eg:**
   
   .. code-block:: xml
   
	<?xml version="1.0" encoding="UTF-8"?>
	<plugin>
	       <author>Geo Varghese</author>
	       <label>Test Plugin</label>
	       <description>Seo Panel Test Plugin: Check the structure of test plugin and it will help you to create new Seo Panel Plugins.</description>
	       <version>1.0.0</version>
	       <website>http://www.seopanel.in/plugins/</website>
	</plugin>
	

   **author** - The name of the person who created plugin

   **label** - The name of the plugin

   **description** - The description of the plugin

   **version** - The current version of the plugin

   **website** - A link to a website where user can download plugin.

   Once you are familiar with these files and functions, it really easy to create plugins for seo Panel.
