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
                echo "hello"
                }
            }
        stage('Deploy') {
            steps {
                echo "hi"
            }
        }
    }
}

