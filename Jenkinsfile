pipeline {
    agent any
    stages{
        stages('build'){
            steps  {
                sh 'mvn clean package'
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
}