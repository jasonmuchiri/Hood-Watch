# Hood-Watch

#### A web app that keeps track of what is happening in your neighborhood 

## Description 

This is a web application that allows you to be in the loop about everything happening in your neighborhood. From contact information of different handyman to meeting announcements or even alerts.


### User Story

To view the user story, open the specs.md file.

## Author

> _[Jason Muchiri](https://github.com/jasonmuchiri)_

## Set up instructions and installations

### Prerequisites

- python3.6 

- python virtual environment ~ to create one run the following command `python3.6 -m venv --without-pip virtual`

- python pip ~ to install pip activate virtual environment `source virtual/bin/activate` then run `curl https://bootstrap.pypa.io/get-pip.py | python`

- Postgres ~ to install follow the following commands in your home directory:
    - `sudo apt-get update`
    - `sudo apt-get install postgresql postgresql-contrib libpq-dev`
    - `sudo service postgresql start`
    - `sudo -u postgres createuser --superuser $USER`
    - `sudo -u postgres createdb $USER`
    - `touch .psql_history`

### Installation instructions

- Clone the repo ~ `git clone https://github.com/jasonmuchiri/Hood-Watch.git` && `cd Neighbourhood`

- Activate virtual environment: 
   `python3.6 -m venv --without-pip virtual` then `source virtual/bin/activate`

- Install all the dependancies in the requirements.txt file to get a development env running
   `pip3 install -r requirements.txt`

- Create a database 
  ```bash
  psqlpip install psycopg2
  CREATE DATABASE hood;
  ```

- Create .env file and paste the following filing where appropriate:
  ```python
  SECRET_KEY = '<Secret_key>'
  DBNAME = '<dbname>'
  USER = '<Username>'
  PASSWORD = '<password>'
  DEBUG = True

  EMAIL_USE_TLS = True
  EMAIL_HOST = 'smtp.gmail.com'
  EMAIL_PORT = 587
  EMAIL_HOST_USER = '<your-email>'
  EMAIL_HOST_PASSWORD = '<your-password>'
  ```

- Run initial migration
  ``` bash
  python3.6 manage.py makemigrations neighbourhood
  python3.6 manage.py migrate
  ```

- Run the app

   - `python3.6 manage.py runserver`

- Open the `localhost:8000` to check if the app is running successfully.

### Dependancies

All the project's dependancies are found in the requirements.txt file.Open it for reference.

## Known bugs

Some functionality not fully implemented

## Technologies used

    - python3.6
    - Django1.11
    - HTML
    - CSS
    - Bootstrap
    - Postgresql

## Live link in heroku

> 

## Contacts

For help and support feel free to contact me :
> _jasonmkinyua@gmail.com_

## License

> MIT License

> Copyright (c) 2019 _cooldragon_