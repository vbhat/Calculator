# Calculator 
A calculator app built using Vue.js and Go to be used for demo purposes. This is based on this                       [tutorial](https://medium.com/@adeshg7/vuejs-golang-a-rare-combination-53538b6fb918). Docker has been added to the project to demonstrate how the intern project will be setup. 

## Setup
Make sure you have [Docker](https://www.docker.com/products/docker-desktop) and [Docker Compose](https://docs.docker.com/compose/) installed.

## Docker Provisioning
To build the images referenced in your project run the following command in your current directory after you have cloned the repo
```
docker-compose -f docker-compose.yml build
```

Once the build completes, you can spin up the services by running
```
docker-compose -f docker-compose.yml up
```
At this point you can access the frontend through your browser at `localhost:8080`.

Bring down the services by running
```
docker-compose -f docker-compose.yml down
```

## Docker Housekeeping
To remove containers not being used in the compose file and any created images
```
docker-compose -f docker-compose.yml down --remove-orphans --rmi all
```

Remove all unused containers, networks, images (both dangling and unreferenced), and optionally, volumes.
```
docker system prune -af
```
More information can be found [here](https://vsupalov.com/cleaning-up-after-docker/)

