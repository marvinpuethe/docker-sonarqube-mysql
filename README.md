# Docker Compose file for Sonarqube with MySQL

## Installation

1. Install docker and docker-compose
1. Clone the repository
1. Open terminal and cd into ./sonarqube-mysql
1. Run `docker-compose up -d`
1. Open browser and browse to <http://youripaddress:9000/>

## Complete installation instructions for Ubuntu

### Docker

I.e. with convenience script:

```bash
curl -fsSL get.docker.com -o get-docker.sh
sudo sh get-docker.sh
```

> <https://docs.docker.com/engine/installation/linux/docker-ce/ubuntu/>

### Sonarqube with MySQL

```bash
// Clone repository
sudo apt-get install git
git clone https://github.com/marvinpuethe/docker-sonarqube-mysql.git

// Start docker-compose
cd docker-sonarqube-mysql/sonarqube-mysql
docker-compose up -d
```

## Environment Parameters

| Name                      | Description                                                                           |
| ------------------------- | ------------------------------------------------------------------------------------- |
| MYSQL_ROOT_PASSWORD       | Password for root dbuser in mysql                                                     |
| MYSQL_DATABASE            | Database name in mysql used for storing sonarqube information                         |
| MYSQL_USER                | Dbuser used for connecting the sonarqube application                                  |
| MYSQL_PASSWORD            | Password for dbuser                                                                   |
| SONARQUBE_JDBC_USERNAME   | Username for connecting to the mysql db (make sure this is the same as MYSQL_USER)    |
| SONARQUBE_JDBC_PASSWORD   | Password for connecting to the mysql db (make sure this is the same as MYSQL_PASSWORD)|
| SONARQUBE_JDBC_URL        | JDBC Url for connecting to the mysql db                                               |