# Laravel React Inertia Project

This project is a web application built with Laravel, React, and Inertia.js.

## Installation

Follow these steps to set up the project:

1. Clone the repository:

    ```
    git clone https://github.com/c99rahul/laravel-react-inertia.git
    ```

2. Navigate to the project directory:

    ```
    cd laravel-react-inertia
    ```

3. Install PHP dependencies (Laravel packages):

    ```
    composer install
    ```

4. Install JavaScript dependencies (Vite, React, and Inertia):

    ```
    pnpm install
    ```

5. Set up the environment file:

    - Copy `.env.example` and rename it to `.env`
    - Add your database credentials to the newly-created `.env` file:
        ```
        DB_CONNECTION=pgsql
        DB_HOST=127.0.0.1
        DB_PORT=5432
        DB_DATABASE=laravel_react_inertia
        DB_USERNAME=your_db_username
        DB_PASSWORD=your_db_password
        ```

6. Create the database:

    - Create a new database named `laravel_react_inertia` in your Database server
    - In the newly-created database, create the `users` table using the following SQL command:
        ```sql
        CREATE TABLE users (
            id SERIAL PRIMARY KEY,
            email VARCHAR(100) UNIQUE NOT NULL,
            name VARCHAR(100) NOT NULL,
            created_at TIMESTAMP WITH TIME ZONE DEFAULT CURRENT_TIMESTAMP,
            updated_at TIMESTAMP WITH TIME ZONE DEFAULT CURRENT_TIMESTAMP
        );
        ```

7. Generate the application key:

    ```
    php artisan key:generate
    ```

8. Run database migrations:

    ```
    php artisan migrate
    ```

9. Start the development servers:
    - For Laravel:
        ```
        php artisan serve
        ```
    - For React:
        ```
        pnpm dev
        ```

## Usage

After completing the installation steps, you can access the application by navigating to the URL provided by the Laravel development server (typically `http://localhost:8000`).

Using the main navigation, move between the different pages of the app. The "Home" and "About" pages are static, while the "Users" page allows you to send and retrieve data from the database.

## License

MIT License
