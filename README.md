# API for yatube project

API app for yatube project using Django Rest Framework

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

### Prerequisites

1. Install git, docker and docker-compose
2. Clone repo
```
git clone https://github.com/OdintsovTim/infra_sp2
```

### Installing

Add .env to main folder by the following template:

```
DB_NAME=postgres
POSTGRES_USER=postgres
POSTGRES_PASSWORD='write your db password'
DB_HOST=db
DB_PORT=5432
```

## Deployment

Run containers with docker-compose
```
docker-compose up -d
```

Enter container
```
docker exec -it <CONTAINER ID> bash
```

Make migrations and create superuser
```
python manage.py makemigrations && python manage.py migrate && python manage.py createsuperuser
```

Add test data from fixtures.json if you need
```
python manage.py loaddata fixtures.json
```

## Built With

* [Docker](https://docs.docker.com/) - The web framework used
* [Django](https://docs.djangoproject.com/en/3.0/) - Dependency Management
* [Django Rest Framework](https://www.django-rest-framework.org/tutorial/quickstart/) - Used to generate RSS Feeds

## Authors

* **Timur Odintsov** - *Initial work* - [OdintsovTim](https://github.com/OdintsovTim)
