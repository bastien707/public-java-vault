The Fat or Uber jar **contains the application and all its dependencies**, including an embedded web server, making it self-contained and easy to deploy.

The benefit is to have to maintain only one jar so it's easier to deploy because it's portable and it contains all the dependencies.

### How it works  with spring boot ?

- It uses a plugin `spring-boot-maven-plugin` or `spring-boot-gradle-plugin` to create the jar.
- To generate the fat jar you can run the command `mvn clean package`[^1]


[^1]: `mvn clean` will delete the target folder.