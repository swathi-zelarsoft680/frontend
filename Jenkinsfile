pipeline{
    agent any

    stages {

        stage('prepare Artifacts') {
            steps {
                sh '''
                zip -r frontend.zip *
            '''
            }

        }
        stage('upload Artifacts') {
            steps {
                sh '''
           curl -f -v -u admin:momdad007 --upload-file frontend.zip http://172.31.9.76:8081/repository/frontend/frontend.zip
        '''
            }
        }
    }
}