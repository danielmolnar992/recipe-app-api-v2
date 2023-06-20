# recipe-app-api-v2

Recipe API project with Docker<br>

## Stack:

- Python 3.9
- Postgres 13
- Docker
- Django 4 framework
- DRF Spectecular to create swagger and documentation
- Flake8, isort for linting support
- Github Actions for testing and linting checks


## Usage:

Run `docker-compose up`
Swagger on: 127.0.0.1:8000/api/docs

1. Create a user: /api/user/create/
2. Request token with email and password: /api/user/token/
3. Use the Authorization menu on the top right and select tokenAuth as "Token <your_token>"
4. Create recipes with ingredients and add tags
5. Update and delete them as you wish (You can't create them separately, only delete and update (put or patch))
6. Upload images to recipes

To create superuser: `docker-compose run --rm app sh -c "python manage.py createsuperuser"`
Exit and run `docker-compose down -v`
Run tests with: `docker-compose run --rm app sh -c "python manage.py test && flake8"`
Run isort command: `docker-compose run --rm app sh -c "isort . --lai 2"`
