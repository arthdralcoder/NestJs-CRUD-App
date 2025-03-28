NestJS Terminologies and Basic CRUD Application
📌 NestJS Terminologies
1. DTO (Data Transfer Object)
A design pattern used in software engineering to simplify data transfers. Instead of sending data individually, all data is bound into a single object and transferred between layers or networks.

2. Controllers
Responsible for handling requests and responses. They also:

Coordinate the flow of requests.

Execute the corresponding logic.

3. Providers/Services
Define functionalities or dependencies that need to be injected into controllers.

4. Middleware
Middleware functions are executed before route handlers and ensure smooth execution. If a middleware fails, it must pass control to the next available middleware.

5. Guards
Used for authentication. They determine whether a request should be processed by the request handler.

6. Pipes
Used for validation and transformation:

Validation ensures the received data is valid.

Transformation converts the received data into the required format before processing.

7. Exception Filters
Handle unhandled exceptions and process them accordingly.

8. Interceptors
Responsible for:

Transforming the response before sending it to the client.

Modifying or overriding the original function’s behavior.

Handling exceptions and modifying responses dynamically.

9. Lifecycle Events
NestJS provides four lifecycle hooks to manage execution flow:

onModuleInit(): Triggered when all dependencies are initialized.

onApplicationBootstrap(): Called after the entire app is bootstrapped.

onModuleDestroy(): Invoked before a module is destroyed.

onApplicationShutdown(): Executed just before the application terminates (useful for cleanup tasks).

10. Decorators
Special functions that add metadata to classes, methods, or properties. Used to define:

Routes (@Get(), @Post())

Modules (@Module())

Middleware, and more.

🔥 Basic CRUD Application in NestJS
Files Implemented
items.controller.ts

items.service.ts

📌 CRUD Functionalities in items.service.ts
create → Adds an item to the list.

findOne → Finds an item by its ID.

findAll → Retrieves all items.

update → Updates itemName and itemPrice fields.

delete → Removes an item by itemId.

📌 API Endpoints for Testing (Postman)
Operation	Method	Endpoint
Create	GET	http://localhost:3000/items/
Find One	PUT	http://localhost:3000/items/id/
Find All	PUT	http://localhost:3000/items/
Update	PATCH	http://localhost:3000/items/
Delete	DELETE	http://localhost:3000/items/id/
🔑 Difference Between Authorization Middleware & Guards
Middleware: Runs before guards, authenticates users, and then passes the request to the controller.

Guards: Authorize users after authentication, ensuring they have the necessary permissions to access specific routes/resources.
