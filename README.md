# api-quick-start

## by Farah Ailouti and Mohammad Ghzzawi

#### How to use your library (where applicable):
#### docker-compose up

* docker-compose run web python manage.py createsuperuser

* docker-compose run web python manage.py migrate

* docker-compose run web python manage.py makemigrations

* pip install djangorestframework
#
* docker-compose up --build
* docker-compose down
* docker-compose restart
* docker-compose run web python manage.py migrate
* docker-compose run web python manage.py collectstatic
#

Template Project for starting up CRUD API with Django Rest Framework

## Customization Steps

- DO NOT migrate yet
- add additional dependencies as needed
  - Re-export requirements.txt as needed
- change `things` folder to the app name of your choice
- Search through entire code base for `Thing`,`Things` and `things` to modify code to use your resource
  - `project/settings.py`
  - `project/urls.py`
  - App's files
    - `views.py`
    - `urls.py`
    - `admin.py`
    - `serializers.py`
    - `permissions.py`
- Update ThingModel with fields you need
  - Make sure to update other modules that would be affected by Model customizations. E.g. serializers, tests, etc.
- Rename `project/.env.sample` to `.env` and update as needed
- Run makemigrations and migrate commands
- Run `collectstatic` if needed.
- Optional: Update `api_tester.py`
