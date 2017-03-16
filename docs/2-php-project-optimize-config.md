= PHP project general optimization configurations =

1. Composer Optimization

    1.1 Class Autoloading Optimization
    - add to composer.json:
        "config": {
            "optimize-autoloader": true,
            "classmap-authoritative": true
        }
    - run
        composer install -a -o
        composer dump-autoload -a -o

    1.2 Install vendors from dist
    add to composer.json:
        "config": {
            "preferred-install": {
                "*": "dist"
            }
        }
    - run
        composer install -o -a --prefer-dist

    Links:
    * https://getcomposer.org/doc/articles/autoloader-optimization.md
    * https://habrahabr.ru/post/258891/
    * https://www.reddit.com/r/PHP/comments/2jzp6k/i_dont_need_your_tests_in_my_production/

2. PHP 7 configuration

Links:
* https://www.phpclasses.org/blog/post/493-php-performance-evolution.html

3. Nginx configuration

4. MySQL configuration