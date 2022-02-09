Creating django in docker 

We can do this in two ways like, we can build the docker and then create django app in docker container(we can install django framework on docker), or we can create the django app and then create the docker container (dockerizing the django app).



Commands used for 1st method implementation(creating django in docker): (implemenattion is in dockerdjango folder)

After creating the Dockerfile, docker-compose.yml, requirements.txt, then execute the commands to run the django app in docker container.
sudo pip install docker-compose - We use this command to install docker-compose

sudo docker-compose run web django-admin startproject mysite . - This is used to create the project named mysite in docker container

sudo chown -R $USER:$USER . - This is used to change the permissions from root to user.

sudo docker-compose up - This is used to run the server

sudo docker ps - This is used to see the information about docker containers and information of docker images is also seen.

sudo docker exec dockerdjango_web_1 python manage.py startapp hello - This is used to create the app named hello inside the existing project using docker container.






Commands used for 2nd method implementation(dockerizing django):  (implemantation is in djangodocker folder)

After creating the Dockerfile, docker-compose.yml, requirements.txt, then execute the commands to run the django app in docker container.
sudo docker-compose build    - This will create the docker image

sudo docker-compose  up       -  This is used to run the server


