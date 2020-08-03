- runserver on 0.0.0.0 interface (localhost remains in container)
- Add 0.0.0.0 and docker-machine ip to settings
ALLOWED_HOSTS = ['0.0.0.0', '192.168.99.100']
- A project can contain multiple apps. An app can be in multiple projects.
- The URLconf matches a request's url (no domain name, no GET/POST parameters) to urlpatterns and then calls the view function. The request is given as argument to it, with parameters as keyword arguments.
- SQLite is enough for the tutorial, but should be replaced for production environments and larger projects (install bindings and configure database permisions and tables).
- Use UTC in the code and use local time only when interacting with end users: https://docs.djangoproject.com/en/3.0/topics/i18n/timezones/#:~:text=The%20solution%20to%20this%20problem,installed%20when%20you%20install%20Django.
- Time zones values are not UTC+-xy:wz https://stackoverflow.com/a/29311392/4281529
- Database migration creates necessary tables for each entry of INSTALLED_APPS
- Create docker image with database utilities, e.g. sqlite3
- To change models:
  1. Change models in models.py
  2. Create migrations for the models with python manage.py makemigrations
  3. Apply changes to database (migrate) with python manage.py migrate
- Django provides a database API for
  - Creation (insertion)
  - Filtering (querying)
  - Indexing
  - Deletion
  - Relation management
- Django sets up an admin site by default
  - Create users with python manage.py createsuperuser
  - Can be translated with LANGUAGE_CODE setting
  - Models need to be registered in their admin.py to appear here
  - We can edit a model's fields from here
  - We can look at the history of changes
