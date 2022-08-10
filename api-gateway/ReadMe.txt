1. Create spring boot starter project with Spring Web and Eureka Discovery Client and Spring GateWay.
2. Annotate ApiGatewayApplication.java with @EnableEurekaClient.
3. Place application.yml file in src/main/resources.
4. Server port and application name also add in application.properties if they are not read correctly from .yml file.
5. Run the application and check the URL: http://localhost:9001 from postman.
6. Check the Eureka server URL: http://localhost:8761 - check if API-GATEWAY registered.


Check below URL for testing user, favourite services through gateway service from postman.
1. For User-
	1. addUser - http://localhost:9001/api/v1/userservice/register with JSON object.
	2. forLogin - http://localhost:9001/api/v1/userservice/login with JSON object.
	
2. For Favourite -
    1. deleteNewsById - http://localhost:9001/api/news/{id}


General Issues:
1. Spring application names should not contain '_' , instead can be used by '-'.
   Ex: USER_SERVICE will not work when we use in gateway .yml file as lb://USER_SERVICE.
2. In .yml - routes - predicates - Path - P should be capital.
