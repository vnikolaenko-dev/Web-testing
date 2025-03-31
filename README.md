# web-testing
<img src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiSqT1SJ2-10Nt4SfENScW41TuQBkqvHpApsNeBw6h44_KLbyCywu8NO_y_d4ug6bfLFPKM-z0groqAkCdzBy9oS1GTxpOI_IU0YEANjFETgemUnLKqTZnxAgqQtEJ3aWHEVfyxMmAK4fA/s1600/spring-boot-logo.png" title="spring" alt="spring" width="300" height="150"/>&nbsp;
</br>
Набор инструментов для тестирования вашего приложения на Java Spring Boot.
</br>
</br><img src="https://github.com/devicons/devicon/blob/master/icons/prometheus/prometheus-plain-wordmark.svg" title="prometheus" alt="prometheus" width="75" height="75"/>&nbsp; - приложение, используемое для мониторинга событий, сбора и хранения метрик.
</br><img src="https://github.com/devicons/devicon/blob/master/icons/grafana/grafana-plain-wordmark.svg" title="grafana" alt="grafana" width="75" height="75"/>&nbsp; - программная система визуализации данных, ориентированная на данные систем ИТ-мониторинга.
</br><img src="https://avatars.githubusercontent.com/u/12608521?s=200&v=4" title="artillery" alt="artillery" width="75" height="75"/>&nbsp; - платформа для нагрузочного тестирования.


В этом гайде мы рассмторим следующие инструменты:


## Часть №1

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
</br>
http://localhost:8080/actuator/metrics/system.cpu.usage - загрузка процессора
</br>
http://localhost:8080/actuator/heapdump - скачать дамп памяти JVM в формате .hprof
</br>
и т.д.

## Часть №2

Видеть информацию в формате Json, конечно, полезно, однако хотелось бы иметь более удобный способ оценки работоспособности продукта.

Здесь нам поможет:
</br>1) Prometheus - система мониторинга и сбора метрик с открытым исходным кодом
</br>2) Grafana  - инструмент для визуализации данных

