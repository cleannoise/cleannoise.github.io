PHP7 with mongodb on composer
=

Add to composer.json:
1. Correct repository(without this option you will see errors)
````
"repositories": [
        {"url": "https://github.com/alcaeus/mongo-php-adapter", "type": "vcs"}
    ]
````

2. Add correct dependencies:
````
"require": {
...
        "alcaeus/mongo-php-adapter": "dev-master",
        "doctrine/mongodb": "dev-master",
        "doctrine/mongodb-odm": "dev-master",
````

Links:
-
* https://github.com/alcaeus/mongo-php-adapter