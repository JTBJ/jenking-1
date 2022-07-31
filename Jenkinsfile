pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                bat 'echo "Hello World"'
                bat '''
                    echo "Multiline shell steps works too"
                    cd ../../../IdeaProjects/swingPractice/src/selfPractice
                    javac Main.java
                    java Main.java
                '''
            }
        }
        stage('Test') {
            steps {
                bat '''echo "Fail!"; exit 1'''
            }
        }
    }
    post {
        always {
            bat '''echo "This will always run"'''
        }
        success {
            bat '''echo "This will run only if successful"'''
        }
        failure {
            bat '''echo "This will run only if failed"'''
        }
        unstable {
            bat '''echo "This will run only if the run was marked as unstable"'''
        }
        changed {
            bat '''echo "This will run only if the state of the Pipeline has changed"'''
            bat '''For example, if the Pipeline was previously failing but is now successful'''
        }
    }
}
