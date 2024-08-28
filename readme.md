# Vehicle Service System

A full-stack web application designed for managing vehicle repairs, components, and transactions. This project utilizes Django for the backend and React.js for the frontend, allowing users to manage vehicles, record issues, calculate costs, and visualize revenue trends.

## Table of Contents

1. [Project Overview](#project-overview)
2. [Tech Stack](#tech-stack)
3. [Setup Instructions](#setup-instructions)
   - [Backend Setup](#backend-setup)
   - [Frontend Setup](#frontend-setup)
4. [Usage](#usage)
   - [Backend](#backend)
   - [Frontend](#frontend)
5. [API Endpoints](#api-endpoints)
6. [Testing](#testing)
7. [License](#license)

## Project Overview

The Vehicle Service System application enables users to:

- Register and manage vehicle components with repair and purchase prices.
- Add and manage vehicles.
- Record issues for vehicles and specify whether repairs or new components are needed.
- Calculate the final price for services.
- Visualize daily, monthly, and yearly revenue data through responsive graphs.

## Tech Stack

- **Backend**: Django, Django REST Framework
- **Frontend**: React.js, Recharts
- **Database**: SQLite (default, can be configured to use PostgreSQL, MySQL, etc.)
- **Development Tools**: Django development server, npm/yarn for frontend

## Setup Instructions

### Backend Setup

1. **Clone the repository:**

   ```bash
   git clone https://github.com/your-username/vehicle-service-system.git
   cd vehicle-service-system
   ```

2. **Create and activate a virtual environment:**

   ```bash
   python -m venv venv
   source venv/bin/activate   # On Windows use: venv\Scripts\activate
   ```

3. **Install backend dependencies:**

   ```bash
   pip install -r requirements.txt
   ```

4. **Apply database migrations:**

   ```bash
   python manage.py migrate
   ```

5. **Create a superuser (optional, for Django admin access):**

   ```bash
   python manage.py createsuperuser
   ```

6. **Run the Django development server:**

   ```bash
   python manage.py runserver
   ```

   The backend will be available at `http://localhost:8000/`.

### Frontend Setup

1. **Navigate to the frontend directory:**

   ```bash
   cd frontend
   ```

2. **Install frontend dependencies:**

   ```bash
   npm install
   ```

   or if you use yarn:

   ```bash
   yarn install
   ```

3. **Start the React development server:**

   ```bash
   npm start
   ```

   or if you use yarn:

   ```bash
   yarn start
   ```

   The frontend will be available at `http://localhost:3000/`.

## Usage

### Backend

- Access the Django admin panel at `http://localhost:8000/admin/` to manage data.
- Use Django REST Framework's browsable API or tools like Postman to interact with API endpoints.

### Frontend

- The React application provides the user interface and will interact with the Django backend to display data and manage user interactions.

## API Endpoints

### Components

- **List all components**: `GET /api/components/`
- **Create a new component**: `POST /api/components/`
- **Retrieve a component**: `GET /api/components/{id}/`
- **Update a component**: `PUT /api/components/{id}/`
- **Delete a component**: `DELETE /api/components/{id}/`

### Vehicles

- **List all vehicles**: `GET /api/vehicles/`
- **Create a new vehicle**: `POST /api/vehicles/`
- **Retrieve a vehicle**: `GET /api/vehicles/{id}/`
- **Update a vehicle**: `PUT /api/vehicles/{id}/`
- **Delete a vehicle**: `DELETE /api/vehicles/{id}/`

### Issues

- **List all issues**: `GET /api/issues/`
- **Create a new issue**: `POST /api/issues/`
- **Retrieve an issue**: `GET /api/issues/{id}/`
- **Update an issue**: `PUT /api/issues/{id}/`
- **Delete an issue**: `DELETE /api/issues/{id}/`

### Transactions

- **List all transactions**: `GET /api/transactions/`
- **Create a new transaction**: `POST /api/transactions/`
- **Retrieve a transaction**: `GET /api/transactions/{id}/`
- **Update a transaction**: `PUT /api/transactions/{id}/`
- **Delete a transaction**: `DELETE /api/transactions/{id}/`

### Revenue Data

- **Get revenue data**: `GET /api/revenue-data/`
  - Returns daily, monthly, and yearly revenue data.

## Testing

To run backend tests:

1. **Run the tests:**

   ```bash
   python manage.py test
   ```

Make sure to write unit tests for models, views, and serializers to ensure the application's functionality.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.


### Notes

- **Replace `your-username`** with your GitHub username or the URL of your repository.
- **Ensure paths and commands** match your actual project setup.
- **Update the License section** if your project uses a different license or include a `LICENSE` file in your repository.

