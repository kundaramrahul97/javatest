pipeline {
    agent any

    tools{
        maven 'maven'
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('code quality') {
            steps {
                echo 'code quality'
            }
        }
        stage('Deploy Dev') {
            steps {
                echo 'Dev'
            }
        }
        stage('Deploy UAT') {
            steps {
                echo 'UAT'
            }
        }
        stage('Deploy Pre Prod') {
            steps {
                echo 'Pre prod'
            }
        }
        stage('Deploy to prod') {
            steps {
                echo 'prod'
            }
        }
    }
}