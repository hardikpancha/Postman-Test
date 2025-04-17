pipeline {
    agent {
        docker {
            image 'postman/newman:alpine'
        }
    }
    stages {
        stage('Run Postman Tests') {
            steps {
                sh '''
                    newman run UsersAPIs.postman_collection.json \
                        -g workspace.postman_globals.json \
                        -r htmlextra
                '''
            }
        }
    }
}
