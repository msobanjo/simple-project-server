pipeline {
    agent any

    stages {
        stage('Testing Environment') {
            steps {
                    sh 'mvn test -Dtest=ControllerAndServiceSuite'
                    sh 'mvn test -Dtest=IntegrationSuite'
                }
            }
        stage('Build') {
            steps {
                sh 'mvn package -DskipTests'
                sh 'docker build -t="msobanjo/docker/simple-project:latest" .'
                }
            }
        stage('Deploy') {
            steps {
                sh 'docker login'
                sh 'docker push msobanjo/docker/simple-project:latest'
            }
        }
    }
}

