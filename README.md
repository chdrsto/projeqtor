# ProjeQtOr

ProjectQtOr is a Browser based,  open source project management solution to manage and run all kind of projects. [HomePage of ProjeQtOr](https://www.projeqtor.org/en/)

This Github project is to build a docker image based on Apache/PHP8.1 and  MySQL to run ProjeQtOr in dockerized environment. 
It will pull ProjeQtOr V11.3.1 from Sourceforge

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

## To-Be fixed:
* Credenitals (root) for MySQL connections
* Dynamically download of the latest ProjeQtOr zipfile from Sourceforge
* Docker build process improvement
* etc.

## Contributing
Pull request are welcome. As this is my first Dockerfile, there might be a of things to be improved (see to be fixed section).

## License
[MIT](https://choosealicense.com/licenses/mit/)
