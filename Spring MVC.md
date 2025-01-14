**Spring MVC** (Model-View-Controller) is a module within the Spring Framework that provides support **for creating web applications**. It follows the MVC design pattern, which separates the application into three interconnected components: Model, View, and Controller. This separation helps manage complexity in large applications and promotes a clear structure.

### `dispatcherServlet`

The central dispatcher that handles all HTTP requests and responses. It is the front controller in the Spring MVC framework. **It routes requests to appropriate handlers (controllers) and renders the view.**

The `@Controller` annotation is part of the Spring MVC module, which provides support for building web applications by following the Model-View-Controller pattern.

`@RestController` **is a convenient annotation that combines `@Controller` and `@ResponseBody`**, which eliminates the need to annotate every request handling method of the controller class with the _@ResponseBody_ annotation.

Without Spring MVC we would have to write  **plain servlet API** or use another . You can write plain servlets to handle HTTP requests and responses, but this involves more boilerplate code and less flexibility compared to Spring MVC.

It comes with new Beans : `session`, `request`, `global session`

[[Spring Webflux]], [[Model View Controller]], [[Servlet]]