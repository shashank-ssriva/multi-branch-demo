pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
		sh 'echo "Triggered via develop branch. Will only build code."'
                sh 'mvn -B -DskipTests clean package'
            }
        }
 }
}
