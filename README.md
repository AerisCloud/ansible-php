PHP
===

This role takes care of installing php on a web server to be able to run php application.

Configuration
--------------

### Inventory

```ini
[web:children]
web-somedc-prod

[web-somedc-prod]
web1.somedc.prod         ansible_ssh_host=10.0.1.111

[web-somedc-prod:vars]
# Unix user/group of php-fpm processes
php_fpm_user = apache
php_fpm_group = apache

# What PHP version to use. Available: 5.4, 5.5 and 5.6. Default: 5.4.
php_version = 5.4

# What folder to use to store sessions. Default: /tmp
php_sessions_dir = /tmp
```

*Note:* If you want to change the PHP version on an already provisioned server,
you must first uninstall manually the previous version.

See also
---------

* [PHP](http://php.net/)
