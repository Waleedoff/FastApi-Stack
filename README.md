# Welcome to BackEnd Stack "python 'fastApi' "!



# Tech Stack Overview 


### Core Development Technologies


#### python  
```
python is a programming language that we use to build our backend services. It is a high-level, general-purpose programming language that is easy to use, easy to  
learn, and it comes with a large ecosystem of libraries and tools. We use Python because it is a powerful, flexible, and versatile language that is well-suited for  
building web applications.
```


#### FastApi
```
A modern, fast (high-performance)
 web framework for building APIs.
 It is easy to use, easy to learn, and it comes with great features
 such as automatic validation of  
 request data,
 automatic generation of API documentation, and more

```


#### SQLAlchemy
```
A popular ORM (Object-Relational Mapping) library for Python.
  It makes it easy to work with databases,
  and it provides a high-level,
  intuitive API for working with data.
```

#### Pytest

```
A powerful testing framework for Python.
 It makes it easy to write tests,
 and it provides powerful features such as fixtures,
 parameterized testing, and more.
```


##  Infrastructure



#### Docker
```
A set of platform as a service products that use OS-level 
  virtualization to deliver software in packages called containers.
  Containers are isolated from one another and  
  bundle their own software, libraries and configuration files.	
  They can communicate with each other through well-defined channels. 
  All containers are run by a single  
  operating-system kernel and are thus more lightweight than virtual machines
```

#### Docker Compose
```
A tool for defining and running multi-container Docker applications.
  It makes it easy to configure and run our services,
  and it provides a simple, intuitive API for  
  defining and running our services
```


## User Authentication and Authorization


#### Keyclock

```
An open-source identity and access management system
   that we use to manage authentication and authorization 
   for our services. It provides a powerful set of  
   features such as single sign-on, social login, and more.

```


#### Json Web Token

```
A compact, URL-safe means of representing claims to be transferred between two parties.
  The claims in a JWT are encoded as a JSON object that is digitally signed  
  using JSON Web Signature (JWS). JWTs can be signed using a secret (with the HMAC algorithm)
  or a public/private key pair using RSA

```


## Data Storage and ManagementData Storage and Management

#### PostgreSQL

```
A powerful, open-source object-relational database system that we use to store and manage our   data. It is a highly scalable, reliable, and robust database system that  
is well-suited for building web applications
```


#### Alembic

```
A lightweight database migration tool for Python.
  It makes it easy to manage database schema changes, 
  and it provides a simple, intuitive API for creating and  
  applying migrations

```


## Docker Installation on MacOS

Docker is a popular containerization technology that allows you to run applications in isolated environments. Installing Docker on your MacOS machine is a  
straightforward process that can be completed by following these steps:

* Visit the Docker website and download the latest version of Docker Desktop for MacOS
* Once the download is complete, double-click the .dmg file to start the installation process. 
	Follow the on-screen instructions to complete the installation.
* After installation, launch Docker Desktop from your Applications folder. 
  Docker should start and run in the background
* Verify that Docker is running by opening a terminal window and running the following command:
```
docker version
```

If Docker is running, you should see output similar to the following:

```
Client:  
Cloud integration: v1.0.29  
Version: 20.10.21  
API version: 1.41  
Go version: go1.18.7  
Git commit: baeda1f  
Built: Tue Oct 25 18:01:18 2022  
OS/Arch: darwin/arm64  
Context: default  
Experimental: true
```

* Congratulations! You now have Docker installed on your machine. To get started with Docker, you only need a text editor of your choice (VSCode is(VSCode is  
recommended)recommended) and some basic knowledge of Docker commands


## Docker Commands

The following are some of the most commonly used Docker commands:
```
  docker compose up  - Starts the Docker containers.
  docker compose run <container> <command>  - Runs a command in a Docker container. 
         We usually use this    command to run tests, linters, and other tools
  docker compose down  - Stops the Docker containers.  
  docker compose ps  - Lists the running Docker containers.  
  docker compose logs  - Displays the logs for the running Docker containers.  
  docker compose exec <container> <command>  - Executes a command in a running Docker    container
  docker compose exec <container> bash  - Opens a bash shell in a running Docker container. 
         We usually use    this command to run database migrations.
```

Starting a new task involves several steps to ensure that we are working with the most up-to-date information and are able to track our progress effectively. The  
following steps outline the process we follow.


- Read the task from JiraRead the task from Jira: Jira is our main project management tool. We use it to track bugs, new features, and other tasks. Whenever we start a new task, we  
first read the task description, requirements, and acceptance criteria from Jira.  
- Create a ticketCreate a ticket: Once we have read the task description, we create a new ticket in Jira to track our progress. This ticket is assigned a unique code that we use  
to name our git branch.  
- Update git cloneUpdate git clone: Before we start working on the task, we make sure that our git clone is up-to-date. This ensures that we have the latest code changes and are  
not working on an outdated version of the code.  
- Create a new branchCreate a new branch: We create a new git branch using the ticket code we obtained from Jira. This makes it easy to track our progress and keep our changes  
isolated from the main branch.  
- Start with the taskStart with the task: With the new branch created, we are ready to start working on the task. We follow the requirements and acceptance criteria listed in Jira to  
ensure that we are meeting the expectations of the task.


 By following these steps, we ensure that we are working with the most up-to-date information, are able to track our progress effectively, and are able to collaborate  
with other team members in a seamless manner.


## API

When working on a project, it is important to have a clear structure in place to keep things organized and easy to manage. In this guide, we'll be discussing the steps  
involved in creating a structured folder system for a project's API

Firstly, we start by creating folders and files as required. If necessary, these folders should be located in <platform-name>/app/api/<entity-name>  . It is  
important to ensure that the structure of the folder is consistent and easy to follow. The structure of the folder should consist of the following files - __init__.py  ,  
models.py  , routes.py  , schemas.py  and one folder named services.py

* "___init__.py - This file is used to initialize a package in Python. It is usually an empty file, but it is required in order to mark a directory as a Python package.
* models.py - This file contains our database models. 
                        It defines the structure of our database tables and the relationships between them. 
                        We use SQLAlchemy
* routes.py - This file contains each route of the entity. It defines the endpoints that are available for the API and the functions that will be executed when  
those endpoints are called. We use FastAPI to define our endpoints. Each endpoint is mapped to a function that executes the business logic for that endpoint.

* schema.py - This file is used for Pydantic models. It defines the structure of the data that will be sent and received by the API. We define the input and  
output schemas for our endpoints in this file.


* services.py    folder - This folder contains the business logic. It includes all the functions that handle the data processing and manipulation. We keep our  
business logic separate from the web framework code to keep the code modular and easy to test & debug.

So till this point of the process, we should have a folder structure that looks like this:

```
├── app  
│ ├── api  
│ │ ├── <entity-name>  
│ │ │ ├── __init__.py  
│ │ │ ├── models.py  
│ │ │ ├── routes.py  
│ │ │ ├── schemas.py  
│ │ │ └── services  
│ │ │ └── <service-name>.py

```


## Tests


* init.py  - This file is used to initialize a package in Python. It is usually an empty file, but it is required in order to mark a directory as a Python package.  
* conftest.py  - This file contains the fixtures that are used in the tests. It is used to define the test database and the test client.  
* data.py  - This file contains the most common test data that is used in the tests.  
* src/  folder - This folder contains the tests for the API. It includes all the tests for the API endpoints, and unit testing.  
* src/<entity-name>/  folder - This folder contains the tests for the entity.  
* src/<entity-name>/test_<feature-name>/  folder - This folder contains the tests for the feature. It includes all the tests for the feature endpoints, and  
unit testing.  
* src/<entity-name>/test_<feature-name>/fixtures.py  - This file contains the fixtures that are used in the tests for the feature.  
* src/<entity-name>/test_<feature-name>/test_endpoint.py  - This file contains the tests for the endpoint.  
* src/<entity-name>/test_<feature-name>/test_unit.py  - This file contains the unit tests for the feature.]


By the end of this whole process, we should have a folder structure that looks like this:


```
├── <platform-name>  
│ ├── app  
│ │ ├── api  
│ │ │ ├── <entity-name>  
│ │ │ │ ├── __init__.py  
│ │ │ │ ├── models.py  
│ │ │ │ ├── routes.py  
│ │ │ │ ├── schemas.py  
│ │ │ │ └── services  
│ │ │ │ └── <service-name>.py  
│ │ ├── testing  
│ │ │ ├── __init__.py  
│ │ │ ├── conftest.py  
│ │ │ ├── data.py  
│ │ │ └── src  
│ │ │ └── __init__.py  
│ │ │ └── <entity-name>  
│ │ │ └── test_<feature-name>  
│ │ │ ├── __init__.py  
│ │ │ ├── fixtures.py  
│ │ │ ├── test_endpoint.py  
│ │ │ └── test_unit.py
```


#  Example of a Simple Code
Here you will see how we are implement endpoint ---


### rouete.py file :

```
```
![alt text](https://i.ibb.co/tYfBx08/route.png
)


```

when you write a route you should be follow these steps:
1: write the prefix cuase you don't need to repeation the same path
2: send the schema in the body instead of model
3: the name of the service must be the same name of the route function
	just add underscore symbol after the name,  like in our 
    example(Create_StartuUP_)
```

### service.py file :

![alt text](https://i.ibb.co/YtMWdMb/service.png
)


```
	Here we wrote the service(Logic) to this endpoint
	and we sent the "CreateStartupRequest" instead of model
	
	
```



### schema.py file :

![alt text](https://i.ibb.co/4PF0P4Y/schema.png
)

```
Here you see schema file 
we wrote schema and validation comes with pydantic 
 
and when we created the starup compan we don't write id in the request
but when it responsed "CreatedStartupResponse" we took the Startup_id 
```




### model.py file :

![alt text](https://i.ibb.co/LQPf4n3/model.png
)

```
Here model file 
these field as you know before the model gonna represented in our database.


```



### enum.py file :

![alt text](https://i.ibb.co/MCYxhBR/enums.png
)

```
Here enum file .
if you are looking at model you will find "Service" as field.
python enums used for represent data that represents a finite set of states

```








--------------------------

THANK YOU IN THE BELOW YOU WILL FIND SOME REFRENCES HELP YOU ...




 -------------------------------------


# How to use PostgreSQL database in FastAPI

* FOLLOW THESE STEPS: 
https://www.educative.io/answers/how-to-use-postgresql-database-in-fastapi



## Pydantic
```
Pydantic is a python library use to data parsing and validation.
Guarantees the types and constraints of the output model, to the input data.


```
![alt text](https://cdnb.artstation.com/p/media_assets/images/images/001/038/453/large/sc_03.jpg?1676661376)



# Here Another Example For Satr Platform Code.

* Suppose we need to implement delete_path endpoint and testing the endpoint.

model.py

![alt text](https://i.ibb.co/C0y6LKQ/model-Path.png)





route.py

![](https://i.ibb.co/wrLXH6S/route-Path.png)

service.py

![](https://i.ibb.co/CtngTsx/service-Path.png)


## testing the endpoint..



* First, create a fixture (setup).


![](https://i.ibb.co/Zd0653b/fixture.png)

* Second, create testendpoint file

![](https://i.ibb.co/0DytJn2/testendpoint.png)


* Third, check inside  the folder of this endpoint test must be inclucde __init__.py file to running the test
![](https://i.ibb.co/Qc7FMJB/init.png)











