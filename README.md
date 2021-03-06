[![Build Status](https://travis-ci.org/brint/wordpress-cookbook.svg?branch=master)](https://travis-ci.org/brint/wordpress-cookbook)
[![Dependency Status](https://gemnasium.com/brint/wordpress-cookbook.svg)](https://gemnasium.com/brint/wordpress-cookbook)

Description
===========

The Chef WordPress cookbook installs and configures WordPress according to the instructions at http://codex.wordpress.org/Installing_WordPress.

Description
===========

This cookbook does not set up the WordPress blog. You will need to do this manually by going to http://hostname/wp-admin/install.php (this URL may be different if you change the attribute values).

Requirements
============

Platform
--------

* Ubuntu 10.04, 12.04, 14.04
* RHEL/CentOS 5, 6
* Windows

Cookbooks
---------

* mysql
* mysql-chef_gem
* php
* apache2
* iis
* windows
* openssl (uses library to generate secure passwords)

Attributes
==========

### WordPress

* `node['wordpress']['version']` - Version of WordPress to download. Use 'latest' to download most recent version.
* `node['wordpress']['parent_dir']` - Parent directory to where WordPress will be extracted. (Windows Only)
* `node['wordpress']['dir']` - Location to place WordPress files.
* `node['wordpress']['db']['name']` - Name of the WordPress MySQL database.
* `node['wordpress']['db']['host']` - Host of the WordPress MySQL database.
* `node['wordpress']['db']['user']` - Name of the WordPress MySQL user.
* `node['wordpress']['db']['pass']` - Password of the WordPress MySQL user. By default, generated using openssl cookbook.
* `node['wordpress']['db']['prefix']` - Prefix of all MySQL tables created by WordPress.
* `node['wordpress']['db']['charset']` - [Character set](http://dev.mysql.com/doc/refman/5.7/en/charset-charsets.html) of the WordPress MySQL database tables. Defaults to 'utf8'.
* `node['wordpress']['db']['collate']` - [Collation](http://dev.mysql.com/doc/refman/5.7/en/charset-collation-effect.html) of the WordPress MySQL database tables.
* `node['wordpress']['allow_multisite']` - Enable [multisite](http://codex.wordpress.org/Create_A_Network) features (default: false).

Usage
=====

Add the "wordpress" recipe to your node's run list or role, or include the recipe in another cookbook.

License and Author
==================

* Author:: Barry Steinglass (barry@opscode.com)
* Author:: Joshua Timberman (joshua@opscode.com)
* Author:: Seth Chisamore (schisamo@opscode.com)
* Author:: Lucas Hansen (lucash@opscode.com)
* Author:: Julian C. Dunn (jdunn@getchef.com)

Copyright:: 2010-2013, Chef Software, Inc.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
