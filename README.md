# Task Service

A Simple Task Management Service with the help of actix web along with task management in Aws Dynamodb.


### How to run


```
git clone https://github.com/to4to/task-service.git
```

```
cd task-service
```
```
cargo build# Task Service

A Simple Task Management Service built with Actix Web and AWS DynamoDB.

## Features

- Task creation, retrieval, and state management
- Integration with AWS DynamoDB for persistent storage
- RESTful API endpoints for task operations

## Prerequisites

- Rust (latest stable version)
- AWS credentials configured for DynamoDB access

## How to Run

1. Clone the repository:

    ```sh
    git clone https://github.com/to4to/task-service.git
    ```

2. Navigate to the project directory:

    ```sh
    cd task-service
    ```

3. Build the project:

    ```sh
    cargo build
    ```

4. Run the project:

    ```sh
    cargo run
    ```

## API Endpoints

### Create a Task

- **URL:** `/task`
- **Method:** `POST`
- **Request Body:**

    ```json
    {
        "user_id": "string",
        "task_type": "string",
        "source_file": "string"
    }
    ```

- **Response:**

    ```json
    {
        "task_global_id": "string"
    }
    ```

### Get a Task

- **URL:** `/task/{task_global_id}`
- **Method:** `GET`
- **Response:**

    ```json
    {
        "user_uuid": "string",
        "task_uuid": "string",
        "task_type": "string",
        "state": "string",
        "source_file": "string",
        "result_file": "string"
    }
    ```

### Update Task State

- **URL:** `/task/{task_global_id}/[start|pause|fail|complete]`
- **Method:** `PUT`
- **Request Body (for complete):**

    ```json
    {
        "result_file": "string"
    }
    ```

- **Response:**

    ```json
    {
        "task_global_id": "string"
    }
    ```

## Project Structure

- **src/api/**: Contains the API endpoint handlers.
- **src/model/**: Contains the data models.
- **src/repository/**: Contains the DynamoDB repository implementation.
- **src/main.rs**: Entry point of the application.

## Dependencies

- Actix Web
- AWS SDK for Rust (DynamoDB)
- Serde for JSON serialization/deserialization
- UUID for unique task identifiers
- Strum for enum string representations
- Log and Env Logger for logging

## Contributing

Contributions are welcome! Please open an issue or submit a pull request.

## License

This project is licensed under the MIT License.

## Contact

For any questions or suggestions, please open an issue in the repository.

```

```
cargo run
```

Any Suggestions are welcomed.




