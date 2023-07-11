# Quiz Game
---
##### Here you can answer for a few questions and get some points 
## Few simple steps to install this project
---

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
cd hw_quiz
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
PG_HOST=127.0.0.1
PG_PORT=5436
PG_USER=app
PG_PASSWORD=123
PG_DBNAME=quiz_db
```

## Everything is ready to run the project. Do command:
```
python3 main.py
```