3. API
======================

The Seo Panel API provides an interface to allow you to access and perform actions 
in Seo Panel both from external applications and scripts as well as internal modules and addons.

The Seo Panel API supports response type: JSON

1. API Setup
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Login as admin and go to following page

Admin Panel => API Manager => API Settings

Change values of API Key and Secret for security according to the below screen shot. 

.. image:: _static/sp_api_settings.png


2. Functions
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The API currently supports the following functions


Website Management
------------------

**Common Attributes**

	- SP_API_KEY => Seo panel api key
	- API_SECRET => Seo panel api secret key 
	- category" = website


Add Website
************************

**Purpose**

This command is used to add a new website in seo panel.

**Attributes**

	- action 	= createWebsite
	- name 		=> The name of the website
	- url 		=> The url of the website
	- user_id 	=> The user id of website

**Optional Attributes**

	- title 		=> The title of the website
	- description 	=> The description of website
	- keywords 		=> The keywords of the website
	- status 		=> The status of the website - default[1]

**Example Command**

.. code-block:: php
	
	$paramList['SP_API_KEY'] = "*******";
	$paramList['API_SECRET'] = "*******";
	$paramList['category'] = "website";
	$paramList['action'] = "createWebsite";
	$paramList['name'] = "test.com";
	$paramList['user_id'] = "1";
	$paramList['url'] = "http://test.com/";

**Successful Response**

	- response = success
	- result = Successfully created website
	- website_id = The id of the website

**Error Response**

	- response = Error
	- error_msg = * Website already exist

Update Website
************************

**Purpose**

This command is used to update existing website in seo panel.

**Attributes**

	- action = updateWebsite
	- id => The id of the website			

**Optional Attributes**
	
	- name 			=> The name of the website
	- url 			=> The url of the website
	- user_id 		=> The user id of website
	- title 		=> The title of the website
	- description 	=> The description of website
	- keywords 		=> The keywords of the website
	- status 		=> The status of the website - default[1]

**Example Command**

.. code-block:: php
	
	$paramList['SP_API_KEY'] = "*******";
	$paramList['API_SECRET'] = "*******";
	$paramList['category'] = "website";
	$paramList['action'] = "updateWebsite";
	$paramList['id'] = 1;
	$paramList['name'] = "Test Website";

**Successful Response**

	- response = success
	- result = Successfully updated website

**Error Response**

	- response = Error
	- error_msg = The invalid website id provided


Delete Website
************************

**Purpose**

This command is used to delete existing website in seo panel.

**Attributes**

	- action = deleteWebsite
	- id => The id of the website			

**Optional Attributes**
	
	
**Example Command**

.. code-block:: php
	
	$paramList['SP_API_KEY'] = "*******";
	$paramList['API_SECRET'] = "*******";
	$paramList['category'] = "website";
	$paramList['action'] = "deleteWebsite";
	$paramList['id'] = 1;

**Successful Response**

	- response = success
	- result = Successfully deleted website and related data

**Error Response**

	- response = Error
	- error_msg = The invalid website id provided



Get Website Details
********************

**Purpose**

This command is used to get details of a website

**Attributes**

	- action = getWebsiteInfo
	- id => The id of the website			

**Optional Attributes**
	
	
**Example Command**

.. code-block:: php
	
	$paramList['SP_API_KEY'] = "*******";
	$paramList['API_SECRET'] = "*******";
	$paramList['category'] = "website";
	$paramList['action'] = "getWebsiteInfo";
	$paramList['id'] = 1;

**Successful Response**

.. code-block:: php

	[response] => success
	[result] => stdClass Object(
	        [id] => website id
	        [name] => website name
	        [url] => website url
	        [owner_name] => owner name
	        [owner_email] => owner email
	        [category] => website category
	        [title] => website title
	        [description] => website description
	        [keywords] => website keywords
	        [title2] => website title2 for directory submission
	        [title3] => website title3 for directory submission
	        [title4] => website title4 for directory submission
	        [title5] => website title5 for directory submission
	        [description2] => website description2 for directory submission
	        [description3] => website description3 for directory submission
	        [description4] => website description4 for directory submission
	        [description5] => website description5 for directory submission
	        [reciprocal_url] => reciprocal url for directory submission
	        [user_id] => user id
	        [status] => website status
	)
    
**Error Response**

	- response = Error
	- error_msg = The invalid website id provided


Get Website Reports
************************

Get User Website Reports
************************



Keyword Management
------------------





Get Keyword Reports
************************

**Purpose**

**Attributes**

**Optional Attributes**

**Example Command**

**Successful Response**

**Error Response**

Get Website Keyword Reports
***************************

**Purpose**

**Attributes**

**Optional Attributes**

**Example Command**

**Successful Response**

**Error Response**

Get User Keyword Reports
************************

**Purpose**

**Attributes**

**Optional Attributes**

**Example Command**

**Successful Response**

**Error Response**


User Management
------------------

Add User
************************

**Purpose**

**Attributes**

**Optional Attributes**

**Example Command**

**Successful Response**

**Error Response**

Update User
************************

**Purpose**

**Attributes**

**Optional Attributes**

**Example Command**

**Successful Response**

**Error Response**


Delete User
************************

**Purpose**

**Attributes**

**Optional Attributes**

**Example Command**

**Successful Response**

**Error Response**

