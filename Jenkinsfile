pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'mvn -B -DskipTests clean package'
            }
        }

        stage('Deploy'){
            when {
                branch 'master'
            }
            steps {
                echo 'Deploying to production...'
                // Add deployment steps here
            }
        }        
    }
}
// pipeline test 3
