# Spring Boot Demo Application

## Prerequisites Installation

```sh
apt-get update 
apt-get install default-java <br>
apt-get install maven <br>
```

Run MySQL Docker 

> `docker run -p 3306:3306 --name mysql-server -e MYSQL_ROOT_PASSWORD=root -d mysql:8.0.23`

Connect to MySQL using mysql command

`docker exec -it  mysql-server mysql -uroot -p`

Create Students Database 

`create database studentsDb;`

Run MySQL with custom volume for data persistence

`docker run  -p 3306:3306 --name mysql-server -v mysql-server-db:/var/lib/mysql -e MYSQL_ROOT_PASSWORD=root -d mysql:8.0.23`

Insert Student with curl 

`curl -i -H "Content-Type:application/json" -d '{"firstName": "Telkapalli", "lastName": "Seshagiri", "city": "Hyderabad"}' http://localhost:8080/student`


Delete Student with ID

`curl -X DELETE http://localhost:8080/student/1`

Docker Compose Scale an application to number of instances

`docker-compose up --scale boot-api-app=3`