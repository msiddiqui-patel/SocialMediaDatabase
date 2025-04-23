# Database Project

This project consists of a React frontend and Flask backend application. Below are instructions for setting up and running both components.

## Prerequisites

- Node.js (v14 or higher)
- Python (v3.8 or higher)
- MySQL Server
- npm (Node Package Manager)
- pip (Python Package Manager)

## Project Structure

```
.
├── frontend/          # React frontend application
└── backend/          # Flask backend application
```

## Backend Setup

1. Navigate to the backend directory:
   ```bash
   cd backend
   ```

2. Create and activate a virtual environment:
   ```bash
   # On macOS/Linux
   python -m venv venv
   source venv/bin/activate

   # On Windows
   python -m venv venv
   .\venv\Scripts\activate
   ```

3. Install required Python packages:
   ```bash
   pip install flask flask-cors mysql-connector-python
   ```

4. Configure the database:
   - Open `config.py` and update the MySQL connection details:
     ```python
     MYSQL_HOST = 'localhost'
     MYSQL_USER = 'your_username'
     MYSQL_PASSWORD = 'your_password'
     MYSQL_DB = 'db_project'
     ```

5. Start the backend server:
   ```bash
   python app.py
   ```
   The backend will run on `http://localhost:5000`

## Frontend Setup

1. Navigate to the frontend directory:
   ```bash
   cd frontend
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Start the development server:
   ```bash
   npm start
   ```
   The frontend will run on `http://localhost:3000`

## Running the Application

1. Start the backend server first (follow Backend Setup steps 1-5)
2. In a new terminal, start the frontend server (follow Frontend Setup steps 1-3)
3. Open your browser and navigate to `http://localhost:3000`

## Development

- The frontend development server has hot-reloading enabled - any changes you make to the frontend code will automatically refresh the browser
- The backend server runs in debug mode - any changes to the backend code will automatically restart the server

## Troubleshooting

- If you encounter any issues with the backend, check that:
  - MySQL server is running
  - Database credentials in `config.py` are correct
  - All required Python packages are installed

- If you encounter any issues with the frontend, try:
  - Clearing the npm cache: `npm cache clean --force`
  - Deleting the `node_modules` folder and running `npm install` again
  - Checking the browser console for any error messages

## Contributing

1. Fork the repository
2. Create a new branch for your feature
3. Make your changes
4. Submit a pull request

## License

This project is licensed under the MIT License - see the LICENSE file for details 