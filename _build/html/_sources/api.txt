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

Add Website
************************

**Purpose**

This command is used to add a new website in seo panel.

**Attributes**
	- name => The name of the website
	- url => The url of the website
	- user_id => The user id of website

**Optional Attributes**

	- title => The title of the website
	- description => The description of website
	- keywords => The keyword of the website
	- status => The status of the website - default[1]

**Example Command**

 $postfields["action"] = "createWebsite";

**Successful Response**

result = success
message =  xxx - returned on error
clientid = returned ID of newly added Client

**Error Response**

result=error&message=




Update Website
************************

**Purpose**

**Attributes**

**Optional Attributes**

**Example Command**

**Successful Response**

**Error Response**


Delete Website
************************


**Purpose**

**Attributes**

**Optional Attributes**

**Example Command**

**Successful Response**

**Error Response**


Get Website Details
************************


**Purpose**

**Attributes**

**Optional Attributes**

**Example Command**

**Successful Response**

**Error Response**


Get Website Reports
************************


**Purpose**

**Attributes**

**Optional Attributes**

**Example Command**

**Successful Response**

**Error Response**


Get User Website Reports
************************

**Purpose**

**Attributes**

**Optional Attributes**

**Example Command**

**Successful Response**

**Error Response**


Keyword Management
------------------

Add Keyword
************************


**Purpose**

**Attributes**

**Optional Attributes**

**Example Command**

**Successful Response**

**Error Response**


Update Keyword
************************

**Purpose**

**Attributes**

**Optional Attributes**

**Example Command**

**Successful Response**

**Error Response**

Delete Keyword
************************

**Purpose**

**Attributes**

**Optional Attributes**

**Example Command**

**Successful Response**

**Error Response**

Get Keyword Details
************************

**Purpose**

**Attributes**

**Optional Attributes**

**Example Command**

**Successful Response**

**Error Response**

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

