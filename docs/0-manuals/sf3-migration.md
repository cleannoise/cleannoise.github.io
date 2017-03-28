# Migrate to Symfony 3

* /web/app.php, /web/app_dev.php must be like on: 
https://github.com/symfony/symfony-standard/tree/master/web

* app/config/config.yml add "assets: ~":
````
framework:
    ...
    assets: ~
````

* All services must be inject on services.yml with "" like: 
````
"@service_name" , not @service_name
````

* Remove from /app/routing_dev.yml route "_configurator"
````
resource: "@SensioDistributionBundle/Resources/config/routing/webconfigurator.xml"
````

* at now sonata-admin does not parse this on config.yml:
````
twig:
   form:
       resources:
````

* change DI factory services (for example KnpMenuBundle ):
````
   before:
        factory_service: project_app.menu.menu_builder
        factory_method: createBottomNavbar
   now:
       factory: ["@project_app.menu.menu_builder", createTopNavbar]
````
* on .yml fix regexp variables(for example or validation.yml):
````
   before:
       pattern: "/^(\+[\d]{1,4})$/"
   now:
       pattern: "/^\\(\\+[\\d]{1,4}\\)$/"﻿
````        