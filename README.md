OpenSSL DLLs for PHP 7.0.27 with FIPS Compliant

# Prerequisite:
-------------
1. PHP 7.0.27 version or 7.0.X

# Setup OpenSSL FIPS Complaint Extension in PHP:
----------------------------------------------
1. Open PHP directory where you have installed, or may find the path where you have located php.exe and php.ini
2. Copy and past below 2 files inside PHP main directory:
  - libeay32.dll
  - sslaey32.dll
3. Copy php/ext/php_openssl.dll file from extracted directory to inside your php/ext/ directory
4. Update your php.ini file to enable openssl extension by removing ; from line start
 
   extension=php_openssl.dll

5. Restart IIS Server
6. If you would like to test openssl fips enabled extension, you may test by executing following lines:

<?php

openssl_fips_init(); 
echo openssl_fips_enabled();

?>

Cheers !
