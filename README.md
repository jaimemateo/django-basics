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
