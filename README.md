# jenkins-integration


CI/CD with Jenkins using Pipelines and Docker
--------------------------------------------------

1) Jenkins Installation steps cmd

-> wget https://github.com/mibrahim-github-cloud/jenkins-integration/blob/main/scripts/install_jenkins.sh

-> bash install_jenkins.sh

--------------------------------------------------------------------------------
2) creating Jenkins CI with docker client(using the existing Jenkins image)

->docker ps -a

->git clone https://github.com/mibrahim-github-cloud/jenkins-docker

->cd jenkins-docker

->docker build -t jenkins-docker .

->docker stop jenkins

->docker rm jenkins

->ls /var/jenkins-home

->docker run -p 8080:8080 -p 50000:50000 -v /var/jenkins_home:/var/jenkins_home -v /var/run/docker.sock:/var/run/docker.sock -d --name jenkins jenkins-docker {using the same jenkins files}

->docker exec -it jenkins bash {verifying the docker.sock path}

->ls -ahl /var/run/docker.sock

--------------------------------------------------------------------------------
Refer=>https://github.com/wardviaene/jenkins-course
