pipeline {
    agent any 
    stages {
        stage("build"){
            steps {
                script {
            sh """
            aws ecr get-login-password --region us-east-2 | docker login --username AWS --password-stdin 315073111691.dkr.ecr.us-east-2.amazonaws.com
            sudo docker build -t frontend .
            sudo docker tag frontend:latest 315073111691.dkr.ecr.us-east-2.amazonaws.com/frontend:latest
            sudo docker push 315073111691.dkr.ecr.us-east-2.amazonaws.com/frontend:latest

            """
        }
         }
    }
}
}
