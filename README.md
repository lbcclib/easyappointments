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

## Deploy

CircleCi builds the code as a tarball for every commit.  To deploy:

    wget https://path-to-build.tar.gz
    tar xzvf build.tar.gz
    cp appointments.lbcc.linnlibraries.org/config.php build/config.php
    mv appointments.lbcc.linnlibraries.org old
    mv build appointments.lbcc.linnlibraries.org

If you ever wish to build manually, it's:

    npm run build


