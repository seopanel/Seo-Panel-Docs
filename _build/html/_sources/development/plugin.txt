Plugin Development Guide
~~~~~~~~~~~~~~~~~~~~~~~~

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

   Create a "views" folder to add all template files required by plugin to show the HTML output.

   **menu.ctp**
   After creating a "views" folder next step is to create a "menu.ctp" file inside the folder "views". This file will display the left menu for a plugin and using that different features of plugin is accessed by user.

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

   **pluginMenu('action=settings'), pluginMenu('action=index')** - This function will create an ajax function for "onClick" event and while click on this menu link it will call "settings" and "index" functions of "TestPlugin.ctrl.php" respectively.

   All templates files are created inside " views" folder with ".ctp.php" extension.    
   
   
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

   **pluginPOSTMethod('search_form', 'subcontent', 'action=show')** - This function will create an AJAX POST method for "onClick" event and it will post the elements in the HTML form  "search_form" with extra arguments  'action=show'. The result will be updated in  the div with id "subcontent".

   There are lots of useful functions are available in Seo Panel and explained under section the "Common Functions" .
   
   
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

   This folder contains all images required for a plugin. The images can be accessed in templates using the constant "PLUGIN_IMGPATH".

   **Eg:**
   
   .. code-block:: php
   
   	<img src="<?=PLUGIN_IMGPATH?>/star.gif">


   **viii) database.sql**

   This file contains the MYSQL dump of all database tables and data required to install plugin in to Seo Panel. This file is imported to Seo Panel database during the time of installation of plugin.


   **ix) upgrade.sql**

   This file contains the MYSQL dump of all database tables and data required to upgrade intstalled plugin in Seo Panel. This file is imported to Seo Panel database during the time of upgradation of plugin.


   **x) plugin.xml**

   This XML file is used to add the details about the plugin. Please check below sample "plugin.xml" file.

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
   
   
~~~~~~~~~~~~~~~~~~~~~~~
Common Plugin Functions
~~~~~~~~~~~~~~~~~~~~~~~

The common plugin functions available to create seo panel plugins are

---------------------------------------------
1) pluginGETMethod($args='', $area='content')
---------------------------------------------

Function to create an plugin ajax GET method using automatically created plugin url according to corresponding plugin.

**$args**
The arguments to be send with ajax GET request

**Eg**:: 

   "&id=2&col=refid"

**$area**
The area(div id) to be updated with result of ajax request.
The default value is "content", the content div  will be updated with result of ajax request.

**Return**
Returns ajax GET request function call and can be used in javascript trigger events like "onClick"

**Eg**::

   <a href="javascript:void(0);' onclick="<?php echo pluginGETMethod('action=settings', 'content'); ?>">Click</a>

It will create a code like below according to plugin::

   <a href="javascript:void(0);" onclick="scriptDoLoad('seo-plugins.php?pid=18', 'content', 'action=settings')">Click</a>

while click on above link the method "settings" of plugin id 18 is called and result after the execution of request will be updated in the div "content".

---------------------------------------------------------
2) pluginPOSTMethod($formName, $area='content', $args='')
---------------------------------------------------------

Function to create an plugin ajax POST method to post elements of particular form to plugin method.

**$formName**
The name of the form element should be submitted


**$area**
The area(div id) to be updated with result of ajax request.
The default value is "content", the content div  will be updated with result of ajax request.

**$args**
Using this we can pass extra arguments with form submission.

**Eg**::

   "&action=submitmsg&val=1"

**Return**
Returns ajax POST request function call and can be used in javascript trigger events like "onClick"

**Eg**::
   
   <a href="javascript:void(0);" onclick="<?php echo pluginPOSTMethod('projectform', 'content', 'action=createproject'); ?>" >Click</a>

It will create a code like below according to plugin::

   <a href="javascript:void(0);" onclick="scriptDoLoadPost('seo-plugins.php', 'projectform', 'content', '&pid=18&action=createproject')">

While click on above link, it will submit elements of form with name "projectform" to the method "createproject" of plugin id 18 and result after the execution of request will be updated in the div "content".

----------------------------------------------------
3) pluginConfirmGETMethod($args='', $area='content')
----------------------------------------------------

Same as **"pluginGETMethod"** but before execution of request a confirm box is displayed to confirm the user to allow action. Used while delete a project,user etc.

----------------------------------------------------------------
4) pluginConfirmPOSTMethod($formName, $area='content', $args='')
----------------------------------------------------------------

Same as **"pluginPOSTMethod"** but before execution of request a confirm box is displayed to confirm the user to allow action. Used while edit,update project,user etc.

----------------------------------------
5) pluginMenu($args='', $area='content')
----------------------------------------

Same as **"pluginGETMethod"**  and used to create plugin left submenus while loading a plugin first.


**Eg**::

   <li><a href="javascript:void(0);" onclick="<?php echo pluginMenu('action=viewreports'); ?>">Reports Manager</a></li>

~~~~~~~~~~~~~~~~
Plugin Constants
~~~~~~~~~~~~~~~~

--------------
1) PLUGIN_PATH
--------------


The absolute path to plugin directory

**Eg**::

   /opt/lampp/htdocs/seopanel/plugins/TestPlugin

------------------
2) PLUGIN_VIEWPATH
------------------

The absolute path to plugin  views folder

**Eg**:: 

   /opt/lampp/htdocs/seopanel/plugins/TestPlugin/views

------------
3) PLUGIN_ID
------------

The id of the plugin, can used to create plugin specific urls

-----------------
4) PLUGIN_WEBPATH
-----------------

The web path to directory of a plugin.

**Eg**::

   http://localhost/seopanel/plugins/TestPlugin

-----------------
5) PLUGIN_IMGPATH
-----------------

The web path to plugin image directory

**Eg**::

   http://localhost/seopanel/plugins/TestPlugin/images/

-----------------
6) PLUGIN_CSSPATH
-----------------

The web path to plugin css directory

**Eg**::
   
   http://localhost/seopanel/plugins/TestPlugin/css

----------------
7) PLUGIN_JSPATH
----------------

The web path to plugin javascript directory

**Eg**::

   http://localhost/seopanel/plugins/TestPlugin/js

--------------------
8) PLUGIN_SCRIPT_URL
--------------------

The web url to access a specific plugin

**Eg**:: 
   
   http://localhost/seopanel/seo-plugins.php?pid=18
 
  
~~~~~~~~~~~~~~~~~~~~~~~~~
Common Database Functions
~~~~~~~~~~~~~~~~~~~~~~~~~

Inside a plugin functions database object can be accessed by **$this->db**

**Eg:**

.. code-block:: php

   <?php
   $sql = "Select * from projects";
   projectList = $this->db->select($sql);

The above code will assign the projects list  as an array to variable $projectList

The important functions can be used for database operation are

--------------------------------------
1) select($query, $fetchFirst = false)
--------------------------------------

This function is used for database select statement and will return the database table rows as an array.

**$query**
The sql select query to be executed to get the results.

**$fetchFirst**
*true* - Will return only first row of the results
*false* - Will return all rows and default value is "false"

**Return**
The array contains the result list. Returns empty  array if query fails or when empty rows retrieved. The return array can be accessed like below example

**Eg**

.. code-block:: php

   <?php
   $sql = "select * from projects";        
   $projectList = $this->db->select($sql);
   foreach ($projectList as $i => $prInfo) {
      echo $prInfo['id'];
   }
   
   $sql = "select * from projects";
   $prInfo = $this->db->select($sql, true);
   echo $prInfo['id'];


-------------------------------
2) query($query, $noRows=false)
-------------------------------

This function is used to execute the sql query like update,delete etc

**$query**
The sql query to be executed.

**$noRows**
true - It will set number of database entries affected by execution of query in the variable $this->db->noRows
false - will not set number of database entries affected, default value is "false"

**Return**
Return the result of the execution like the return variable of php mysql query function

~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Session Management Functions
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The common session management functions are

------------------
1) checkLoggedIn()
------------------

Function to check whether user logged in to the seo panel or not. If not logged in, current page will be redirected to login page.

-----------------------
2) checkAdminLoggedIn()
-----------------------

Function to check whether admin logged in to the seo panel or not. If not logged in, current page will be redirected to login page.

---------------
3) isLoggedIn()
---------------

Function to get logged in user’s id in seo panel.

**Return:**
If user logged in, "user id" will be returned.
If user not logged in, false will be returned.

------------
4) isAdmin()
------------

Function to get logged in admin’s id in seo panel.

**Return:**
If admin logged in, "admin id" will be returned.
If admin not logged in, false will be returned.