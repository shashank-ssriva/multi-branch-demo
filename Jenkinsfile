pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
		sh 'echo "Triggered via develop branch. Will only build code."'
                sh '/usr/local/bin/mvn -B -DskipTests clean package'
            }
        }
 }
}
