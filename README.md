Markdown
# ASP.NET MVC Web API To-Do List App👌

This project is a RESTful API for managing a user's to-do list, with optional admin functionalities. It utilizes ASP.NET MVC and implements authorization for secure access control.

## Functionality

* **User Management:**
    * Users can register, log in, and view their own to-do items. (Basic users)
    * Admins can add, edit, and delete all users and their to-do items. (Admin users)
* **To-Do Management:**
    * Users can add, update, and delete their own to-do items.
    * To-do items include details like description and location (optional).

## API Endpoints

| URL                | Method | Authorization | Description                        | Request Body | Response Body          |
|--------------------|--------|---------------|------------------------------------|---------------|-------------------------|
| /api/todo          | GET    | User           | Get all user's to-do items           | -             | List of to-do items       |
| /api/todo/{id}     | GET    | User           | Get a specific user's to-do item by ID | -             | To-do item details      |
| /api/todo          | POST   | User           | Add a new to-do item                | To-do details | Created to-do item details |
| /api/todo/{id}     | PUT    | User           | Update a user's to-do item          | To-do details | Updated to-do item details |
| /api/todo/{id}     | DELETE | User           | Delete a user's to-do item           | -             | Success/Failure message |
| /api/user          | GET    | User (Admin)  | Get current user details (User) / Get all users (Admin) | -             | User details / List of users |
| /api/user          | POST   | Admin          | Add a new user                     | User details  | Created user details   |
| /api/user/{id}     | DELETE | Admin          | Delete a user and their to-do items | -             | Success/Failure message |
| /api/login         | POST   | -              | Login with username/password        | Login credentials | JWT token               |

## Technical Details

* Persistent Storage: JSON files (temporary, consider database integration)
* Dependency Injection: Facilitates switching to database storage in the future
* Logging: Records request details (start time, controller/action, user, duration)

## Client Notes

* Default page displays user's to-do list (add, update, delete options).
* Login page displayed if no token or expired token.
* Admin users have a link to manage users.
* Login page includes a Postman button for testing API endpoints.

## Challenges (Optional)

* User details update (name, password)
* Admin to-do management as a regular user
* Google account login integration

## Getting Started

1. Clone the repository.
2. Install required dependencies (.NET Core SDK, Node.js, npm).
3. Configure project settings (connection strings, etc.).
4. Run the project (server and client).

## Contribution

Pull requests are welcome! Please follow our contribution guidelines.
