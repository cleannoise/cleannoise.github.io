- BackUp data to c:\mongodb\bin\dump\db_name
````
mongodump -d db_name -o c:\data\dump
````

- Restore data from c:\mongodb\bin\dump\db_name
````
mongorestore --drop -d db_namec:\data\dump\db_name
````