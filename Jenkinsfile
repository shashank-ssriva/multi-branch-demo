pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh '/usr/local/bin/mvn -B -DskipTests clean package'
            }
        }
        stage('Test') {
            steps {
                sh '/usr/local/bin/mvn test'
            }
            post {
                always {
                    junit 'target/surefire-reports/*.xml'
                }
            }
        }
        stage('Deliver') {
            steps {
                sh './scripts/deliver.sh'
            }
        }
    }
}
