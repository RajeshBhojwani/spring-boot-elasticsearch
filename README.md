
# Overview
In this project, We will show the usage of ElasticsearchRepository and ElasticsearchTemplates.
This project uses Spring-data-elasticsearch and that is compatible with ElasticSearch 2.4.4 only.
Don't use ElasticSearch 5.x and above with spring-data-elasticsearch as it is not updated yet with latest version. 
If you want to use latest ElasticSearch 5.x then you need to directly use Spring with Transport or node client apis.
See dependencies details on this link -
https://github.com/spring-projects/spring-data-elasticsearch/wiki/Spring-Data-Elasticsearch---Spring-Boot---version-matrix

## Step 1 Download the code from github
```git clone https://github.com/RajeshBhojwani/spring-boot-elasticsearch.git ```

## Step 2 Build the project
```mvn clean install```

## Step 3 Launch the application
```java -jar target\elasticsearch-0.0.1-SNAPSHOT.jar```

## Step 4  Use Curl or Postman to test the REST apis created. 
UserController has api using ElasticsearchTemplate
UserRepositoryController has api using ElasticsearchRepository

## APIs for ElastisearchTemplate usage
1. POST call for creating new User-
http://localhost:8102/new

### JSON data
```
{
  "name": "Sumit",
   "userSettings": {
   	"gender" : "male",
   	"occupation" : "CA",
   	"hobby" : "chess"
   }
}
```

2. GET call for Retrieve all Users
http://localhost:8102/all

3. Add User setting entry by name
http://localhost:8102/settings/Deepika/hobby/poetry

For other apis, check code.

## APIs for ElasticsearchRepository usage

1. POST call for creating new User-
http://localhost:8102/repo/new
### JSON Data
```
{
  "name": "Deepika",
   "userSettings": {
   	"gender" : "Female",
   	"occupation" : "Software Engineer",
   	"hobby" : "racing"
   }
}
```

2. GET call for Retrieve all Users -
http://localhost:8102/repo/all


3. Add User settings entry by for a userId -
http://localhost:8102/repo/settings/AWdeQyaoTJbZRlQtLZfL/hobby/chess

For other apis, check code.


For detail explanation of this project check this blog - https://www.rajeshbhojwani.co.in/2018/12/overview-elasticsearch-real-time.html




