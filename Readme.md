# uBrokeNews 

A Full-Stack application that provides trustworthy and timely news from a wide range of sources with no reading restrictions. 

## Features

- Create an account, login and logout
- Unauthorized access to news with categories
- Users with profiles can follow news sources and categories
- Custom user feed
- Ability to like and save articles
- Search for articles

The application has been deployed and can be accessed from **http://54.158.160.72**

## Getting Started

### Requirements

- Docker 
  - https://docs.docker.com/get-docker/ 
  - ```bash
    sudo snap install docker 
    ```

### Installation

1. Clone the repository with submodules:
   ```bash
   git clone --recurse-submodules https://github.com/yaraya24/uBrokeNews.git
   ```

2. Edit the .env file in `uBrokeNews/backend/news_app_project/.env`
   - If the DATABASE_USER and DATABASE_PASSWORD are changed, the docker-compose.yml file needs to reflect the change
   - Update allowed hosts parameter if not being deployed on localhost
   - Ensure you change the Secret Key 

3. Build and run the application:
   ```bash
   docker-compose up -d --build
   ```
   
   **Note:** Wait up to 2 minutes for the application to obtain the articles.

You can now access the web application on localhost on port 80 or via the public IPv4 address.

## API Endpoints

| Description | Endpoint |
|-------------|----------|
| All articles that are considered headlines | `/api/v1/` |
| Sports Articles | `/api/v1/sports` |
| Business Articles | `/api/v1/business` |
| Culture Articles | `/api/v1/culture` |
| Technology Articles | `/api/v1/technology` |
| Search Endpoint | `/api/v1/search` |
| Saved Articles | `/api/v1/saved` |
| Custom User Feed | `/api/v1/myfeed` |
| Details on specific article | `/api/v1/<id>` |
| Profile page for authenticated user | `/api/v1/profile` |