# uBrokeNews 📰

A modern full-stack news web application built with React.js frontend and Django backend, containerized with Docker for easy deployment and development.

## 🚀 Features

- **Modern Web Interface**: Clean, responsive React.js frontend for browsing news
- **Robust Backend**: Django REST API for news management and administration
- **Database Storage**: PostgreSQL database for reliable data persistence
- **Containerized Architecture**: Docker Compose for seamless deployment
- **Admin Interface**: Django admin panel for content management
- **API Endpoints**: RESTful API for programmatic access to news data

## 🏗️ Architecture

This application follows a microservices architecture with the following components:

- **Frontend**: React.js application (port 80 via Nginx)
- **Backend**: Django web application (port 8000)
- **Database**: PostgreSQL 11
- **Web Server**: Nginx (reverse proxy and static file serving)

## 📋 Prerequisites

Before running this application, make sure you have the following installed:

- [Docker](https://docs.docker.com/get-docker/) (version 20.0+)
- [Docker Compose](https://docs.docker.com/compose/install/) (version 1.27+)
- [Git](https://git-scm.com/downloads)

## 🛠️ Installation & Setup

### 1. Clone the Repository

```bash
git clone https://github.com/yaraya24/uBrokeNews.git
cd uBrokeNews
```

### 2. Initialize Submodules

This project uses git submodules for the backend and frontend components:

```bash
git submodule init
git submodule update
```

### 3. Build and Run with Docker Compose

```bash
docker-compose up --build
```

This command will:
- Build the backend Django application
- Build the frontend React application
- Set up the PostgreSQL database
- Configure Nginx as a reverse proxy
- Start all services

### 4. Access the Application

Once all containers are running:

- **Main Application**: http://localhost
- **API Endpoints**: http://localhost/api/
- **Admin Interface**: http://localhost/admin/

## 🔧 Development Setup

### Running in Development Mode

For development, you might want to run services individually:

```bash
# Start only the database
docker-compose up db

# Run backend in development mode (if supported)
# See backend submodule documentation for details

# Run frontend in development mode (if supported)  
# See frontend submodule documentation for details
```

### Project Structure

```
uBrokeNews/
├── backend/                 # Django backend (git submodule)
├── frontend/                # React.js frontend (git submodule)
├── nginx/                   # Nginx configuration
│   └── default.conf
├── docker-compose.yml       # Docker Compose configuration
├── .gitmodules             # Git submodules configuration
└── README.md               # This file
```

## 📚 Usage

### Accessing News Content

1. Navigate to http://localhost in your web browser
2. Browse available news articles
3. Use the search and filtering features (if available)

### Administration

1. Access the admin interface at http://localhost/admin/
2. Log in with administrator credentials
3. Manage news articles, categories, and users
4. Configure application settings

### API Usage

The application provides RESTful API endpoints at `/api/`. Refer to the backend submodule documentation for detailed API documentation.

## 🐳 Docker Services

The application consists of three main Docker services:

- **`backend`**: Django application server
- **`db`**: PostgreSQL database
- **`nginx`**: Web server and reverse proxy

### Useful Docker Commands

```bash
# View running containers
docker-compose ps

# View logs
docker-compose logs

# Stop all services
docker-compose down

# Rebuild and restart
docker-compose up --build

# Run database migrations (if needed)
docker-compose exec backend python manage.py migrate

# Create superuser (if needed)
docker-compose exec backend python manage.py createsuperuser
```

## 🤝 Contributing

This project uses git submodules for the backend and frontend components. To contribute:

1. **For backend changes**: Contribute to the [news_web_application](https://github.com/yaraya24/news_web_application) repository
2. **For frontend changes**: Contribute to the [reactjs_news_app](https://github.com/yaraya24/reactjs_news_app) repository
3. **For infrastructure changes**: Contribute to this main repository

### Development Workflow

1. Fork the relevant repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## 📝 License

Please refer to the individual submodule repositories for licensing information.

## 🐛 Troubleshooting

### Common Issues

**Port Already in Use**
```bash
# Stop any services using port 80
sudo lsof -i :80
# Kill the process or use a different port
```

**Submodule Issues**
```bash
# Reset submodules
git submodule deinit --all
git submodule update --init --recursive
```

**Database Connection Issues**
```bash
# Restart the database container
docker-compose restart db
# Check database logs
docker-compose logs db
```

## 📞 Support

For issues related to:
- **Backend**: Report issues in the [news_web_application](https://github.com/yaraya24/news_web_application/issues) repository
- **Frontend**: Report issues in the [reactjs_news_app](https://github.com/yaraya24/reactjs_news_app/issues) repository  
- **Infrastructure/Docker**: Report issues in this repository

---

Made with ❤️ by [yaraya24](https://github.com/yaraya24)