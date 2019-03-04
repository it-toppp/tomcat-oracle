

docker-compose exec db sqlplus system/oracle

CREATE USER numtest IDENTIFIED BY numtest;
GRANT CONNECT,RESOURCE,DBA TO numtest;

imp system/oracle@xe FILE=/damp/numtest.dmp FROMUSER=numtest TOUSER=numtest
