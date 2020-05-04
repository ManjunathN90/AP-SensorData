# AP-SensorData
An application to record incoming sensor data to screen and analyse stored data with basic statistics, table and chart view.

## Prerequisites
Install recent version of node, python and postgres. Make sure one has the compatible versions of following
```
1. npm@6.14.4
2. python 3.8.2
3. postgres 12
```
### Folder Structure
1. frontend/ (Where front end code of the application resides)
2. sensorData/ (where back end APIs of the application resides)

### Database setup (Postgres)
1. Password for postgres would be 1234.
2. Create an empty databse named 'sensor-DB' in postgres.
we are good to go.

### Kindly follow the following steps in order:
1. Create a virtual environment in the folder one above this file was cloned for example xyz folder ex: xyz/AP-SensorData. Then activate the vitual environment.
2. Change directory to frontend folder example xyz/AP-SensorData/frontend. Then run following commands one by one
```
   - npm install
   - npm run build
 ```
3. Change back to backend folder i.e sensorData xyz/AP-SensorData/sensorData. Then run following commands one by one
```
   - pip install -r requirements.txt
   - python manage.py makemigrations
   - python manage.py migrate
   - python manage.py runserver
```
4. Since the application is running on localhost:8000 we can launch that on browser with link http://127.0.0.1:8000
5.At this point of time, we should see the home page of the application. 

## About the application

### Objective
Objective of the application was to store incoming sensor data at certain intervals and to retrieve stored data with filter parameters like date range along with a sensor type giving basic statistics for the selected sensor type and date range along with table and chart view.

### Assumptions
To mock the above mentioned requirement of recording incoming sensor data few assumptions have been made for demo purpose.
1. A button "RECORD SENSOR DATA" has been provided to trigger incoming of sensor data.
2. once the above action is triggered, 30 sensor data samples at interval of 0.5 seconds with reading(0-100), ordered date timestamp(starting 2008) and sensor type category["Temperature","Wind", "Humidity"] will be send to backend Create API to store to DB.









