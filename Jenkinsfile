pipeline {
    agent any
    stages {
        stage('Back-end'){
            agent {
                docker { image 'maven:3.9.8-amazoncorretto-21-debian'}
            }
            steps{
                sh 'mvn --version'
            }

        }
        stage ('Front-end'){
            agent{
                docker { image 'node:16-alpine'}
            }
            steps{
                sh 'node --version'
            }
        }
        stage ('DB'){
            agent{
                docker { image 'mysql::oraclelinux9'}
            }
            steps{
                sh 'mysql --version'
            }
        }
    }

}
