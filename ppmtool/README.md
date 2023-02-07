# About

PPMTool stands for personal project management tool. This application is written using Spring boot 2.0 in the backend, ReactJS and Redux on the front end.

## Application architecture
<img src="https://github.com/vsushko/full-stack-projects/blob/master/img/ppmtool-architecture.png" width="792" height="824">

## Codebase
### Technologies

Architecture of this repo:
- **Full-stack JavaScript and Java:** The Java programming language is useed in the backend, and React on the frontend. Here is a lists of all the big technologies which is used:
- **Spring Boot:** Backend Java app
- **Flowtype**: Type-safe JavaScript
- **React:** Frontend React app
- **MySQL DB:** Data storage

### Folder structure
```sh
ppmtool/
├── public                    # Public files used on the frontend
├── ppmtool-react-client/src/ # Frontend SPA
├──── actions                 # Actions which would be dispatched on the store
├──── components              # App components
├──── reducers                # State changing functions
├──── securityUtils           # Security Utils
├── src/                      # Spring boot Java app
├──── domain                  # Domain objects
├──── exceptions              # App exceptions
├──── payload                 # DTOs
├──── repositories            # DAO interfaces for providing CRUD operations on database tables
├──── security                # JwtAuthentication
├──── services                # Business functionalities
├──── validator               # Bean Validations
├──── web                     # Controller classes for the request handling
├──── resources               # App resourcess
```

## Data
### List of entities:

- Backlog - describes backlog entity
- Project - describes project entity
- ProjectTask - describes project task entity
- User - describes user

#### project
| column  | description |
| ------------- | ------------- |
| id  | identifier |
| project_name | project name |
| project_leader | project leader |
| project_identifier | project identifier |
| description | project description |
| start_date | project starting date |
| end_date | projet end date |
| created_at | date when project task was created |
| updated_at | date when project task was updated |
| user_id | link to the related user |


#### backlog
| column  | description |
| ------------- | ------------- |
| id  | identifier |
| ptsequence | sequence of project tasks within each backlog |
| project_identifier | the same identifier as a project |
| project_id | link to the related project |

#### project_task
| column  | description |
| ------------- | ------------- |
| id | identifier |
| summary | header of project task |
| acceptance_criteria | user information |
| status | status for traversing of the board |
| priority | for grouping tasks |
| due_date | task due date |
| create_at | date when project task was created |
| update_at | date when project task was updated |
| project_identifier | store id here for persisting tasks related for specific backlog |
| project_sequence | projectIdentifier + 1 |
| backlog_id | link to related backlog |

#### user
| column  | description |
| ------------- | ------------- |
| id  | identifier |
| username | user name |
| full_name | user full name |
| password | user's password |
| create_at | date when user was created |
| update_at | date when user was updated |

### Entity–relationship model
<img src="https://github.com/vsushko/full-stack-projects/blob/master/img/ppmtool-er-model.png" width="800" height="600">

<!--We will build our REST APIs with Spring boot for CRUD operations
## Features

## Browser: Client interaction
## Internet
## Webserver
## Application Server
## Database Server

We will create our front end using ReactJS and Boostrap

And will use Redux and Thunk to manage the state of our application in the front-end

We will secure our application using JWT tokens


REST Architecture with support for mobile applications
All the relationships of data modeling
Development of user interface with JSP, JQuery, AJAX and JSON
Design, develop and unit test the presentation tier
Design, develop and unit test the business tier
Design, develop and unit test the data access tier
Design, develop and unit test the resource (entity) tier
Popular patterns and best practices writing a complete Spring and Hibernate based relational database driven Java web application
-->
