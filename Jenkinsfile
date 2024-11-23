pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'mvn -B -DskipTests clean package'
            }
        }

        stage('Debug') {
            steps {
                sh 'env | grep BRANCH'
                echo "Detected branch: ${env.BRANCH_NAME}"
            }
        }

        stage('Deploy'){
            when {
                expression {
                    env.GIT_BRANCH == 'origin/master'
                }
            }
            steps {
                echo 'Deploying to production...'
                // Add deployment steps here
            }
        }        
    }
}
// pipeline test 4
