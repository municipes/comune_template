This is a composer based installer for the [Comune Silfi](https://www.drupal.org/project/comune_silfi).

# Prerequisites

1. [Composer](https://getcomposer.org/download/)

It's just composer, isn't it awesome? :)

## Installazione
Per installare il CMS Comune procedi così
1) Installa il codice:
```shell
$ composer create municipes/comune_template project-name --no-install
$ cd project-name
$ composer require drush/drush --no-install
$ composer install
```
2) Configura Drupal eseguendo [setup_step02](scripts/setup_step02__configure_drupal.sh)
3) Configura Comune eseguendo [setup_step03](scripts/setup_step03__configure_municipes.sh)

Se usi ddev puoi installare tutto con un unico comando, esegui [ddev_installer](scripts/municipes_ddev_installer.sh)
```shell
bash <(curl -s -H "Cache-Control: no-cache" "https://raw.githubusercontent.com/municipes/comune_template/10.x/scripts/municipes_ddev_installer.sh")
```


## Installation of Comune Silfi

```
composer create municipes/comune_template:10.x DIRECTORY --no-interaction
```

Composer will create a new directory called DIRECTORY.
The installed folders will contain all Drupal related files in the `web`
directory and any third-party dependencies in the composer `vendor` directory.
Drupal core will be installed to `web/core`. Inside you will find the
html directory with the entire code base of the [Comune Silfi distribution](https://www.drupal.org/project/comune_silfi).
Install your Comune Silfi site like any other Drupal website using the `install.php` script or `drush`.

## Learn more about Composer for Drupal

Checkout this [presentation](https://docs.google.com/presentation/d/1gxcxT6o47xVrfsZ7ZSQKjBRT-gfE54A1Z9kjvvGHwCo/edit#slide=id.p) from @ModsUnraveled.

## Issues

### Install issues for Comune Silfi
[documentation](https://www.drupal.org/docs/8/distributions/comune-silfi/installing-and-updating)

### Comune Silfi issues & Support
For any issues with the platform we kindly ask you to use the [drupal.org](https://www.drupal.org/project/issues/comune_silfi) issue queue.
This way we can centralise all the information and make the feedback available
for other users for documentation purposes. Next to giving people the credit they deserve.

