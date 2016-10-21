Plugin Dvelopment Guide
~~~~~~~~~~~~~~~~~~~~~~~

~~~~~~~~~~~~
Introduction
~~~~~~~~~~~~

Seo Panel Plugins help us to modify, customize, and extend the features of Seo Panel according to our requirement. Instead of changing the core programming of Seo Panel, you can add extra functionality to Seo Panel with Seo Panel Plugins.
 
Seo Panel Plugin: A Seo Panel Plugin is a independant program with a set of extra features, written in the PHP scripting language, that adds a specific set of features or services to the Seo Panel.
 
If you would like to create a new Seo Panel plugin, then first search the plugin in Seo Panel plugin repository - http://www.seopanel.in/plugins/
If it is not existing any where, then use following articles to create a new plugin for Seo Panel and publish it through Seo Panel repository. 

Note: This article assumes you are already familiar with the basic functionality of Seo Panel, and PHP programming.


~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Steps to Create a Seo Panel Plugin
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

This section guide us through the steps needs to follow while creating a  new Seo Panel plugin.

--------------------------- 
Names, Files, and Locations
---------------------------

 
**Plugin Name**
 
 
The first step for plugin creation is finding a name for your plugin according to the features you would like to implement with it.

Eg: The name for a search engine submission plugin can be named like "Search Engine Submitter"

Once you found a name for your plugin, then search it in `Seo Panel plugin repository <http://www.seopanel.in/plugins>`_ to find any other plugin existing with the same name. If it is already existing, then choose another name or create plugin for another feature.


**License**


It is customary to follow the standard header with information about licensing for the Plugin. Most Plugins use the GPL2 license used by Seo Panel  or a license compatible with the GPL2. To indicate a GPL2 license, include the following lines in all files of your Plugin:

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

If you are creating a plugin Named "Test Plugin", Then plugin file structure should be like below list
   
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

   First step is to create a folder named “TestPlugin”,  which contains all plugin files and folders. The plugin directory name should not contain spaces and other special characters.
   
   
   