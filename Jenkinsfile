pipeline {

    agent any

    stages {

        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }

        stage('Docker Build') {
            steps {
                sh 'docker build -t tallaom/maven-demo:v1 .'
            }
        }

        stage('Docker Push') {
            steps {
                sh 'docker push tallaom/maven-demo:v1'
            }
        }

    }

}
