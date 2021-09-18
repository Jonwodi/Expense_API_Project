# Python django rest framework API instructions and guidance

#===========================================================

Create a main project folder and cd into your main project folder using your command line terminal. Open the main project folder in vs code using "code ." while still in your command line terminal. Then enter "pipenv shell" in your vs code terminal to create a virtual environment.

#===============================================================================

Copy pipefile packages such as django, isort flake8 etc. From previous python django projects into your current pipefile that was created when you created a virtual environment. Then enter "pipenv install --dev", into your vs code terminal to install the packages you copied into your pipefile.

#===============================================================================

Then inside your vs code code terminal enter "django-admin startproject project .". To create a project folder that is below or within your main project folder.
Then while you're still inside your vs code terminal, enter "django-admin startapp app_name" or python manage.py startapp app_name". To create a app folder for your project. The app can be named anything you want e.g. "python manage.py expense_api".

#===============================================================================

Then go into your project folder and open settings.py. Once you're inside the setting.py file add the following:

['app_name', or in this example 'expense_api',
'rest_framework',
'rest_framework_api_key',]

inside the INSTALLED_APPS array (list).

#===============================================================================

Create a .gitignore file in the main project folder. Then copy and paste the following:

.vscode
.idea/
**pycache**/
\*.sqlite3

into the .gitignore file.

#===============================================================================

Then go into project folder and then find and open the urls.py file. Add the following urls path:

'path("", include(("app_name.urls", "app_name"), namespace="app_name")),'

into the urlpatterns list (array). Also make sure add 'include' to django.urls import. So, it should look like this:

'from django.urls import path, include'

#===============================================================================

Go into your app folder and create urls.py file that is within or under your app folder. Open the urls.py file that is inside your app folder and add the following:

'from django.urls import path'

Also create an empty list (array), with the variable name urlpatterns, basically the same variable name used inside the urls.py file that is inside your project folder.

#===============================================================================

Then go into your models.py file which is inside your app folder. Then create the required fields for your models and database. Then use 'python manage.py makemigrations' followed by 'python manage.py migrate' to run migrations and to record the data into the database.

#===============================================================================

Go to your app folder and open the tests.py file which is inside your app folder. Create your tests. Also make sure to import 'APIClient' from the django rest framework. Your import should look like this:

'from rest_framework.test import APIClient'

#===============================================================================

Then whilst still in your tests.py file import 'reverse' from django.urls and status from django rest frameworks. Your imports should look like this:

'from rest_framework.test import APIClient'
'from rest_framework import status'

#===============================================================================

Then go into your urls.py file inside your app folder and create your urls using the variable name urlpatterns which will be a list (array) that contains your urls path and also include the following import:

'from . import views'

#===============================================================================

Then go into your views.py file which is inside or under your app folder. Create your views. Then import 'APIView' from the django rest framework and import your 'Serializer' from serializers.py file which is a file that will also be in your app folder once it's created. The imports should look like this:

'from rest_framework.views import APIView'

'from .serializers import ExpenseSerializer'

#===============================================================================

Also, inside your views.py file make sure to include the following imports, 'status' and 'Response', which are both from django rest framework. The imports should look like this:

'from rest_framework.response import Response'

'from rest_framework import status'

#===============================================================================

Create a serializers.py file inside or underneath your app folder. Then create your serializers for your app. Then import 'serializers' from django rest framework and also import your 'classModel' from your models.py file which is also in your app folder. The import should look like this:

'from rest_framework import serializers'

'from .models import classModel'

#===============================================================================
