.. title:: SEO Panel My Account | Profile, 2FA, Alerts & Connections

.. meta::
   :description: Guide for SEO Panel My Account - edit your profile, enable two-factor authentication, read in-app alerts, and manage Google/MCP connections.


My Account
~~~~~~~~~~

Go to **Admin Panel => My Account** for every page on this one - **My Profile**, **Connections**, **Alerts** and **MCP Access** - all reached from the same left-menu group.

~~~~~~~~~~
My Profile
~~~~~~~~~~

Your own account details, and the jumping-off point for editing them or turning on two-factor authentication.

1) Go to **Admin Panel => My Account => My Profile**

   .. image:: ../_static/sp_my_profile.png

   - Shows your **First Name**, **User Type**, **Username**, **Email**, and (for non-admin accounts on a plan) **Keyword Limit**, **Website Limit** and **Expiry Date**
   - **Edit My Profile** - change your username, first/last name or email, or set a new password (your **current password** is required to change the password - a hijacked or left-open session alone isn't enough)
   - **Two-Factor Authentication** - see below

~~~~~~~~~~~~~~~~~~~~~~~~~~
Two-Factor Authentication
~~~~~~~~~~~~~~~~~~~~~~~~~~

Protect your own login with a TOTP authenticator app (Google Authenticator, Authy, 1Password, etc.), on top of your password.

1) Go to **Admin Panel => My Account => My Profile => Two-Factor Authentication**

   .. image:: ../_static/sp_two_factor_setup.png

   - Add the **Secret key** to your authenticator app manually, or follow the **Setup link** - some apps/password managers can import directly from it
   - Enter the 6-digit code your app shows and click **Confirm and enable**
   - You're then shown a set of one-time-use **backup codes** - save them somewhere safe, they're shown only once and let you log in if you lose your authenticator device
   - Once enabled, you can **Regenerate backup codes** (invalidates the old set) or **Disable** two-factor authentication (requires your current password either way)
   - With two-factor enabled, logging in asks for the 6-digit code (or a backup code) as a second step after your password

~~~~~~~~
Alerts
~~~~~~~~

Your own in-app notification inbox - a new Seo Panel version being available, Seo Panel API connection/verification problems, and report-related warnings land here.

1) Go to **Admin Panel => My Account => Alerts**

   .. image:: ../_static/sp_alerts_list.png

   - Filter by **Search** text, **Category** or date **Period**
   - Click any row's **Id** to read its full message
   - **Delete** a single alert from its row's Action dropdown, or every listed alert at once with the bottom **Delete** button

~~~~~~~~~~~
Connections
~~~~~~~~~~~

.. include:: google_connection.rst

~~~~~~~~~~~~~~
MCP Access
~~~~~~~~~~~~~~

Generate a personal access token for your own AI agent to query your Seo Panel data directly - see :doc:`mcp_access` for the full guide. Reached from here as **Admin Panel => My Account => MCP Access**, and also linked from the AI Visibility Summary page.

   .. image:: ../_static/sp_mcp_access_profile.png
