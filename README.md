


Demo: https://youtu.be/1HY2QJaXlsk

🚀 React + Django REST Framework

A modern full-stack web application built with React on the frontend and Django REST Framework (DRF) on the backend.

The project combines a responsive React UI with a powerful REST API, database management through Django ORM, and modern frontend tools for efficient data fetching and UI development.

🎥 Demo

▶️ Watch the project demo on YouTube

✨ Features
⚛️ Modern React frontend
🎨 Responsive UI with Tailwind CSS
🧩 Reusable components with shadcn/ui
🔄 Server-state management with React Query
🌐 RESTful API powered by Django REST Framework
🗄️ Django ORM for database operations
🔐 Authentication support
🔑 JWT authentication support
🔗 Axios API integration
🌍 CORS configuration
🧪 Backend and frontend testing
📦 Production-ready React build
🐘 PostgreSQL / SQLite database support
🛠️ Tech Stack
Frontend
Technology	Purpose
React	Frontend UI
React Router	Client-side routing
Axios	API requests
React Query	Server-state management
Tailwind CSS	Styling
shadcn/ui	UI components
JavaScript / TypeScript	Application development
Backend
Technology	Purpose
Python	Backend programming language
Django	Web framework
Django REST Framework	REST API
Django ORM	Database management
SQLite	Development database
PostgreSQL	Production database
📁 Project Structure
project-root/
│
├── backend/
│   ├── manage.py
│   │
│   ├── config/
│   │   ├── settings.py
│   │   ├── urls.py
│   │   ├── asgi.py
│   │   └── wsgi.py
│   │
│   └── apps/
│       └── api/
│           ├── models.py
│           ├── serializers.py
│           ├── views.py
│           ├── urls.py
│           └── migrations/
│
├── frontend/
│   ├── package.json
│   ├── public/
│   │
│   └── src/
│       ├── components/
│       ├── pages/
│       ├── services/
│       ├── App.jsx
│       └── main.jsx
│
└── README.md

⚙️ Requirements

Before running the project, make sure you have the following installed:

🐍 Python 3.10+
🟢 Node.js 18+
📦 npm
🔧 Git
🔧 Backend Setup
1. Clone the repository
git clone https://github.com/your-username/your-repository.git
cd your-repository

2. Navigate to the backend
cd backend

3. Create a virtual environment
python -m venv venv

Windows
venv\Scripts\activate

macOS / Linux
source venv/bin/activate

4. Install dependencies
pip install -r requirements.txt

5. Run database migrations
python manage.py migrate

6. Create a superuser
python manage.py createsuperuser

7. Start the Django server
python manage.py runserver


The backend will be available at:

http://127.0.0.1:8000/

Django Admin
http://127.0.0.1:8000/admin/

API
http://127.0.0.1:8000/api/

🎨 Frontend Setup

Open a new terminal and navigate to the frontend:

cd frontend

1. Install dependencies
npm install

2. Start the development server
npm run dev


The frontend will be available at:

http://localhost:5173/

🔗 API Configuration

Create a .env file inside the frontend directory:

frontend/
└── .env


Add the following:

VITE_API_URL=http://127.0.0.1:8000/api

Axios Configuration

Example API client:

import axios from "axios";

const api = axios.create({
  baseURL: import.meta.env.VITE_API_URL,
});

export default api;


You can then use this API client throughout your React application.

📡 REST API

The backend exposes RESTful API endpoints through Django REST Framework.

Example Endpoints
Method	Endpoint	Description
GET	/api/users/	Get all users
POST	/api/users/	Create a user
GET	/api/users/:id/	Get a user
PUT	/api/users/:id/	Update a user
DELETE	/api/users/:id/	Delete a user
Example Response
{
  "id": 1,
  "username": "john",
  "email": "john@example.com"
}

🔐 Authentication

The project can support multiple authentication methods:

Django Session Authentication
Token Authentication
JWT Authentication
JWT Authentication

Install Simple JWT:

pip install djangorestframework-simplejwt


Add JWT authentication to your Django REST Framework configuration:

REST_FRAMEWORK = {
    "DEFAULT_AUTHENTICATION_CLASSES": (
        "rest_framework_simplejwt.authentication.JWTAuthentication",
    ),
}

🌐 CORS Configuration

Install django-cors-headers:

pip install django-cors-headers


Add it to INSTALLED_APPS:

INSTALLED_APPS = [
    # ...
    "corsheaders",
    "rest_framework",
]


Add the middleware:

MIDDLEWARE = [
    "corsheaders.middleware.CorsMiddleware",
    # ...
]


For local development:

CORS_ALLOWED_ORIGINS = [
    "http://localhost:5173",
]


⚠️ For production, configure CORS with your actual frontend domain instead of allowing development origins.

🧪 Testing
Backend

Run Django tests:

python manage.py test

Frontend

Run frontend tests:

npm test

🏗️ Production Build

Build the React application:

cd frontend
npm run build


The production build will be generated in:

frontend/dist/


For production deployment, the Django application can be served using a production WSGI/ASGI server such as Gunicorn or Uvicorn.

The React application can be deployed to a static hosting platform or served through a web server such as Nginx.

🔒 Environment Variables

Never commit sensitive environment variables or secrets to Git.

Backend .env
DEBUG=True
SECRET_KEY=your-secret-key
DATABASE_URL=your-database-url

Frontend .env
VITE_API_URL=http://127.0.0.1:8000/api


Add environment files and generated directories to .gitignore:

.env
.env.*
venv/
__pycache__/
node_modules/
dist/
*.pyc

📜 Useful Commands
Django
# Start development server
python manage.py runserver

# Create migrations
python manage.py makemigrations

# Apply migrations
python manage.py migrate

# Create admin user
python manage.py createsuperuser

# Run tests
python manage.py test

React
# Install dependencies
npm install

# Start development server
npm run dev

# Create production build
npm run build

# Preview production build
npm run preview

🤝 Contributing

Contributions are welcome! 🎉

Fork the repository.
Create a new feature branch:
git checkout -b feature/my-feature

Make your changes.
Commit your changes:
git commit -m "Add my feature"

Push your branch:
git push origin feature/my-feature

Open a Pull Request.

Please make sure your code follows the project's existing conventions and includes appropriate tests where necessary.

📄 License

This project is licensed under the MIT License.

👨‍💻 Author

Nirmal Dangi
⭐ Support

If you found this project useful, consider giving the repository a ⭐ star on GitHub.

Built with ❤️ using React + Django REST Framework.
