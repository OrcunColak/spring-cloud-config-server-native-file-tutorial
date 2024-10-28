# Native
spring.profiles.active=native
spring.cloud.config.server.native.search-locations=classpath:/configs

# To Refresh

```
curl -X POST http://localhost:8080/actuator/refresh
```

This prints the name of refreshed variables

```
>curl -X POST http://localhost:8080/actuator/refresh
["eureka.client.serviceUrl.defaultZone"]

>curl -X POST http://localhost:8080/actuator/refresh
[]
```