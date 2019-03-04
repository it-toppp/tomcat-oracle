

docker-compose exec db sqlplus system/oracle

CREATE USER numtest IDENTIFIED BY numtest;
GRANT CONNECT,RESOURCE,DBA TO numtest;

docker-compose exec db imp system/oracle@xe FILE=/damp/numtest.dmp FROMUSER=numtest TOUSER=numtest

docker-compose exec admin flask mailu admin admin it-top.pp.ua password
