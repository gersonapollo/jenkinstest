pipeline {
    agent any

    stages {
        stage ('Compilation Stage') {
            steps{
                withMaven(maven: 'Maven_3_6_1') {
                    sh 'mvn clean compile'
                }
            }
        }

        stage ('Testing Stage') {
            steps{
                withMaven(maven: 'Maven_3_6_1') {
                    sh 'mvn test'
                }
            }
        }

        stage ('Deployment Stage') {
            steps{
                withMaven(maven: 'Maven_3_6_1') {
                    sh 'mvn deploy'
                }
            }
        }
    }
}
