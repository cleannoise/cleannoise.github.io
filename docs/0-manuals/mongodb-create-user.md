# Create user for MongoDB

1) Connect to mongoDB:
````
mongo --port 27017
````

2) on command:
````
use database_name
db.createUser({user:"admin_name", pwd:"1234",roles:["readWrite","dbAdmin"]})﻿
````