# Python django rest framework API

#==================================

Create a project folder and cd into your project folder using your command line terminal. Open the project folder in vs code using "code ." while still in your command line terminal. Then enter "pipenv shell" in your vs code terminal to create a virtual environment.

#===============================================================================

Copy pipefile packages such as django, isort flake8 etc. From previous python django projects into your current pipefile that was created when you created a virtual environment. Then enter "pipenv install --dev", into your vs code terminal to install the packages you copied into your pipefile.

#===============================================================================

Then inside your vs code code terminal enter "django-admin startproject project .". To create a project folder that is below or within your main project folder.
Then while you're still inside your vs code terminal, enter "django-admin startapp app" or python manage.py startapp app". To create a app for your project. The app can be named anything you want e.g. "python manage.py startapp todo_app".

#===============================================================================

Then go into your project folder and open settings.py. Once you're inside the setting.py file add the following:

'expense_api',
'rest_framework',
'rest_framework_api_key',

inside the INSTALLED_APPS array (list).
