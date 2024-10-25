# application.properties for Native
spring.profiles.active=native
spring.cloud.config.server.native.search-locations=classpath:/configs

# application.properties for Git
spring.profiles.active=git
spring.cloud.config.server.git.uri=https://github.com/your-repo/config-repo

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