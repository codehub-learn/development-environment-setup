# Oracle Database Enterprise Edition on Docker Container Guide

1) In order to download the oracle database through Docker, you need an Oracle account.

2) Head to the follow link:
https://container-registry.oracle.com/ords/f?p=113:10

3) While in the website, click on "Database -> enterprise" and you should be located in a page with the title "Oracle Database Enterprise Edition"

4) On the right side, there is a License Agreement you need to Accept. Before doing anything else, you are required to accept the license agreement. You can set English as the language.

5) Run docker, then open a terminal and write the following command to sign in with your Oracle account:
docker login container-registry.oracle.com

6) Pull the oracle EE image:
docker pull container-registry.oracle.com/database/enterprise:21.3.0.0

7) Create a docker container from the image:
docker run -d --name ee -p 1521:1521 container-registry.oracle.com/database/enterprise:21.3.0.0

8) The initialization phase of the image takes a long time (~10-15 mins), so in order to see the progress of the phase, write the following in the same terminal window you used to run the container:
docker logs --follow ee

9) When the setup completes, open a new terminal window and run the following:
docker exec ee ./setPassword.sh 1234

10) In the same terminal window, run the following command to connect directly to the container environment:
docker exec -it ee sh

11) Then, start the database listener service using the following command:
lsnrctl start

11) Next, you need to connect to the database. The command  is the following:
sqlplus sys/1234@ORCLCDB as sysdba

12) Congratulations! You connected to the Oracle Database Server and now you can use it.
