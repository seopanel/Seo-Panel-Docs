System Requirements
===================

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

