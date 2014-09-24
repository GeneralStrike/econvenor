# eConvenor

[eConvenor](https://www.econvenor.org) is a Django web application which helps people convene a group more effectively.

## Installation for local testing or development

1. Clone the eConvenor Github repository: `git clone https://github.com/econvenor/econvenor.git`
1. Set up a new virtual environment using virtualenv: `mkvirtualenv development`
    - You need to have `virtualenv` and `virtualenvwrapper` to do this.
    - You can install them with: `sudo pip install virtualenv virtualenvwrapper`
1. Install requirements.txt: `pip install -r requirements.txt`
    - If this fails, do `sudo apt-get install python-dev postgresql libpq-dev` then try again.
1. Set these environment variables in your `.bashrc` (DO NOT use these values for PRODUCTION):
    - ECONVENOR_ADMIN_URL=administration
    - ECONVENOR_DATABASE_NAME=econvenor_database
    - ECONVENOR_DATABASE_PASSWORD=ncds8rbce7
    - ECONVENOR_DATABASE_USER=eonvenor_database_owner
    - ECONVENOR_EMAIL_PASSWORD=no_email_password
    - ECONVENOR_EMAIL_PORT=no_port
    - ECONVENOR_ENVIRONMENT=development
    - ECONVENOR_SECRET_KEY=13480dj3io12nrb4786ydge76gq78yd3b
1. Set up a local database: `manage.py syncdb`
    - During this process, set up a superuser with account name `superuser`, email `superuser@econvenor.org` and password `superuser`.
1. Migrate the database: `manage.py migrate`
1. Load test data from fixtures: `manage.py loaddata testdata`
    - This sets up a user with email `ash@econvenor.org` and password `ashanderson1!` and populates that account with test data.
1. Start the local server: `manage.py runserver` 
1. Point your browser to `localhost:8000` and sign in as `ash@econvenor.org`.

## Issue tracker

eConvenor's issue tracker is at [https://trac.econvenor.org](https://trac.econvenor.org)
