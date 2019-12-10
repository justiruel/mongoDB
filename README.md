# Instalasi
- https://www.digitalocean.com/community/tutorials/how-to-install-mongodb-on-ubuntu-18-04
# Setting Authentication
- mongo mongodb://<host>:<port>
- use admin
- 
```
> db.createUser(
  {
    user: "useradmin",
    pwd: "Password1!",
    roles: [ { role: "readWrite", db: "metaforce" } ]
  }
)
```
- mongod.cfg
```
systemLog:
  destination: file
  path: "D:\\APP\\mongo\\log\\mongo.log"
  logAppend: true
security:
  authorization: enabled
```
- mongod --config D:\APP\mongo\mongod.cfg
- mongo mongodb://superadmin:thepianohasbeendrinking@<host>:<port>
- jika menggunakan linux => https://medium.com/mongoaudit/how-to-enable-authentication-on-mongodb-b9e8a924efac
