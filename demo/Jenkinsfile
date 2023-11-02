pipeline {
    agent any

    stages {
        stage ('GetProject') {
            steps {
                git 'https://github.com/CarthyP/Lab6SpringBootDemo.git'
            }
        }
        stage ('build') {
            steps {
                sh 'mvn clean'

            }
        }
        stage ('Package') {
            steps {
                sh 'mvn package'
            }
        }
        stage ('Archive')
        {
            steps {
                archiveArtifacts allowEmptyArchive: true,
                    artifacts: '**/demo*.war'
            }
        }
    }
}