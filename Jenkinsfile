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
        stage('Prod approval') {
            steps {
                script{
                    if (env.BRANCH_NAME == "master"){
                        input("Proceed for Prod deployment approved ?")
                    }
                    
                }
            }
        }
        stage('Deploy to prod') {
            steps {
                echo 'prod'
            }
        }
    }
    post {
        always {
            echo 'One way or another, I have finished'
            deleteDir() /* clean up our workspace */
        }
        success {
            echo 'I succeeded!'
        }
        unstable {
            echo 'I am unstable :/'
        }
        failure {
            mail to: 'team@example.com',
             subject: "Failed Pipeline: ${currentBuild.fullDisplayName}",
             body: "Something is wrong with ${env.BUILD_URL}"
        }
        changed {
            echo 'Things were different before...'
        }
    }
       
}