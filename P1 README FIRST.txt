
Please connect to db2 first with docker

-------------------------For Docker Terminal-------------------
docker pull ibmcom/db2
 
docker run -itd --name mydb2 --privileged=true -p 50000:50000 -e LICENSE=accept -e DB2INST1_PASSWORD=kenward -e DBNAME=testdb -v luw:/database ibmcom/db2
 
docker exec -ti mydb2 bash -c "su - db2inst1"
 
db2 connect to cs157a

db2 -tvf p1_create.sql 
-------------------------For Docker Terminal-------------------




-------------------------Formal Terminal-------------------
FIRST

javac BankingSystem.java
javac P1.java
javac programLauncher.java

SECOND

java -cp ":./db2jcc4.jar" ProgramLauncher ./db.properties

Or.....
Check result with test1.out notes:
java -cp ":./db2jcc4.jar" ProgramLauncher ./db.properties > test1.out

MADE A RESULT FOR CODE

-------------------------Formal Terminal-------------------

