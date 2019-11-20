pipeline {
    agent any

    stages {
        stage('Test') {
            steps {
                    sh 'mvn test -Dtest=ControllerAndServiceSuite'
                    sh 'mvn test -Dtest=IntegrationSuite'
                }
            }
        stage('Build') {
            steps {
                sh 'mvn package -DskipTests'
                sh 'docker build -t="msobanjo/simple-project:latest" .'
                }
            }
        stage('Deploy') {
            steps {
                sh 'docker push msobanjo/simple-project:latest'
            }
        }
         stage('Testing Environment') {
            steps {
                echo "hello"
            }
        }
      stage('Staging') {
            steps {
                echo "hello"
            }
        }
      stage('Production') {
            steps {
                echo "hello"
            }
        }
    }
}


