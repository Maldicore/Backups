Backup and Restore Plugin for CakePHP
=====================================
Version 1.0 for cake 2.x

This backup and restore plugin enables developers to quickly and easily backup and restore both database schema and data based on backup dates.

As you develop your application, changes to the database need to be managed in a consistent and easy manner, especially in a team environment where different people bring in different changes and this can get extremely difficult at times. Backup and restore enables you to share and co-ordinate database changes as well as data in a manageable fashion distributed using git itself, hence significantly removing the complexity of handling these changes (no more phpmyadmin for database updates). We have used backup and restore Plugin in production environments with multiple backups and for database roll-outs for fast deployments, without any hiccups. However, in the event we have missed a scenario we cannot be held responsible for any data loss, use this at your own risk. Said that we would love to fix any bug found by you! :)

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

![Backup](https://lh3.googleusercontent.com/-zPRwqzgjb7s/ULVo939aa3I/AAAAAAAACYQ/e85juiba1zg/s400/Selection_067.png)

Restoring
----------
* In your cakePHP application root folder (in a terminal) execute

<pre>
	./app/Console/cake Backups.backup restore
</pre>

It will prompt you all available backup versions with date and time, just type a corresponding version (eg: 0) and hit enter

![Restore](https://lh5.googleusercontent.com/-O7FI-eLyiWc/ULVVtVhCmtI/AAAAAAAACXk/LNerKNlBQc8/s400/Selection_068.png)

Troubleshooting
----------------
* In case of any errors that is not predicted in the script you can always (manually) restore from one of the backup.

Notes
------
* The database user (in cakephp database config) must have rights to drop tables for restore to work! As the restore process drops the tables and restore them one by one.

Requirements
==============
PHP version: PHP 5.2+
CakePHP version: 2.1

Support
=========
For support and feature request, please create an issue: 
https://github.com/Maldicore/Backups/issues

ToDo List
==========
* UnitTesting
* Settings to choose datasource and output directory

Contributing to this Plugin
=============================
Please feel free to contribute to the plugin with new issues, requests, unit tests and code fixes or new features. If you want to contribute some code, create a feature branch and send us your pull request.

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