## API Version
http://52.62.49.204:7180/api/version
v16

## CM version
http://52.62.49.204:7180/api/v16/cm/version
{
  "version" : "5.11.0",
  "buildUser" : "jenkins",
  "buildTimestamp" : "20170412-1255",
  "gitHash" : "70cb1442626406432a6e7af5bdf206a384ca3f98",
  "snapshot" : false
}

## List all CM users

http://52.62.49.204:7180/api/v16/users
{
  "items" : [ {
    "name" : "admin",
    "roles" : [ "ROLE_ADMIN" ]
  }, {
    "name" : "minotaur",
    "roles" : [ "ROLE_CONFIGURATOR" ]
  } ]
}

## 