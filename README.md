rackspace_memcached Cookbook
==================

Installs memcached and provides a template for its main configuration file.

Requirements
------------

### Platforms
- CentOS 6.4
- Ubuntu 12.04
- Debian 7.2

May work on other systems with or without modification.

### Cookbooks
This cook book does not depend on any other cookbooks

Attributes
----------
The following are node attributes passed to the template:

- `['rackspace_memcached']['config']['memory']` - maximum memory for memcached instances. Default is 64M.
- `['rackspace_memcached']['config']['user']` - user to run memcached as.
- `['rackspace_memcached']['config']['port']` - TCP port for memcached to listen on. Default is 11211.
- `['rackspace_memcached']['config']['udp_port']` - UDP port for memcached to listen on. Default is 11211.
- `['rackspace_memcached']['config']['listen']` - IP address for memcache to listen on, defaults to **0.0.0.0** (world accessible).
- `['rackspace_memcached']['config']['maxconn']` - maximum number of connections to accept (defaults to 1024)
- `['rackspace_memcached']['config']['max_object_size']` - maximum size of an object to cache (defaults to 1MB)
- `['rackspace_memcached']['config']['logfilename']` - logfile to which memcached output will be redirected in /var/log/$logfilename.


Usage
-----
Simply set the attributes and the cookbook will configure the `/etc/memcached.conf` file (Ubuntu, Debian) or /etc/sysconfig/memcached file (CentOS, RHEL). If you want to use multiple memcached instances, you'll need to modify the recipe to disable the startup script and the template in the default recipe.

Contributing
------------
* See contributing guidelines [here](https://github.com/rackspace-cookbooks/contributing/blob/master/CONTRIBUTING.md)

Testing
-------
* See contributing guidelines [here](https://github.com/rackspace-cookbooks/contributing/blob/master/CONTRIBUTING.md)

License & Authors
-----------------
- Author:: Joshua Timberman (<joshua@opscode.com>)
- Author:: Joshua Sierles (<joshua@37signals.com>)
- Author:: Kent Shultz (<kent.shultz@rackspace.com>)

```text
Copyright:: 2009-2012, Opscode, Inc
Copyright:: 2009, 37signals
Copyright:: 2014, Rackspace, US Inc.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```
