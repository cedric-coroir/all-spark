# all-spark
Well of all spark

# Docker
### Database Volume
```sh
mkdir -p /data/db
sudo docker create -v /data/db:/datadb --name datadb dockerfile/mongodb
```

### MongoDb instance
```sh
sudo docker run -d -p 27017:27017 --volumes-from datadb --name mongodb dockerfile/mongodb
```
