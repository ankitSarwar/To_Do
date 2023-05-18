<h1 align="center"> TodoAPP </h1>

-   The TodoAPP Controller is a part of the Doctor App project, implemented using the Spring Boot framework. It provides various endpoints to perform CRUD operations. 

>### Prerequisites

-   [![SpringBoot](https://camo.githubusercontent.com/a6677a4ec12bd03f835c62db09a8db96a6d726afe3985c8fbf5c43db9b6cb8ad/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f4672616d65776f726b2d537072696e67426f6f742d677265656e)](https://camo.githubusercontent.com/a6677a4ec12bd03f835c62db09a8db96a6d726afe3985c8fbf5c43db9b6cb8ad/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f4672616d65776f726b2d537072696e67426f6f742d677265656e)

-   [![Java](https://camo.githubusercontent.com/be815b7d90eac640a950b5ef6e2bd93f30cab6ac1cd9ace277bc560e3e6fc11c/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f4c616e67756167652d4a617661253230382532306f722532306869676865722d79656c6c6f77)](https://camo.githubusercontent.com/be815b7d90eac640a950b5ef6e2bd93f30cab6ac1cd9ace277bc560e3e6fc11c/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f4c616e67756167652d4a617661253230382532306f722532306869676865722d79656c6c6f77)


>### Data flow
> ----------------------------------------------------------------------------------------------------------------------------------

>### In this project, we have four layers-

-   Controller - The controller layer handles the HTTP requests, translates the JSON parameter to object, and authenticates the request and transfer it to the business (service) layer. In short, it consists of views i.e., frontend part.
-   Service -The business layer handles all the business logic. It consists of service classes and uses services provided by data access layers.
-   Repository - This layer mainatains the database thing on which CRUD operations are performed
-   Model - This layer consists basically the class level things- the various classes required for the project and these classes consists the attributes to be stored.


>## API Endpoints
The following endpoints are available:

- GET /todoPackage/getAllTodos: Get all todos.
- GET /todoPackage/getTodosByStatus?status=<status>: Get todos by status (true or false).
- GET /todoPackage/getTodoById/{id}: Get a todo by ID.
- POST /todoPackage/addTodo: Add a new todo.
- DELETE /todoPackage/deleteTodoById/{id}: Delete a todo by ID.
- PUT /todoPackage/updateTodoById/{id}/{status}: Update the status of a todo.

>## Models
- Todo class
- Represents a todo item.
- id (String): The ID of the todo.
- todoName (String): The name of the todo.
- todoStatus (boolean): The status of the todo (completed or not).
  
>## Controllers
- TodoController clss
- The controller class responsible for handling todo-related requests.

- GET /getAllTodos: Retrieves all todos.
- GET /getTodosByStatus: Retrieves todos based on the specified status.
- GET /getTodoById/{id}: Retrieves a todo by its ID.
- POST /addTodo: Adds a new todo.
- DELETE /deleteTodoById/{id}: Deletes a todo by its ID.
- PUT /updateTodoById/{id}/{status}: Updates the status of a todo.
  
>## Services
- TodoService
- The service class that contains the business logic for managing todos.

- getAllTodos: Retrieves all todos.
- addTodo: Adds a new todo.
- getTodosByUserStatus: Retrieves todos based on the specified status.
- getTodoBasedOnId: Retrieves a todo by its ID.
- removeTodoById: Deletes a todo by its ID.
- updateTodoStatusById: Updates the status of a todo.
  
>## Repository
- TodoDao class 
- The data access object class that manages the todo data.

- getTodosFromDataSource: Retrieves todos from the data source.
- save: Saves a todo to the data source.
- remove: Removes a todo from the data source.
- update: Updates the status of a todo in the data source.
  
>## Summary
The Todo App is a simple Spring Boot application that allows users to manage their todos. It provides endpoints for creating, retrieving, updating, and deleting todos. The app demonstrates the basic usage of Spring Boot and can be extended with additional features such as user authentication, database integration, and error handling.
