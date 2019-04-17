# Hide WordPress Install

Custom WordPress install for security or other reasons

## Features

* Use WordPress as a composer dependency.
* Environment configuration outside the public directory
* WordPress core in app folder to not leave references /wp/
* Resources: Custom directory to not to leave references /wp-content/ 
* Modules: Custom directory to not to leave references /plugins/
* {custom-theme-name}: Custom name of the theme and child to not leave references of the active theme


## Folder structure

```
domain.com
 - {environment}.config.php
 - composer.json
 - /vendor/                        (Composer packages folder)
 - /public/                        (Public directory)
    - - index.php
    - - wp-config.php
    - - /app/                      (Here is WordPress core)
    - - /resources/                (Custom wp-content directory)
    - - - /themes/
    - - - - /{custom-theme-name}/
    - - - /modules/                (WordPress plugin directory)
    - - - /mu-plugins/ 
    - - - - custom-theme-dir.php
    - - - - mu-require.php
```


### Installing

* Clone repository
* Edit composer file
* Run composer install