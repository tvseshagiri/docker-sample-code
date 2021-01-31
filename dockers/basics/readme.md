# Docker Commands

## List Containers
Listing running containers 

> `docker ps`

List all (running and stopped containers) with size

> `docker ps -as`

Filter docker containers with names 

> `docker ps --filter "name=mysql"`

List only container IDs

> `docker ps -a -q`

## Remove containers
Remove stopped containers by id

> `docker rm b38cfb53e532`

Remove running container

> `docker rm --force`

Remove all stopped containers

> `docker rm $(docker ps -a -q)`

## Search Containers

Search with a name
> `docker search java`

Filter serach by stars

> `docker search `**` --filter stars=1000 `**` java`
