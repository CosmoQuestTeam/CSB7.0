# CSB7.0
An open source implementation of CosmoQuest's Citizen Science Builder software. 

### Step 1: Setup the Server
#### 1.1 Setup LAMP Server

Setup an Apache 2 / MySQL 8 / PHP 7 environment. If we don't have specific instructions you need below, look for 
instructions for Wordpress. Our setup should be the same.

* OSX 
    * Enable Apache `apachectl start`
    * In `/etc/apache2/httpd.conf`
        * Uncomment `LoadModule` statements for php7 and mod_rewrite _Use Legacy Password Encryption_
        * Set `AllowOverride All`
    * Restart Apache `sudo apachectl restart`
    * [Install MySQL](https://dev.mysql.com/downloads/mysql) 
    * Add mysql to your `.bash_profile` by adding `export PATH="/usr/local/mysql/bin:$PATH"`
- Ubuntu: find the Digital Ocean Tutorial for your version of Ubuntu
- Windows: _to be determined_

If you don't have a LAMP (or Win AMP) setup, find instructions to install 
Wordpress. This software requires the same kind of server configuration! 
For ubuntu, the Digital Ocean tutorials are among the best.


#### 1.2 Add SASS support 
To install SASS, follow instructions on sass-lang.com/install. Once things
are installed, you'll need to compile your sass files into css files whenever
the sass is edited. 

PHPstorm can watch and compile sass (see https://www.jetbrains.com/help/phpstorm/transpiling-sass-less-and-scss-to-css.html).

Instructions on compiling SASS in ubuntu are here: https://webdesign.tutsplus.com/tutorials/watch-and-compile-sass-in-five-quick-steps--cms-28275

#### 1.3 If you can, add a security certificate
You should always use a certificate. If you don't have one, try using the free 
[Let's Encrypt: CertBot](https://letsencrypt.org/getting-started/).

####Step 2: Copy csb-settings-example.php csb-settings.php and edit the file to match your systems settings

####Step 3: Go to http://yourdir/csb-installer/installer.php in your browser. 
  This will install databases and setup an admin user using the settings in csb-settings.php