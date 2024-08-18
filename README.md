# ProjeQtOr

This project is building a docker image based on Apache/PHP8.1 as well as MySQL server. It will build and run two docker container for PHP and MySQL.
It will pull ProjeQtOr V11.3.1 from Sourceforge and build an image

## Installation
You just need to clone the repository, then add a mypass.env file while renaming the sample file and adjust the content with a more secure root password.
Next, you have to build and deploy the container.
Finish the ProjeQtOr setup and start with your first project

```bash
git clone https://github.com/chdrsto/projeqtor.git

## move to the config to enable the .env file with the MySQL credentials
cd config/
cp mypass.env.sample mypass.env
vi mypass.env

## Once the credentials have been changed, move to the main folder and trigger the build process
cd ../
docker compose build --no-cache # --no-cache will pull all files ignoring possibly existing cache files
```

## Usage

```bash
## To start the container, run ...:
docker compose up -d

## To stop a container, run ...:
docker compose down

```
Once the containers are up and running, open a Browser and call the ProjeQtOr landing page of your sever :  http://IP-address/projeqtor

You have to set the IP to the MySQL server and provide the root password which you've set in the mypass.env file and complete the setup.

The first login will trigger the ProjeQtOr update process.
Login as Admin using "admin/admin" for username and  password. Once complete, you can login using the same credentials again.

Change the admin password, setup a new Client, Users, and create a new Project

Enjoy.

## Contributing
Pull request are welcome. As this is my first Dockerfile, there might be a of things to be improved (see to be fixed section).

## To-Be fixed:
* Credenitals (root) for MySQL connections
* Dynamically download of the latest ProjeQtOr zipfile from Sourceforge
* Docker build process improvement
* etc.

## License
[MIT] (https://choosealicense.com/licenses/mit/)
