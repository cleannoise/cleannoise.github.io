Install Ubuntu, nginx, php7, mongodb
=

Install php7
-
* https://gist.github.com/hollodotme/418e9b7c6ebc358e7fda

Install mongodb
-
````
- sudo apt-get install libssl-dev
- sudo apt-get install pkg-config
- pecl install mongodb
- echo "extension=mongodb.so" >> `php --ini | grep "Loaded Configuration" | sed -e "s|.*:\s*||"`﻿
````