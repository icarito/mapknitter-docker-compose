# Containerized MapKnitter service

This service is configured to run with a MYSQL database, and use local file storage.

To run it, make sure your paths are correct (by default /srv/mapknitter\_priv1).
Run `git submodule init` to pull the mapknitter sources.
Also set up your database passwords in `database.yml`. 

Then run `docker-compose build`. It should download and build the MySQL container and build the Mapknitter container. You will need to run `docker-compose run web rake db:init` and `docker-compose run web rake assets:precompile` in order to set up the environment before the app is ready to work.

Finally, run `docker-compose up` and you'll have Mapknitter on localhost:3000 !
