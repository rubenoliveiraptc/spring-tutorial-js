# Spring Tutorial
#### requirements
* Netbeans, Java, Maven, Docker, docker-compose, Git
* create ~/spring-tutorial-js with git clone
* docker-compose > rabbitmq 6000,7000 mongo 29001 postgresql 6543
* java ports 8880,8881,8882

## Simple Rest
* https://spring.io/guides/gs/rest-service/
* create alice port 8880

## RestTemplate
* https://spring.io/guides/gs/consuming-rest/
* create bob override port to 8881
* add resttemplate to alice

## Health and Actuator
* https://spring.io/guides/gs/actuator-service/
* add health to alice and bob

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
