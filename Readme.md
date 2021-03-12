# uBrokeNews 

A Full-Stack application that provides trustworthy and timely news from a wide range of sources that with no reading restrictions. 

- Create an account, login and logout
- Unauthorized access to news with categories
- Users with profiles can follow News sources and categories
- Custom user feed
- Ability to like and save articles
- Search for articles



### Getting Started

**Requirements:**

- Docker 

  - https://docs.docker.com/get-docker/ 

  - ```
    sudo snap install docker 
    ```

**Installation:**

```
git clone --recurse-submodules https://github.com/yaraya24/uBrokeNews.git
```

Edit the .env file in uBrokeNews/backend/news_app_project/.env

* If the DATABASE USER and DATABASE_PASSWORD are changed, the docker-compose.yml file needs to reflect the change

* Update allowed hosts parameter if is not being deployed in the localhost
* Ensure you change the Secret Key 

```
docker-compose up -d --build

* Wait up to 2 minutes for the application to obtain the articles
```

You can now access the web application on the localhost on port 80 or via the public IPv4 address.

The application has been deployed and can be accessed from **http://54.158.160.72**



### API Endpoints:

All articles that are considered headlines: */api/v1/* 

Sports Articles: */api/v1/sports* 

Business Articles: */api/v1/business*

Culture Articles: */api/v1/culture*

Technology Articles: */api/v1/technology*

Search Endpoint: */api/v1/search*

Saved Articles: */api/v1/saved*

Custom User Feed: *api/v1/myfeed*

Details on specific article: *api/v1/<id>*

Profile page for authenticated user: *aip/v1/profile*



