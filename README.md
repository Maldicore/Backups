Backup and Restore Plugin for CakePHP
=====================================
Version 1.0 for cake 2.x

This backup and restore plugin enables developers to quickly and easily backup and restore both database schema and data based on backup dates.

As an application is developed, changes to the database may be required, and managing that in teams can get extremely difficult. Backup and restore enables you to share and co-ordinate database changes as well as data in an iterative manner, removing the complexity of handling these changes. We have used backup and restore in a production environment for multiple backups and rolling them out for fast deployment.

Installation
=============

* Unzip or clone this plugin into your app/Plugin/Backups folder or the shared plugins folder for your CakePHP installation.
* Add the plugin to your app/Config/bootstrap.php using CakePlugin::load('Backups')

Usage
======

Backups
-------
* In your cakePHP application root folder (in a terminal) execute

<pre>
	./app/Console/cake Backups.backup
</pre>

It will backup all the tables in the database and zip (if ZipArchive exits!)
the backup files are stored in ./app/Backups

Restoring
----------
* In your cakePHP application root folder (in a terminal) execute

<pre>
	./app/Console/cake Backups.backup restore
</pre>

It will prompt you all available backup versions with date and time, just type a corresponding version (eg: 0) and hit enter

Troubleshooting
----------------
* In case of any errors that is not predicted in the script you can always (manually) restore from one of the backup.

Notes
------
* The database user (in cakephp database config) must have rights to drop tables for restore to work! As the restore process drops all the tables and restore them one by one.

Requirements
==============
PHP version: PHP 5.2+
CakePHP version: 2.1

Support
=========
For support and feature request, please create an issue: 
https://github.com/Maldicore/Backups/issues

Contributing to this Plugin
=============================
Please feel free to contribute to the plugin with new issues, requests, unit tests and code fixes or new features. If you want to contribute some code, create a feature branch from develop, and send us your pull request.

License
Copyright 2012, Maldicore Group Pvt Ltd

Licensed under The MIT License: http://www.opensource.org/licenses/mit-license.php
Redistributions of files must retain the above copyright notice.

Copyright
==========
Copyright 2012
Maldicore Group Pvt Ltd
G. Reethimaage Aage
Male', Republic of Maldives
http://maldicore.com