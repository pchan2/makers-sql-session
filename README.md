# Extend a database-backed web application

## Setup

First of all, to get everything set up

- Fork this repo to your GitHub account
- Clone your forked repo to your machine
- `cd` into the directory and install the dependencies by doing `bundle`
- Set up the database by doing `rake setup`
- Seed the database with records by doing `rake seed_db`
- Start the server by doing `rackup`
- Explore the app in your browser!

## The challenge

1. Open `country_data.rb` in your text editor.  This is the only file you need to edit.
2. Read the code in the first three methods `.all`, `.european_countries` and `.all_data_sorted_by_population_increasing_order`
3. Note down anything you don't understand and investigate what's going on.  You could use some of your debugging tools here.
4. Find the empty methods and add code to perform the queries described (by the names of the methods).  Don't worry about testing this time – focus on implementing the DB queries.

## Resources
[https://stackoverflow.com/questions/19262312/rails-installing-pg-gem-on-os-x-failure-to-build-native-extension](https://stackoverflow.com/questions/19262312/rails-installing-pg-gem-on-os-x-failure-to-build-native-extension)
1. Error installing pg:         ERROR: Failed to build gem native extension.
  1. brew update
  2. brew install postgresql
  3. bundle or gem install pg

[https://stackoverflow.com/questions/13410686/postgres-could-not-connect-to-server](https://stackoverflow.com/questions/13410686/postgres-could-not-connect-to-server)
2. rake aborted! PG::ConnectionBad: connection to server on socket "/tmp/.s.PGSQL.5432" failed: FATAL:  database "patrickchan" does not exist
  1. postgres -D /usr/local/var/postgres -- it will give you a much more verbose output if postgres fails to start.
  2. Run initdb or pg_basebackup to initialize a PostgreSQL data directory.
  3. no use...
