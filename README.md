# ProjeQtOr

This project is building a docker image based on Apache/PHP8.1 as well as MySQL server. It will build and run two docker container for PHP and MySQL.
It will pull ProjeQtOr V11.3.1 from Sourceforge and build an image

## Installation
You just need to clone the repository and add a mypass.env file including the database credentials. You just have to rename the sample file and adjust the content to a valid password.

Next, you build the docker image using docker compose command:
docker compose build --no-cache

Then, you start the container using following command:
docker compose up

Once the containers are up and running, open a Browser and call the ProjeQtOr page http://IP-address/projeqtor

You have to provide the root password from the mypass.env file and finish the setup.

Login as Admin using "admin/admin" username / password. This will run the system upgrade. Once finished, login using the same credentials again.

Setup the Client, Users, and create a new Project

Enjoy.
