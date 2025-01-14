Model–view–controller (MVC) is a software design pattern commonly used for developing user interfaces that divides the related program logic into three interconnected elements. These elements are:

**Model**: Represents the application’s data and business logic. It is responsible for accessing data from a database or other sources and processing that data.

**View**: Responsible for rendering the user interface, typically generating HTML output, or in the context of REST, JSON or XML. The view receives data from the model and presents it to the user.

**Controller**: Acts as an intermediary between the Model and the View. It processes user requests, manipulates the model, and returns the appropriate view.