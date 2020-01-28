# Java War with DB running on Tomcat

Experiment running Tomcat in the container, customized with adding jndi datasource `config/tomcat/conf/context.xml`
and MySql driver `config/tomcat/lib/mysql-connector-java-5.1.47.jar`

## todo - add all of this to kubernetes deployment 

docker run -d --name mysql -p 3306:3306 -e MYSQL_ROOT_PASSWORD=secret -e MYSQL_DATABASE=javatest mysql:5

docker image build -t ashumilov/dbapp ./

docker container run -it --publish 8080:8080 ashumilov/dbapp

http://localhost:8080/dbapp/dbtest
