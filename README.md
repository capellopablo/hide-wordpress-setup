# Hide WordPress Install

Custom WordPress intall for security

## Notes

* Usar WordPress como dependencia de composer.
* Datos del configuración del entorno fuera de la carpeta pública
* WordPress core en carpeta app para no dejar referencias wp
* Resources: Carpeta de wp-content custom para no dejar referencias
* Modules: Carpeta de plugins custom para no dejar referencias de plugins
* {custom-theme-name}: Nombre personalizado del theme y child para no dejar referencias del theme activo


## Folder structure

```
domain.com
 - {environment}.config.php
 - composer.json
 - /vendor/
 - /public/
    - - index.php
    - - wp-config.php
    - - /app/ (wp)
    - - /resources/ (custom wp-content)
    - - - /themes/
    - - - - /{custom-theme-name}/
    - - - /modules/ (wp plugins)
    - - - /mu-plugins/ 
    - - - - custom-theme-dir.php
    - - - - mu-require.php
```


### Installing

* Clone repository
* Edit composer file
* Run composer install