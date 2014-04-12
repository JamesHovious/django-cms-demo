django CMS Demo
===============

A demo site that shows a simple django CMS setup. I've included the sqlite
database and some media into the project to make it easier to see how 
django CMS works.

Get the code and run the project locally.  Make sure to checkout the 
frontend editing feature and try to add some pages.

This demo assumes you know a bit about Django, Python, virtualenv, pip and that you
have Python, pip and virtualenv installed already.  Also, if you aren't using virtualenv
to pip install the requirements, shame on you.  But, it'll work
without it.


Installation (with included database)
-------------------------------------

::

    $ git clone git://github.com/andrewschoen/django-cms-demo.git
    $ cd django-cms-demo
    $ virtualenv env
    $ source env/bin/activate
    $ pip install -r requirements.txt
    $ python manage.py runserver


Installation (without included database)
----------------------------------------

::

    $ git clone git://github.com/andrewschoen/django-cms-demo.git
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

Customizing your configuration
------------------------------

To deploy with Heroku/Amazon S3 navigate to settings.py uncomment the below lines and fill them in with your relevant information.

::

    #import herokuify
    #CACHES = herokuify.get_cache_config()   # Memcache config for Memcache/MemCachier

    #COMPRESS_STORAGE = "herokuify.storage.CachedS3StaticStorage"
    #COMPRESS_OFFLINE = True
    #ROBOTS_CACHE_TIMEOUT = 60*60*24

    #To set up Amazon S3 media hosting just input your bucket information below

    #DEFAULT_FILE_STORAGE = 'storages.backends.s3boto.S3BotoStorage'
    #AWS_QUERYSTRING_AUTH = True
    #AWS_STORAGE_BUCKET_NAME = 'sample_bucket'
    #STATICFILES_STORAGE = 'storages.backends.s3boto.S3BotoStorage'
    #S3_URL = 'https://s3.amazonaws.com/sample_bucket/'

For more information on configuration see http://pythonhosted.org/django-herokuify/

Admin credentials
+++++++++++++++++

If you're using the included database, here are the admin credentials.

un: admin

pw: admin