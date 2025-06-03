## run MySQL container with a volume attached:

docker run -d --name mysql-container -v mysql_data:/var/lib/mysql -e MYSQL_ROOT_PASSWORD=1234 -e MYSQL_DATABASE=app_db -e MYSQL_USER=app_user -e MYSQL_PASSWORD=1234 -p 3306:3306 mysql-local:1.0.0

## run an App container which will connect to a MySQL db container:

docker run -d --name todoapp-container -p 8000:8000 todoapp:2.0.0

## link to my personal docker hub repository win an app image:

docker pull konstant1nou77/mysql-local:1.0.0
docker pull konstant1nou77/todoapp:2.0.0

##  how to access the application via a browser:

Open your browser and go to http://localhost:8080