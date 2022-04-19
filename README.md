# Todo-list Project 

# In this project we have:
- Golang and `MUX` library as backend web api
- Mysql database 
- simple `index.html` and some css and js also ajax as frontent web ui.

# main.go
- Core of project. functions that use in apis like create, delete, update,etc.
- using `MUX` and `CORS` packages as web api and http request handler.
- `logrus` package for service logging.
- `GORM`, `mysql driver` and `dialect` Packages for connecting to mysql DB.
- after running and make connection with DB, you can use apis in `8000` port of ur localhost; or opennig `index.html` and use app with ui.

# Runnig Project
for database you can use a docker container and run it with this commands:
1. `docker run -d -p 3306:3306 --name=mysql -e 'MYSQL_ROOT_PASSWORD=root' mysql`
2. `docker exec -it mysql mysql -uroot -proot -e 'CREATE DATABASE todolist'`

first you should download and install packages w/ this command

3. `go mod tidy`


then run it (in project directory):

4. `go run .`

now our todo-list application server is runnig and you can see it in  `index.html` file.

# APIs
## GET methods
- `/healthz`: Check server is runnign healthy

- `/todo`: return all iterms 

- `/todo-completed`: return all completed items

- `/todo-incomplete`: return all incomplete items

## POST methods
- `/todo`: create an item

- `/todo/{id}`: toggle done or not of an item


## DELETE methods
- `/todo/{id}`: delete item with specefic id
