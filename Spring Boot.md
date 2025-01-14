Spring Boot is an open source Java framework created by spring community. It makes it easy to create stand-alone, production-grade Spring based Applications that you can "just run".
## Features

- Create stand-alone Spring applications
- Embed Tomcat, Jetty or Undertow directly (no need to deploy WAR files) with spring MVC.
- Provide opinionated 'starter' dependencies to simplify your build configuration
- Automatically configure Spring and 3rd party libraries whenever possible
- Provide production-ready features such as metrics, health checks, and externalized configuration
- Absolutely no code generation and no requirement for XML configuration

## Advantages
- Auto configuration
-  Uber jar
- Starter

For example we would configure beans in XML
```xml
<beans xmlns="http://www.springframework.org/schema/beans"
       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
       xsi:schemaLocation="http://www.springframework.org/schema/beans             http://www.springframework.org/schema/beans/spring-beans.xsd">
    <bean id="myBean" class="com.example.MyBean">
        <!-- bean properties -->
    </bean>
</beans>
```

With spring boot it's easier :

```java
@Configuration
public class AppConfig {

    @Bean
    public MyBean myBean() {
        return new MyBean();
    }
}
```