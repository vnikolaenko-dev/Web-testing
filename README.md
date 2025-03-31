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
management.endpoints.web.exposure.include=health,info,env,beans,metrics
```

теперь при запуске нашего приложения мы можем смтореть различные метрики:
</br>
http://localhost:8080/actuator/helth - общее состояние приложения
http://localhost:8080/actuator/metrics/system.cpu.usage - загрузка процессора
и т.д.

