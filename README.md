flask and gunicorn tutorial
===========================

The default development server for flask is not suited for production environments. Gunicorn is a simple WSGI client written in pure python. This repository serves as a simple example of connecting the two.

[This answer](https://serverfault.com/a/331263) on StackOverflow explains why something like Gunicorn is needed.

More on Gunicorn can be found [here](http://docs.gunicorn.org/en/latest/run.html)

Running flask server
====================

`export FLASK_APP="app.main:create_app"`

`flask run`

Running gunicorn server
=======================

gunicorn -w 4 --reload -b localhost:5000 "app.main:create_app(testing=True)" 
