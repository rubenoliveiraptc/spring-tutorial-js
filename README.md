# Spring Tutorial
#### requirements
* Netbeans, Java, Maven, Docker, docker-compose, Git
* create ~/spring-tutorial-js with git clone
git clone git@github.com:rubenoliveiraptc/spring-tutorial-js.git
* docker-compose > rabbitmq 6000,7000 mongo 29001 postgresql 6543
* java ports 8880,8881,8882

## Simple Rest
* https://spring.io/guides/gs/rest-service/
* create alice port 8880
mkdir alice
cd alice/
mkdir -p src/main/java/hello
nano pom.xml
nano src/main/java/hello/Greeting.java
nano src/main/java/hello/GreetingController.java
nano src/main/java/hello/Application.java
mvn clean package
java -jar target/alice-0.1.0.jar 
java -Dserver.port=8880 -jar target/alice-0.1.0.jar
http://localhost:8880/greeting
http://localhost:8880/greeting?name=User



## RestTemplate
* https://spring.io/guides/gs/consuming-rest/
* create bob override port to 8881
* add resttemplate to alice
add empty contructor to Greeting and toString method

## Health and Actuator
* https://spring.io/guides/gs/actuator-service/
* add health to alice and bob
curl http://localhost:8880/health
curl http://localhost:8881/health

## Spring AMQP
https://spring.io/guides/gs/messaging-rabbitmq/
* create charlie as a consumer port 8882 and add bob as producer
https://github.com/zhentao/rabbit-ha-example


## Spring Data Postgresql
* https://spring.io/guides/gs/accessing-data-jpa/
* https://spring.io/guides/gs/accessing-data-rest/
* add jpa to charlie

## Spring Data Mongo
* https://spring.io/guides/gs/accessing-data-mongodb/
* https://spring.io/guides/gs/accessing-mongodb-data-rest/
* add mongo to producer

## Spring Sleuth
* http://cloud.spring.io/spring-cloud-sleuth/
* add sleuth to alice,bob,charlie



## Extra
Tune tomcat,logback,spring profiles


## Spring JdbcTemplate
https://spring.io/guides/gs/relational-data-access/

Async  https://spring.io/guides/gs/async-method/

Service Registration and Discovery https://spring.io/guides/gs/service-registration-and-discovery/

Docker
https://spring.io/guides/gs/spring-boot-docker/
