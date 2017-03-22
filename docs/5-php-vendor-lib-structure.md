Php vendor lib structure
=

Example 1:
-
    All .php files on root folder
    Structure:
        /Controller/
        /Lib/
        /Tests/
        /.gitattributes
        /.ginignore
        /composer.json
        /phpunit.xml.dist
        /README.md

Example 2:
-
    All additional files (.md, ,.xml) on root, .php files on /src, doc files on /doc, test cases on /tests, but phpunit.xml.dist on root
    Structure:
        /docs/
        /src/
        /tests/
        /.gitattributes
        /.ginignore
        /composer.json
        /phpunit.xml.dist
        /README.md

Example 3:
-
    All additional files (.md, ,.xml) on root, .php files on /src, doc files on /doc, test cases and phpunit.xml.dist on /tests
    Structure:
        /docs/
        /src/
        /tests/
        /tests/phpunit.xml.dist
        /.gitattributes
        /.ginignore
        /composer.json
        /README.md

Composer optimization:
-
    All libs must includes .gitattributes file for optimization composer.
    Composer must be runs with --prefer-dist
    .gitattributes example:
        /docs               export-ignore
        /tests              export-ignore
        /.gitattributes     export-ignore
        /.gitignore         export-ignore
        /.travis.yml        export-ignore
        /phpunit.xml        export-ignore
        /README.md          export-ignore


Links:
* https://www.reddit.com/r/PHP/comments/2jzp6k/i_dont_need_your_tests_in_my_production/
* http://blog.nikolaposa.in.rs/2017/01/16/on-structuring-php-projects/
* http://symfony.com/doc/current/contributing/index.html
* https://framework.zend.com/participate/contributor-guide
* https://laravel.com/docs/5.4/contributions
* https://github.com/thephpleague/skeleton