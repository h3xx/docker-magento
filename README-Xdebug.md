# Enabling Xdebug in PHPStorm

1. Project must be rooted at the git clone root directory, i.e. with `app`,
   `vendor` directories present.
1. Server name: "Magento"
  - Map path {Project Root} => `/var/www/html`
2. Preferences: Debug / Skipped Paths. Browse to and add `magento-vars.php`.
3. Telephone button green

PHPStorm will not be able to verify that xdebug is working because of Magento's
crazy handling of URL paths -> file paths. You'll just have to trust that it's
working.

4. You must run `bin/xdebug enable` every time you start the container. TODO

5. Cloud: Replace in `php.ini`:

```dosini
auto_prepend_file = /var/www/html/magento-vars.php
```
