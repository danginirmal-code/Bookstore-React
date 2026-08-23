


Demo: https://youtu.be/1HY2QJaXlsk
React + Django REST Framework

A full-stack web application built with React on the frontend and Django REST Framework (DRF) on the backend.

🚀 Tech Stack
Frontend
React
React Router
Axios
JavaScript / TypeScript
React Query
CSS / Tailwind CSS
shadcn
Backend
Python
Django
Django REST Framework
Django ORM
SQLite / PostgreSQL
📁 Project Structure
project-root/
├── backend/
│   ├── manage.py
│   ├── config/
│   │   ├── settings.py
│   │   ├── urls.py
│   │   ├── asgi.py
│   │   └── wsgi.py
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
│   └── src/
│       ├── components/
│       ├── pages/
│       ├── services/
│       ├── App.jsx
│       └── main.jsx
│
└── README.md

⚙️ Requirements

Make sure you have installed:

Python 3.10+
Node.js 18+
npm
Git
🔧 Backend Setup

Navigate to the backend directory:

cd backend


Create a virtual environment:

python -m venv venv


Activate it.

Windows
venv\Scripts\activate

macOS / Linux
source venv/bin/activate


Install dependencies:

pip install -r requirements.txt


Run migrations:

python manage.py migrate


Create a superuser:

python manage.py createsuperuser


Start the Django development server:

python manage.py runserver


The backend will be available at:

http://127.0.0.1:8000/


API endpoints can be accessed through:

http://127.0.0.1:8000/api/


Django admin:

http://127.0.0.1:8000/admin/

🎨 Frontend Setup

Open another terminal and navigate to the frontend:

cd frontend


Install dependencies:

npm install


Start the React development server:

npm run dev


The frontend will usually be available at:

http://localhost:5173/

🔗 API Configuration

Create an environment file in the frontend:

frontend/
└── .env


Add:

VITE_API_URL=http://127.0.0.1:8000/api


Example Axios configuration:

import axios from "axios";

const api = axios.create({
  baseURL: import.meta.env.VITE_API_URL,
});

export default api;

📡 Example API

A typical DRF endpoint might look like:

GET    /api/users/
POST   /api/users/
GET    /api/users/:id/
PUT    /api/users/:id/
DELETE /api/users/:id/


Example response:

{
  "id": 1,
  "username": "john",
  "email": "john@example.com"
}

🔐 Authentication

For authentication, this project can use:

Django session authentication
Token authentication
JWT authentication

For JWT, install:

pip install djangorestframework-simplejwt


Example Django configuration:

REST_FRAMEWORK = {
    "DEFAULT_AUTHENTICATION_CLASSES": (
        "rest_framework_simplejwt.authentication.JWTAuthentication",
    ),
}

🌐 CORS

Install django-cors-headers:

pip install django-cors-headers


Add it to INSTALLED_APPS:

INSTALLED_APPS = [
    # ...
    "corsheaders",
    "rest_framework",
]


Add middleware:

MIDDLEWARE = [
    "corsheaders.middleware.CorsMiddleware",
    # ...
]


For local development:

CORS_ALLOWED_ORIGINS = [
    "http://localhost:5173",
]

🧪 Testing
Backend
python manage.py test

Frontend
npm test

🏗️ Production Build

Build the React application:

cd frontend
npm run build


The production files will be generated in:

frontend/dist/


For production deployment, use a production WSGI/ASGI server such as Gunicorn/Uvicorn and serve the React build using your preferred web server or hosting platform.

🔒 Environment Variables

Do not commit secrets to Git.

Example backend .env:

DEBUG=True
SECRET_KEY=your-secret-key
DATABASE_URL=your-database-url


Example frontend .env:

VITE_API_URL=http://127.0.0.1:8000/api


Add environment files to .gitignore:

.env
.env.*
venv/
__pycache__/
node_modules/
dist/
*.pyc

📜 Common Commands
Django
python manage.py runserver
python manage.py makemigrations
python manage.py migrate
python manage.py createsuperuser
python manage.py test

React
npm install
npm run dev
npm run build
npm run preview

🤝 Contributing
Fork the repository.
Create a feature branch:
git checkout -b feature/my-feature

Make your changes.
Commit your changes:
git commit -m "Add my feature"

Push the branch:
git push origin feature/my-feature

Open a Pull Request.
📄 License

This project is licensed under the MIT License.

👨‍💻 Author

Your Name

Replace this section with your name, GitHub profile, and contact information.
