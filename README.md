Composer integration for contao
===============================

Module which loads the composer autoloader, creates initial composer.json and provide a backend client.

![Backend module](http://img59.imageshack.us/img59/830/composer1.png)

### Installation

##### Checkout repository

Checkout this repository to system/modules/!composer

```
cd /path/to/my/project/documentroot
git clone git@github.com:ContaoCommunityAlliance/Composer.git /tmp/
mv /tmp/Composer/src/system/modules/!composer system/modules/!composer
```

##### Contao page request

Do a normal page request, this will prepare the folder structure and the default composer.json

##### Download composer (the manual way)

Download composer as explained here: http://getcomposer.org/doc/00-intro.md#downloading-the-composer-executable

```
cd ./composer
curl -sS https://getcomposer.org/installer | php
```

##### Download composer (with backend client)

Just call the backend client from the menu, it will tell you that composer is not installed and install it automatically.

##### Add some vendors (the manual way)

Open the composer/composer.json in your prefered editor and add some dependencies as explained here: http://getcomposer.org/doc/04-schema.md

```json
{
    "require": {
        "contao-community-alliance/composer-installer": "dev-master@dev",
        "contao-community-alliance/composer": "dev-master@dev"
    }
}
```

##### Add some vendors (with backend client)

###### Via integrated search

Type your keyword or package name into the search field and press the search button.

![Package search](http://img705.imageshack.us/img705/5623/composer3.png)

Select your package and click the "mark to install" button on the right.
Select prefered version and version contraint to install.

![Package details view](http://img547.imageshack.us/img547/1969/composer4.png)

###### Via integrated editor

![Advanced editor](http://img199.imageshack.us/img199/9184/composer2.png)

Click on "advanced mode" in the backend client and add some dependencies as explained here: http://getcomposer.org/doc/04-schema.md

```json
{
    "require": {
        "contao-community-alliance/composer-installer": "dev-master@dev",
        "contao-community-alliance/composer": "dev-master@dev"
    }
}
```

##### Install the vendors (the manual way)

Tell composer to download the configured vendors

```
php composer.phar install
```

##### Install the vendors (with backend client)

Click on "updated packages" and just wait until composer finished installation.

### Requirements
* php 5.3.4 or higher
* contao 2.11.*
