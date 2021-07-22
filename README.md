# mysql-5.1.73 [![license](https://img.shields.io/github/license/mashape/apistatus.svg?maxAge=2592000)](LICENSE) [![Docker Automated build](https://img.shields.io/docker/pulls/opencdms/mysql.svg)](https://hub.docker.com/r/opencdms/mysql/)

Docker image for MySQL 5.1.73 database based on official [MySQL](https://hub.docker.com/_/mysql/) image which is no longer available.

## Installation

- [Install Docker](https://docs.docker.com/engine/installation/)
- Run docker command to get image: `docker pull opencmds/mysql:5.1.73`
- Validate image successfully downloaded: `docker images`

## Run 

Start a **mysql** server instance:
    
    # general form
    $ $ docker run [OPTIONS] IMAGE[:TAG|@DIGEST] [COMMAND] [ARG...]
    
    # example
    $ docker run -d --name some-mysql -p 3306:3306 -e MYSQL_ROOT_PASSWORD=[my-secret-pw] opencdms/mysql:5.1.73

... where `some-mysql` is the name you want to assign to your container and `[my-secret-pw]` is the password to be set for the MySQL root user. If port 3306 is used then replace `-p 3306:3306` with `-p 3307:3306`
    
Other **commands**:

    ## kill the container
    docker kill [container-id]
    
    # shell script/shell access
    $ docker exec -it opencdms/mysql:5.1.73 bash
    
    # viewing MySQL logs
    $ docker logs opencdms/mysql:5.1.73
    
    # start exisitng container (often: after Docker Engine update)
    docker start [CONTAINER ID]
