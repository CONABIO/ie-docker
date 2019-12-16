# ie-docker
Instructions for deployment and building of docker image for ecosystem integrity pipeline

# For building docker image:

1) git clone this repo:

```
https://github.com/CONABIO/ie-docker.git
```

2) Enter to ie-docker directory:

```
cd ie-docker
```


3) Set and change according to your configuration next variables in terminal:

```
BUILD_DIR=3.6.1
CONTAINER_NAME=r-geospatial-ie
REPO_URL=palmoreck/r_geospatial_ie #this REPO_RUL is provisional
VERSION=v1 #first version of docker image for ie
```

4) Build:

```
docker build $BUILD_DIR --force-rm -t $REPO_URL:$VERSION
```

# For running docker image:

1) Set and change according to your configuration next variables in terminal:


```
DIR=/home/user/my_working_dir
REPO_URL=palmoreck/r_geospatial_ie #this REPO_RUL is provisional
VERSION=v1
CONTAINER_NAME=r-geospatial-ie
PASSWORD=mypassword
PORT=8787
```

2) Run docker image:

```
docker run -d -p $PORT:8787 -v $DIR:/home/rstudio/ --name $CONTAINER_NAME -e PASSWORD=$PASSWORD $REPO_URL:$VERSION 
```


3) In a browser go to localhost at $PORT where docker container is deployed: 

```
localhost:8787
``` 
