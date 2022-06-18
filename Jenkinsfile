pipeline {
    agents 'any'
    stages {
        stage('clone repo') {
            steps {
                echo 'cloning repo'
            }
        }
        stage('build docker') {
            steps {
                sh 'sudo docker rm -f $(docker ps -aq)'
                sh 'sudo docker build . -t mukeshktc/ubuntu_apache:4.0'  
            }
            
        }
        stage('test & publish') {
            steps {
                sh 'sudo docker run -it -d -p 82:80 mukeshktc/ubuntu_apache:4.0'
            }
        }
    }
}
