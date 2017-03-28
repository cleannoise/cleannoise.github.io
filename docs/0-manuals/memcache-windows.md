Install memcache on wondows
=

1) http://www.ubergizmo.com/how-to/install-memcached-windows/

2) run on console
````
sc create "Memcached11211" binPath= "C:\memcached\memcached.exe -d runservice -p 11211" DisplayName= "Memcached11211" start= auto
````

File for test:
```
<?php

 $memcache = new Memcache;
 $memcache->connect("localhost",11211); # You might need to set "localhost" to "127.0.0.1"
 echo "Server's version: " . $memcache->getVersion() . "<br />\n";
 $tmp_object = new stdClass;
 $tmp_object->str_attr = "test";
 $tmp_object->int_attr = 123;
 $memcache->set("key",$tmp_object,false,10);
 echo "Store data in the cache (data will expire in 10 seconds)<br />\n";
 echo "Data from the cache:<br />\n";
 var_dump($memcache->get("key"));
````