pipeline {
    agent any 
    stages {
        stage("build"){
            sh """
            aws ecr get-login | docker login 
            docker build -t ecruurl:$BUILD_NUMBER .
            docker push ecruurl:$BUILD_NUMBER
            """
         }
    }
}