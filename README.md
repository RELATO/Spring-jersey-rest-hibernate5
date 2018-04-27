# Spring-jersey-rest-hibernate5

## Mysql 5.5 docker up
``` 
docker run --name=mysql -e MYSQL_ROOT_PASSWORD=root -p=3306:3306 -d mysql:5.5

``` 

### Building
``` 
mvn clean package
cp target/springjerseyh5rest.war [/opt/apache-tomcat-8.5.16/webapps]
``` 

### Running the war
```
/opt/apache-tomcat-8.5.16/bin/startup.sh
```

### Testing with Postman
``` 
POST http://localhost:8080/springjerseyh5rest/api/rest/basics/users

{
	"name":"junior",
	"company":"relato"
}

GET http://localhost:8080/springjerseyh5rest/api/rest/basics/users/1

{
    "id": 1,
    "name": "junior",
    "company": "relato"
}

``` 

Source:
https://github.com/ravi115/Hibernate-Tutorials.git
