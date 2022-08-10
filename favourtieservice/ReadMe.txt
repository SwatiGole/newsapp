1. Create spring boot starter project with Spring Web and Eureka Discovery Client.
2. Annotate FavourtieserviceApplication.java with @EnableEurekaClient.
3. Place application.yml file in src/main/resources.
4. Server port and application name also add in application.properties if they are not read correctly from .yml file.
5. Run the application and check the URL: http://localhost:8081 from postman.
6. Check the Eureka server URL : http://localhost:8761 - check if FAVOURITE-SERVICE registered.


