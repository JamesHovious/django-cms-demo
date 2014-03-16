django CMS Demo
===============

A demo site that shows a simple django CMS setup. I've included the sqlite
database and some media into the project to make it easier to see how 
django CMS works.

This project is a fork of https://github.com/andrewschoen/django-cms-demo. This demo
specifically is targeted for a Heroku development environment with a Postgresql database.

Get the code and run the project locally.  Make sure to checkout the 
frontend editing feature and try to add some pages.

This demo assumes you know a bit about Django, Python, virtualenv, pip and that you
have Python, pip and virtualenv installed already.  Also, if you aren't using virtualenv
to pip install the requirements, shame on you.  But, it'll work
without it.


Installation (with included database)
-------------------------------------

::

    $ git clone https://github.com/hoviousj/django-cms-demo.git
    $ cd django-cms-demo
    $ virtualenv env
    $ source env/bin/activate
    $ pip install -r requirements.txt
    $ python manage.py runserver


Installation (without included database)
----------------------------------------

::

    $ git clone https://github.com/hoviousj/django-cms-demo.git
    $ cd django-cms-demo
    $ virtualenv env
    $ source env/bin/activate
    $ pip install -r requirements.txt
    $ python manage.py syncdb --all
    $ python manage.py migrate --fake
    $ python manage.py runserver

Viewing the demo
----------------

Open the browser, navigate to http://localhost:8000

Login to the admin at http://localhost:8000/admin

Admin credentials
+++++++++++++++++

If you're using the included database, here are the admin credentials.

un: admin

pw: djangocms