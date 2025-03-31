# web-testing
Набор инструментов для тестирования вашего приложения на Java Spring Boot.


Spring Boot Actuator - предоставляет REST-эндпоинты для мониторинга здоровья, метрик и производительности приложения.
```xml
        <dependency>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-starter-actuator</artifactId>
        </dependency>
```

включим необходиме эндпоинты в application.properties
```properties
management.endpoints.web.exposure.include= health,info,env,beans,metrics
```
