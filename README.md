# django-basics
Treehouse Django Basics Course


1/ INSTALLATION

//Install django
sudo pip install django
sudo pip install djangorestframework

//Run server
python manage.py server 0.0.0.0:8000
//Migrate db
python manage.py migrate

2/ CREATE A HELLO WORLD VIEW

- Create views.py
- Add the HelloWorld view
- Import url

3/ CREATE AN APP

python manage.py startproject courses
- Add to settings

4/ ADD THE MODELS
- Create class Course(models.Model)...
- python manage.py makemigrations

5/ OPEN SHELL TO ADD OBJECTS

python manage.py shell
from courses.models import Course
Course.Objects.all()
Course(title="",description="").save()

- Add return self.title in the model to show the name in the shell

6/// CREATE VIEW FOR MODEL courses

- Define course_list in the views
- Create the url for courses
- Add that url in urls.py in web


7/// CREATE A SUPERUSER

python manage.py createsuperuser
url/admin/
Register Course model in admin.py -> admin.site.register(Course)


8/// TEMPLATES

Create forlder in courses and web
Add in the settings in TEMPLATES - DIR
Change the views to return with render function

9/// STATIC TEMPLATES

STATICFILES_DIRS is a setting for where to find static files. These files will either be served during development or will end up being collected by the collectstatic command during deployment.

staticfiles_urlpatterns() is a function that returns the URL patterns for static files based on DEBUG and a few other settings. You import it from django.contrib.staticfiles.urls.

{% load static from staticfiles %} - The way to import the {% static %} tag for use.

{% static "<path/to/asset>" %} - How to use the {% static %} tag to properly point to a static asset.
