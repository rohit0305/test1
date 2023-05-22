ubuntu image:
_____
1. docker pull ubuntu
2. sudo docker run -it ubuntu bash
3. apt-get -y update
4. apt-get -y install vim/nano/firefox
5. apt-get -y install sudo
6. sudo apt-get install nano
7. docker commit image new_name:tag
8. docker push new_name:tag



selenium-docker 
______
1. docker pull selenium/standalone-chrome
2. docker run -d -p 4444:4444 -v /dev/shm:/dev/shm selenium/standalone-chrome
3. go to localhost:4444/ui
4. Give password secret
5. python3 filename.py



sonarqube :
_____
1. docker run -d --name sonarqube1 -p 9000:9000 sonarqube
2. go to localhost:9000
3. login using admin/admin change creds
4. click manually
5. click locally
6. complete the process 
7. docker run --network=host    --rm     -e SONAR_HOST_URL="http://localhost:  9000"     -e SONAR_SCANNER_OPTS="-Dsonar.projectKey=sample-project"     -e SONAR_TOKEN="sqp_8ca6fc24d2df3217aacfc2fdad663c5b7456f4a8"     -v "<local_file_location>:/usr/src"     sonarsource/sonar-scanner-cli
