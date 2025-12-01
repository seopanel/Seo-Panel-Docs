.. title:: Seo Panel Theme Development Guide with Steps to Create a Seo Panel Theme

.. meta::
   :description: Guide for Seo panel developers to create new theme for seo panel. Functions and features are explained with code samples and test theme.


Theme Development Guide
~~~~~~~~~~~~~~~~~~~~~~~

~~~~~~~~~~~~
Introduction
~~~~~~~~~~~~

Seo Panel Themes help us to **modify, customize, and extend** the features of Seo Panel interface according to our requirement. 
 
If you would like to create a new Seo Panel theme, then first search the theme in Seo Panel theme repository - https://www.seopanel.org/themes/
If it is not existing any where, then use following articles to create a new theme for Seo Panel and publish it through Seo Panel repository. 

**Note:** This article assumes you are already familiar with the basic functionality of Seo Panel, and PHP, HTML, CSS, JS programming.


~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Steps to Create a Seo Panel Theme
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

This section guide us through the steps needs to follow while creating a new Seo Panel theme.

--------------------------- 
Names, Files, and Locations
---------------------------


**Theme Name**
 
The first step for theme creation is finding a name for your theme according to the features you would like to implement with it.

**Eg:** "Test Theme"

Once you found a name for your theme, then search it in `Seo Panel theme repository <https://www.seopanel.org/themes>`_ to find any other theme existing with the same name. If it is already existing, then choose another name for your theme.
   
   
**Theme Files**

If you are creating a theme Named **Test Theme**, Then theme file structure should be like below list
   
   - TestTheme
      - css
      - js
      - images
      - views
      - theme.xml  
      
   **i) TestTheme**

   First step is to create a folder named **"TestTheme"**,  which contains all theme files and folders. The theme directory name should not contain spaces and other special characters.
   
   **ii) views**

   Create a "views" folder to add all template files required by theme to show the HTML output.

   **iii) css**

   The folder contains all css files required by theme.


   **iv) js**

   The folder contains all javascript files required by theme.


   **v) images**

   This folder contains all images required for a theme.


   **vi) theme.xml**

   This XML file is used to add the details about the theme. Please check below sample "theme.xml" file.

   **Eg:**
   
   .. code-block:: xml
   
      <?xml version="1.0" encoding="UTF-8"?>
      <theme>
         <author>Geo Varghese</author>
         <name>Classic</name>
         <description>Classic theme of Seo Panel</description>
         <version>1.0.0</version>
         <website>https://www.seopanel.org/theme/l/1/classic/</website>   
      </theme>	

   **author** - The name of the person who created theme

   **name** - The name of the theme

   **description** - The description of the theme

   **version** - The current version of the theme

   **website** - A link to a website where user can download theme.

   Once you are familiar with these files and functions, it really easy to create themes for seo Panel.

   