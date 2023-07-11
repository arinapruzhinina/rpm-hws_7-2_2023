# HTTP cities serever
#### On this http server, you can POST/PUT/DELETE cities, and view hotels in different cities.

## Few simple steps to install this project

### 1. Do this command to clone my repo

```
git clone https://github.com/arinapruzhinina/rpm-hws_7-2_2023
```
```
cd rpm-hws_7-2_2023
```
```
git checkout pruzhinina
```
### 2. You need to move folder with name hw_http.

```
cd hw_http
```

### 3. You need to create a docker container. Follow this few steps.

```
chmod +x script.sh
```
```
./script.sh
```
### 4. Create .env file in this folder with this text.
```
PG_DBNAME=http_db
PG_HOST=127.0.0.1
PG_PORT=5442
PG_USER=app
PG_PASSWORD=123
RAPID_KEY=62105bc9d7msh30ca44972f28115p1d09a5jsn511d8e8915d5
```
### 5. __Now you should do this command to fill the database:__

```
python3 add_cities.py
```

## Everything is ready to run the project. Do command:
```
python3 main.py
```
## And click the link: http://127.0.0.1:8001

---
#### After this command you fill see the main page. You can choose which page to go to. 
---
### If you choose the page with name "cities", you will see different cities and some infromation about them, like country, local language and population. 

#### You can open Postman and try to do POST/PUT/DELETE requests. Folows this steps:

##### 1. To do POST you should:
* paste the url http://127.0.0.1:8001/cities
* in field "Headers" you should paste:
in field key paste: "Authorization",
in field value paste: "admin {537dc091-cbeb-4802-84f8-46f0ea57694c}"
* in field "Body" you must choose a raw(JSON) and paste json like that:
```
{
    "city": "some city", 
    "country": "some country"
}
```
##### It is necessary to fill field to do POST request. If you want, you can  past full request with language and population. Example:
```
{
    "city": "some city", 
    "country": "some country", 
    "language": "language",
    "population": 1000   
}

```
##### After this command you will see a url with city id. You can press ctrl and click to the link. You will see your city.
 
 ##### 2. To do PUT you should:
* paste the url http://127.0.0.1:8001/cities?id=
after "=" you must to paste city id, witch you want to update.
* in field "Headers" you should paste:
in field key paste: "Authorization",
in field value paste: "admin {537dc091-cbeb-4802-84f8-46f0ea57694c}"
* in field "Body" you must choose a raw(JSON) and paste json like that:
```
{
    "city": "some city", 
    "country": "some country", 
    "language": "language",
    "population": 1000   
}
```
In this field you should write changes, that you want to do.
##### After this command you will see an updated city.

##### 3. To do DELETE you should:
* paste the url http://127.0.0.1:8001/cities?id=
after "=" you must to paste city id, witch you want to update.
* in field "Headers" you should paste:
in field key paste: "Authorization",
in field value paste: "admin {537dc091-cbeb-4802-84f8-46f0ea57694c}"
---
### If you choose the page with name "hotels", you can find hotels in 3 cities (Irkutsk, Moscow and Sochi).
