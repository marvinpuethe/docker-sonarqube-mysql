# Docker Compose file for Sonarqube with MySQL

## Installation
1. Install docker and docker-compose
2. Clone the repository
3. Open terminal and cd into ./sonarqube-mysql
4. Run `docker-compose up -d`
5. Open browser and browse to `http://youripaddress:9000/`

## Parameters
| Name                      | Description                                                                           |
| ------------------------- | ------------------------------------------------------------------------------------- |
| MYSQL_ROOT_PASSWORD       | Password for root dbuser in mysql                                                     |
| MYSQL_DATABASE            | Database name in mysql used for storing sonarqube information                         |
| MYSQL_USER                | Dbuser used for connecting the sonarqube application                                  |
| MYSQL_PASSWORD            | Password for dbuser                                                                   |
| SONARQUBE_JDBC_USERNAME   | Username for connecting to the mysql db (make sure this is the same as MYSQL_USER)    |
| SONARQUBE_JDBC_PASSWORD   | Password for connecting to the mysql db (make sure this is the same as MYSQL_PASSWORD)|
| SONARQUBE_JDBC_URL        | JDBC Url for connecting to the mysql db                                               |