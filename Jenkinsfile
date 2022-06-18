pipeline {
    agents 'any'
    stages {
        stage('clone repo') {
            steps {
                echo 'cloning repo'
                git branch: 'develop', url: 'https://github.com/mukeshktc/case-study.git'
            }
        }
        stage('build docker') {
            steps {
                sh 'sudo docker rm -f $(docker ps -aq)'
                sh 'sudo docker build . -t mukeshktc/ubuntu_apache:4.0'  
            }
            
        }
        
    }
}
