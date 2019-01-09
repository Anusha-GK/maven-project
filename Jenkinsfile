pipeline {
    agent any
 
    tools {
        maven 'localMaven'
    }
 
stages{
        stage('Build'){
            steps {
                sh 'mvn clean compile'
            }
            post {
                success {
                    echo 'Now Archiving...'
                    archiveArtifacts artifacts: '**/target/*.war'
                }
            }
        }
    }
}
