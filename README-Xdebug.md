# Enabling Xdebug in PHPStorm

1. Project must be rooted at the git clone root directory, i.e. with `app`,
   `vendor` directories present.
2. Debug port: 9000,9003
3. Server name: "Magento"
  - Map path {Project Root} => `/var/www/html`
4. Preferences: Debug / Skipped Paths. Browse to and add `magento-vars.php`.
5. Telephone button green

PHPStorm will not be able to verify that xdebug is working because of Magento's
crazy handling of URL paths -> file paths. You'll just have to trust that it's
working.

4. You must run `bin/xdebug enable` every time you start the container. TODO

5. Cloud: Replace in `php.ini`:

```dosini
auto_prepend_file = /var/www/html/magento-vars.php
```
