# About Django

**Date: June 9, 2016**

#### What is Django

Django is a web framework for Python. Django has its own templating and an ORM to help manage data to be used. It also follows a Model-View-Controller architecture.

#### Initializing Django

```
	django-admin startproject sitename
```

This command will create this directory for you, all for your disposal.

```
sitename/
	manage.py
	sitename/
		__init__.py
		settings.py
		urls.py
		wsgi.py
```

Then create your first app typing in this command.

```
	python manage.py startapp app_name
```

Final view of your directory will be this.

```
sitename/
		manage.py
		sitename/
				__init__.py
				settings.py
				urls.py
				wsgi.py
		app_name/
				__init__.py
				admin.py
				apps.py
				models.py
				tests.py
				views.py
				migrations/
						__init__.py
```

The file ```manage.py``` will be responsible in modifying your project in various ways.

#### Running Django

It is as easy as this.

```
	python manage.py runserver
```

#### Migrations

Migration is a tool that lets you set your schema easily given that the settings your database has already been set.

Let us tell Python that we have made changes to the specified app_name and we want it to reflect in our database.

```
	python manage.py makemigrations app_name
```

After informing Python, we apply those changes to the database

```
	python manage.py migrate
```

Your schema is ready afterwards.

#### Admin

One of the best features of Django is that it is able to seperate and distinguish public users from power users / administrators. With Django, we are able to do that and create a GUI to help us.

Let us create the Big Man by typing in the command below then type in the username (admin), email and password you'd like.

```
	python manage.py createsuperuser
```

When we run the server (``` python manage.py runserver```), just like that you are able to create a super user for your app in just a few clicks. Django even provides you with a GUI for the administrator of the application.

#### Django Templating

A sample Django template would look something like this.

```html
{% extends "base.html" %}

{% block title %} Articles for {{ year }}{% endblock %}

{% block content %}
<h1>Articles for {{ year }}</h1>

{% for article in article_list %}
    <p>{{ article.headline }}</p>
    <p>By {{ article.reporter.full_name }}</p>
    <p>Published {{ article.pub_date|date:"F j, Y" }}</p>
{% endfor %}
{% endblock %}
```

Taken directly from the [Django Project Docs](https://docs.djangoproject.com/en/1.9/intro/overview/)

#### Open Source

Yes! Django is definitely free! Just get Python then install Django. It's not that hard!

#### Why shouldn't I use Flask instead

Flask is a micro framework. Django is not. Basically, Django is a full packaged framework that will give you everything you want like ORM, migrations, templating and much more. Flask gives what you need to get you started.

#### References

The [Django Project Docs](https://docs.djangoproject.com/en/1.9/).

#### Author

Almer Mendoza
