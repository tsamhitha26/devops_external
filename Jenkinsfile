pipeline{
    agent any
    stages{
        stage('Build'){
            steps{
                echo 'Build Docker Image'
                bat 'docker build -t myapplication .'
            }
        }
        stage('Run'){
            steps{
                echo 'Running docker image in the container'
                bat 'docker rm -f myapplication || exit 0'
                bat 'docker run -d -p 5000:5000 --name=mycontainer myapplication'
            }
        }
    }
}
