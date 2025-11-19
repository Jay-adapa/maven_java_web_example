For APIs

# Run test
```
$mvnw clean test
```

# Create WAR file
```
$mvnw clean package
```

#  How to run web server with Apache Tomcat ?

```
$mvnw tomcat7:run
```

#  Run in browser 
* http://localhost:8080/api/hello
* http://localhost:8080/api/hello.html



## Step to create server

1. สร้าง MySQL Database
```
docker container run -d -p 3306:3306  \
-e MYSQL_ROOT_PASSWORD=password \
-e MYSQL_DATABASE=wallet \
-e MYSQL_USER=user01 \
-e MYSQL_PASSWORD=xitgmLwmp \
--name db2 mysql:5.7.21
```
/*<tomcat-users xmlns="http://tomcat.apache.org/xml" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://tomcat.apache.org/xml tomcat-users.xsd" version="1.0">
<role rolename="manager-gui"/>
<role rolename="manager-script"/>
<role rolename="manager-jmx"/>
<role rolename="manager-status"/>
<user username="admin" password="admin" roles="manager-gui,manager-script,manager-jmx,manager-status"/>
</tomcat-users>*/


/*
pipeline {
    agent any

    tools {
        maven 'Maven_Home'
    }

    stages {
        stage('Clone Repo & Clean') {
            steps {
                
                bat 'rmdir /s /q maven-simple'

                
                bat 'git clone https://github.com/manishwarMoturi/maven-simple.git'

               
                bat 'mvn clean -f maven-simple/pom.xml'
            }
        }

        stage('Install') {
            steps {
                bat 'mvn install -f maven-simple/pom.xml'
            }
        }

        stage('Test') {
            steps {
                bat 'mvn test -f maven-simple/pom.xml'
            }
        }

        stage('Package') {
            steps {
                bat 'mvn package -f maven-simple/pom.xml'
            }
        }
    }
}
*/
