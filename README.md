# Instalasi
- https://www.digitalocean.com/community/tutorials/how-to-install-mongodb-on-ubuntu-18-04
## langkah instalasi
- sudo apt install -y mongodb
- sudo vim /etc/mongodb.conf, comment (#)
```  
bind_ip = 127.0.0.1
```
- sudo service mongodb restart
- mongo mongodb://103.106.81.48:4321
- mongo mongodb://metaforceadmin:Password*1!@103.106.81.48:4321/metaforce
# Setting Authentication
- 
```
mongo mongodb://<host>:<port>
```
- use admin
- 
```
> db.createUser(
  {
    user: "admin",
    pwd: "Visionet123!",
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
