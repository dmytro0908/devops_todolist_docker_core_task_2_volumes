# Application Deployment Instructions

## 1. Run MySQL Container with Volume Attached
bash
docker volume create mysql_data
docker run -d --name mysql-db -v mysql_data:/var/lib/mysql -p 3306:3306 dmytro0908/mysql-local:1.0.0


## 2. Run Application Container Connected to MySQL
bash
docker run -d --name todoapp-container -p 8000:8000 dmytro0908/todoapp:2.0.0

## 3. Docker Hub Repository
- Application Repository: [https://hub.docker.com/r/dmytro0908/todoapp](https://hub.docker.com/r/dmytro0908/todoapp)

## 4. Access the Application via Browser
Open your browser and navigate to:
- Main Web Interface: [http://localhost:8000](http://localhost:8000)
- REST API: [http://localhost:8000/api/](http://localhost:8000/api/)