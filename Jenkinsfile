pipeline {

    agent any

    stages {
  
        stage('Build') {
            steps {
                ech 'Build Stage'
                sh 'docker build -t pyapp-image .'
            }
        }
        stage('Test') {
            steps {
                echo 'Test workflow still a work in progress.'
                echo 'Waiving Test Stage'
                //sh 'docker run -d --name pyapp-container pyapp-image'
                //sh 'RETVAL=${?}'
                //sh 'docker ps -a'
                //sh 'docker cp pyapp-container:./result.xml result.xml'
                //sh 'docker rm -f pyapp-container'
                //sh 'ls -al ./result.xml'
                //sh 'exit ${RETVAL}'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deployment'
                sh 'docker run -d --name pyapp-container -p 8000:8000 pyapp-image'
            }
        }
    }
}