# microservices-compose-utils

This project contains simple `bash` files that can be used as alias to `docker-compose` commands. 
They are helpful to be used while developing microservices within the [`armand1m/microservices`](https://github.com/armand1m/microservices) environment.
It can also be used to run multiple microservices together as well.

## Commands available:

 - [x] `init`: Initialize git submodules.
 - [x] `update`: Updates (`git pull origin master`) each git submodule.
 - [x] `build`: Build docker images.
   - [x] `build <service-name>`: Builds a single service.
 - [x] `run`: Runs the environment.
   - [x] `run <service-name>`: Runs a service and its dependencies, if specified.
   - [x] `run --build`: Forces rebuild and runs all services.
   - [x] `run --build <service-name>`: Forces rebuild and runs a single service.
 - [x] `logs`: Get services logs to STDOUT
   - [x] `logs -f`: Follow all services logs to STDOUT
   - [x] `logs <service-name>`: Get a single service logs to STDOUT
   - [x] `logs -f <service-name>`: Follow a single service logs to STDOUT
 - [x] `status`: See the containers status.
 - [x] `destroy`: Stop and remove containers.
 - [x] `scale <service>=<number-of-insrtances>`: Scale the number of instances of a service container.
 - [ ] `deploy`: Deploy images to a docker registry.
 - [ ] `publish`: Publish environment into single host or cluster.

 ## Using this repository

 Add it as a `git submodule` in your project and run the commands in a shell.
 Make sure you have Docker running, and Docker Compose in your machine.

 ```shell
 # add this project as a submodule into a folder. I like to use ./commands.
 $ git submodule add https://github.com/armand1m/microservices-compose-utils ./commands
 ```

 Use it:

 ```shell
 # initialize git submodules
 $ ./commands/init

 # updates all git submodules
 $ ./commands/update

 # build docker images
 $ ./commands/build

 # run services
 $ ./commands/run

 # see all services logs
 $ ./commands/logs

 # follow all services logs
 $ ./commands/logs -f

 # see all services status
 $ ./commands/status
 ```
