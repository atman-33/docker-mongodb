## create mongodb container and user
```
docker-compose build --no-cache
docker-compose up -d
```

The following is checking that db created.  

## check mongodb container exists
```
docker ps
```

## move to mongodb container to operate db
```
docker exec -it mongodb bash
```

## connect to mongodb server
```
mongosh mongodb://localhost:27017
```

## check created db and users

*admin => root*
```
use admin
db.auth("root", "pass")
```

*sampledb => sampleuser*
```
use sampledb
db.auth("sampleuser", "pass")
```

## mongodb URL
```
mongodb://localhost:27017
mongodb://root:pass@localhost:27017/admin
mongodb://sampleuser:pass@localhost:27017/sampledb
```