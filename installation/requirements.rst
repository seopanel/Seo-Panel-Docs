.. title:: SEO Panel System Requirements | PHP, MySQL & Server Specifications

.. meta::
   :description: SEO Panel requires PHP 7.4 or higher, MySQL 5.7+ or MariaDB 10.3+, Apache or Nginx web server, and CURL, mysqli and mbstring PHP extensions.

System Requirements
===================

.. raw:: html

   <div style="background: linear-gradient(135deg, #1a6b3c 0%, #2d9e5f 50%, #34a85a 100%); border-radius: 10px; padding: 14px 20px; margin: 16px 0 28px 0; display: flex; align-items: center; justify-content: space-between; flex-wrap: wrap; gap: 12px; box-shadow: 0 4px 14px rgba(26,107,60,0.35);">
     <div style="display: flex; align-items: center; gap: 14px;">
       <div style="background: rgba(255,255,255,0.15); border-radius: 8px; width: 42px; height: 42px; display: flex; align-items: center; justify-content: center; flex-shrink: 0;">
         <i class="fa fa-download" style="color: #fff; font-size: 20px;"></i>
       </div>
       <div>
         <div style="display: flex; align-items: center; gap: 8px; margin-bottom: 3px;">
           <span style="color: #fff; font-size: 15px; font-weight: 700; line-height: 1;">SEO Panel</span>
           <span style="background: rgba(255,255,255,0.2); color: #fff; font-size: 11px; font-weight: 600; padding: 2px 8px; border-radius: 20px; line-height: 1.5;">Latest</span>
           <span style="background: rgba(255,255,255,0.15); color: #fff; font-size: 11px; font-weight: 600; padding: 2px 8px; border-radius: 20px; line-height: 1.5;">Free</span>
         </div>
         <div style="color: rgba(255,255,255,0.85); font-size: 12px; line-height: 1.4;">Download the latest stable release and get started in minutes.</div>
       </div>
     </div>
     <a href="https://www.seopanel.org/download/" target="_blank"
        style="display: inline-flex; align-items: center; gap: 8px; background: #fff; color: #1a6b3c; padding: 9px 20px; border-radius: 7px; font-weight: 700; font-size: 14px; text-decoration: none; box-shadow: 0 2px 8px rgba(0,0,0,0.18); white-space: nowrap;"
        onmouseover="this.style.opacity='.88'" onmouseout="this.style.opacity='1'">
       <i class="fa fa-download"></i> Download
     </a>
   </div>

1. **PHP** version *>= 7.4* (PHP 8.0, 8.1, 8.2, 8.3 supported)

   - Recommended: PHP 8.1 or higher for better performance and security

2. **Database Support**

   - MySQL *>= 5.7* or MariaDB *>= 10.3*
   - MySQL 8.0+ or MariaDB 10.5+ recommended

3. **PHP Extensions Required**

   - **CURL** - For making HTTP requests, Ref: http://php.net/manual/en/curl.setup.php
   - **mysqli** or **PDO MySQL** - For database connectivity
   - **JSON** - For data processing (usually enabled by default)
   - **mbstring** - For multibyte string handling
   - **OpenSSL** - For secure connections

4. **Web Server**

   - Apache 2.4+ with mod_rewrite enabled (recommended)
   - Nginx 1.18+ with proper PHP-FPM configuration
   - Any web server with PHP support

5. **File Permissions**

   - Write permissions for tmp/ directory
   - Write permissions for config/ directory during installation

6. **Recommended Server Specs**

   - Memory: Minimum 256MB, Recommended 512MB or higher
   - Disk Space: Minimum 100MB for application files
   - PHP memory_limit: 128MB or higher
   - PHP max_execution_time: 300 seconds or higher for large operations

