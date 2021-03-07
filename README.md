## About

A slight fork of **Easy!Appointments** for use at Linn-Benton Community College Library.

## Setup

    git clone https://github.com/lbcclib/easyappointments.git
    cd easyappointments

## Pull in changes from upstream

    git fetch https://github.com/alextselegidis/easyappointments TAG_OR_COMMIT_ID
    git rebase FETCH_HEAD
    npm install && composer install


## Dev instance

Copy config-default.php to config.php, and replace the BASE_URL and DB_HOST lines accordingly:

    const BASE_URL      = 'http://localhost:8000';
    const DB_HOST       = 'mysql';


Then run `cd docker && docker-compose up -d`

## Make changes and build

    npm run build

Then, copy the build directory into place, maintaining the existing config.php

