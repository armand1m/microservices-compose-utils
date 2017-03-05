# microservices-compose-utils

This project contains simple `bash` files with some compose commands, to be used as alias while developing microservices within the `armand1m/microservices` environment.
It can also be used to run multiple microservices together as well.

## Commands available:

 - [x] `init`: Initialize git submodules.
 - [x] `update`: Updates (`git pull origin master`) each git submodule.
 - [x] `build`: Build docker images.
 - [x] `run`: Runs the environment.
   - [x] `run <service-name>`: Runs a service and its dependencies, if specified.
 - [x] `status`: See the containers status.
 - [x] `destroy`: Stop and remove containers.
 - [x] `scale <service>=<number-of-insrtances>`: Scale the number of instances of a service container.
 - [ ] `deploy`: Deploy images to a docker registry.
 - [ ] `publish`: Publish environment into single host or cluster.

 ## Using this repository

 Add it as a `git submodule` in your project and run the commands in a shell.
 Make sure you have Docker running, and Docker Compose in your machine.

 ```shell
 # run it in your project's root folder.
 $ git submodule add https://github.com/armand1m/microservices-compose-utils ./commands
 ```

 Use it:

 ```shell
 # initialize git submodules
 $ ./commands/init

 # build docker images
 $ ./commands/build

 # run services
 $ ./commands/run

 # inspect their logs
 $ ./commands/logs
 ```
