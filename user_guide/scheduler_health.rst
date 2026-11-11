.. title:: Scheduler Health - monitor cron runs and run Seo Panel without a system cron job

.. meta::
   :description: Guide for Seo Panel's Scheduler Health dashboard (new in 7.0.0) - monitor background cron runs, the resumable job queue, and the zero-setup ping/beacon trigger for hosts where you can't set up a real system cron job.


Scheduler Health
~~~~~~~~~~~~~~~~

~~~~~~~~~~~~~~
Overview
~~~~~~~~~~~~~~

Every scheduled crawl in Seo Panel - rank checking, backlinks, site auditor, and the rest - runs out of ``cron.php``, normally fired by a system cron job once a day. **Scheduler Health**, new in 7.0.0, is a live dashboard for that whole background system, plus a **zero-setup ping/beacon trigger** for hosts where you can't add a real cron job at all (shared hosting, for example).

1) Go to **Reports => Scheduler Health** (admin-only)


~~~~~~~~~~~~~~
Run history and job queue
~~~~~~~~~~~~~~

1) The banner at the top shows whether a run is **currently in progress**, or the status, trigger source, duration and websites processed of the **last completed run**

   .. image:: ../_static/sp_scheduler_health.png

   - **Recent runs** lists the run history; **Per-tool activity (last 7 days)** breaks success/failure/average duration down by tool
   - **Resumable job queue** processes each tool in small, resumable steps instead of one long-running pass, so an interrupted run picks back up instead of restarting from scratch. Fresh installs have this on by default; an install upgraded from an older version may still have it off, with no downside to turning it on
   - With the job queue on, **Job queue backlog** and **Recently failed chunks** show pending/failed work directly below


~~~~~~~~~~~~~~
External ping trigger
~~~~~~~~~~~~~~

For a host where you can't set up ``cron.php`` as a real system cron job, point an external cron/uptime service - or your own crontab, if you have one anywhere - at a URL that triggers a short, budget-limited cron run instead.

1) Tick **Enable ping trigger**, set a **Budget (seconds)** - how long a single triggered run is allowed to take, 5 to 60 seconds - and click **Save**

2) Click **Generate new secret**, then copy the ping URL shown (the secret is appended as ``?key=...``)

   - The secret identifies and authorizes the caller - anyone with this URL can trigger a cron run, so treat it like a password
   - The endpoint always responds with no output (HTTP 204), and rejects any request with a missing or wrong key with no logging and no state change
   - Regenerating the secret immediately invalidates the old URL - update wherever you pasted it

Independently of the external trigger, a logged-in admin viewing any admin page also opportunistically fires the same budget-limited run in the background (throttled to once every 5 minutes), so an install that's simply being administered day to day gets some scheduling coverage even with no external pinger configured at all. Both paths show up in **Recent runs** above, tellable apart by their **Trigger** column (``ping`` for the external URL, ``ping-beacon`` for the opportunistic admin-page trigger).
